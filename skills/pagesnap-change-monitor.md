---
generated: '2026-09-02'
method: generated
source: openapi/pagesnap-openapi.json + https://pagesnap.142-93-197-141.sslip.io/docs
name: pagesnap-change-monitor
description: >-
  Create a Pagesnap change monitor on a public page, verify its signed webhook, and manage its
  lifecycle. Use when something must be watched over time rather than read once — a pricing page,
  a policy, a status note.
api: Pagesnap API
operations:
  - createMonitor
  - listMonitors
  - getMonitor
  - checkMonitor
  - pauseMonitor
  - resumeMonitor
  - deleteMonitor
---

# Watch a page for changes

Monitors are the one Pagesnap surface that **requires an API key** (`401 KEY_REQUIRED` otherwise)
and the one that creates durable state. Create one at `POST /v1/keys` (`createKey`) if you have
none — no email needed.

## 1. Create

`POST /v1/monitors` (`createMonitor`):

```bash
curl -X POST "https://pagesnap.142-93-197-141.sslip.io/v1/monitors" \
  -H "Authorization: Bearer ps_live_…" -H 'content-type: application/json' \
  -d '{"url":"https://example.com/pricing","mode":"text","interval":"24h",
       "selector":"main","threshold_percent":1,
       "webhook_url":"https://hooks.example.net/pagesnap"}'
```

- `mode`: `text` | `visual` | `meta`. `visual` accepts the full screenshot option set.
- `interval`: `24h` on Free; `1h`, `6h`, `24h` on paid. A higher tier than your plan returns
  `403 PLAN_INTERVAL`.
- Plan caps: Free 2, Starter 10, Pro 50, Scale 200 → `429 MONITOR_LIMIT`.

**The 201 response carries `webhook_secret` exactly once.** `listMonitors` deliberately omits it
and there is no rotation or re-reveal operation. Store it on receipt or you cannot verify
deliveries.

## 2. Verify the webhook

Pagesnap signs the **exact JSON request body, including its timestamp**:

```
X-Pagesnap-Signature: sha256=<hex HMAC-SHA256>
```

Verify the **raw bytes** with a constant-time comparison *before* parsing, then reject timestamps
outside your replay window. Deliveries time out at 10 s and retry three times; redirects are not
followed and response bodies are discarded. After 20 consecutive failed change deliveries the
webhook is disabled — the monitor stays active but goes silent, so alert on
`webhook_enabled: false` in `getMonitor`.

Slack and Discord destinations receive injection-safe native payloads.

## 3. Manage

- `GET /v1/monitors` (`listMonitors`) — the key's monitors.
- `GET /v1/monitors/{monitor_id}` (`getMonitor`) — monitor plus recent checks.
- `POST /v1/monitors/{monitor_id}/check` (`checkMonitor`) — run now; consumes one request.
- `POST …/pause` (`pauseMonitor`) and `POST …/resume` (`resumeMonitor`) — a true reversible pair
  with no deadline; history is preserved.
- `DELETE /v1/monitors/{monitor_id}` (`deleteMonitor`) — **permanent**. It deletes the monitor and
  every stored snapshot, check and diff. There is no restore operation and no grace window.
  Prefer `pauseMonitor` unless you are certain.

## Rules

- Each scheduled or manual check consumes one request. Exhausted quota or a disabled key pauses
  the monitor (`paused_reason` says which).
- Retained: latest 100 checks, 10 changed snapshots and 10 diffs per monitor; snapshots capped at
  500 KB (`413 SNAPSHOT_TOO_LARGE` above that).
- `409 MONITOR_RUNNING` / `MONITOR_PAUSED` are state conflicts — read state, then act.
- The webhook destination passes the same public-address policy as a monitored target and is
  re-resolved on every attempt. Internal endpoints will be refused.
