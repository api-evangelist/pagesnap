# Pagesnap

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Pagesnap turns any publicly reachable HTTP(S) URL into clean LLM-ready Markdown, a screenshot, a PDF, link-preview metadata, or normalized structured data, and extends the same engine to robots-aware site crawls, llms.txt generation, two-page diffs, and persisted change monitors with signed webhooks. The 66-operation REST API is described by a generated OpenAPI 3.1 contract and is callable anonymously at 30 requests/day with no signup, keyed at higher quota, or keylessly per call via x402 v2 exact USDC payments on Base. The same capabilities are projected through a hosted Streamable HTTP MCP server (11 tools, anonymous), an A2A 1.0 JSON-RPC agent with a JWS-signed agent card, and an Agentic Resource Discovery manifest. Pagesnap is an explicit experiment: it was designed, built, deployed, documented and is operated by AI coding agents within a scope set by a human owner who retains control of the single New York VPS and the self-custodied payment wallet. There is no SLA, no failover, and no compliance certification, and the service says so plainly on its own trust page.

**Areas:** Developer Tools · Web Scraping · web-to-markdown · Screenshots · PDF Generation · Metadata Extraction · MCP · A2A · x402 · AI Agents · Content Extraction · Structured Data

## Pagesnap on APIs.io

Everything profiled for Pagesnap is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/pagesnap/](https://apis.io/providers/pagesnap/)** — or go straight to one of the APIs or properties below.

### APIs (11)

- [Pagesnap Account API](https://apis.io/apis/pagesnap/pagesnap-account-api/) — Keys, usage, referrals
- [Pagesnap Agents API](https://apis.io/apis/pagesnap/pagesnap-agents-api/) — MCP and A2A protocols
- [Pagesnap Billing API](https://apis.io/apis/pagesnap/pagesnap-billing-api/) — Checkout and receipts
- [Pagesnap Content API](https://apis.io/apis/pagesnap/pagesnap-content-api/) — Reading and rendering
- [Pagesnap Crawl API](https://apis.io/apis/pagesnap/pagesnap-crawl-api/) — Site crawls and asynchronous jobs
- [Pagesnap Diff API](https://apis.io/apis/pagesnap/pagesnap-diff-api/) — Two-page comparison
- [Pagesnap Discovery API](https://apis.io/apis/pagesnap/pagesnap-discovery-api/) — Machine-readable discovery resources
- [Pagesnap Monitors API](https://apis.io/apis/pagesnap/pagesnap-monitors-api/) — Persisted change monitoring
- [Pagesnap Status API](https://apis.io/apis/pagesnap/pagesnap-status-api/) — Public health and stats
- [Pagesnap Support API](https://apis.io/apis/pagesnap/pagesnap-support-api/) — Capability-based support tickets
- [Pagesnap X402 API](https://apis.io/apis/pagesnap/pagesnap-x402-api/) — Keyless USDC per-call payment

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Pagesnap Webhooks](https://apis.io/asyncapis/pagesnap/pagesnap-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [mcp](https://apis.io/servers/pagesnap/mcp/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Pagesnap Api Overlay](https://apis.io/overlays/pagesnap/pagesnap-api-overlay/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Pagesnap Authentication](https://apis.io/security/pagesnap/pagesnap-authentication/)
- [Pagesnap Domain Security](https://apis.io/security/pagesnap/pagesnap-domain-security/)
- [Pagesnap Trust Center](https://apis.io/security/pagesnap/pagesnap-trust-center/)
- [Pagesnap Vulnerability Disclosure](https://apis.io/security/pagesnap/pagesnap-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Pagesnap Plans Pricing](https://apis.io/plans/pagesnap/pagesnap-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Pagesnap Rate Limits](https://apis.io/rate-limits/pagesnap/pagesnap-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Documentation](https://pagesnap.142-93-197-141.sslip.io/docs)
- [Getting started](https://pagesnap.142-93-197-141.sslip.io/agents)
- [API reference](https://pagesnap.142-93-197-141.sslip.io/docs)
- [Pricing](https://pagesnap.142-93-197-141.sslip.io/pricing)
- [Sign up](https://pagesnap.142-93-197-141.sslip.io/keys)
- [Support](https://pagesnap.142-93-197-141.sslip.io/support)
- [Changelog](https://pagesnap.142-93-197-141.sslip.io/log)
- [Terms of service](https://pagesnap.142-93-197-141.sslip.io/terms)
- [Privacy policy](https://pagesnap.142-93-197-141.sslip.io/terms)
- [GitHub](https://github.com/CalibratedGhosts)
- [Status](https://pagesnap.142-93-197-141.sslip.io/status)

## API Evangelist rating

**Unrated** — no public website could be reached for this company, so there was almost nothing to measure and nothing a reader could check.

This is not a score of zero. No rating is published for this company. If that is wrong because something public exists that we missed, say so on this repository or email [info@apievangelist.com](mailto:info@apievangelist.com) and it will be re-run — free, and no justification needed.

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Pagesnap: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/pagesnap/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
