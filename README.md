# CargoAi (cargoai)

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

CargoAi is a Singapore-headquartered air cargo technology company that operates CargoMART, a digital marketplace where freight forwarders search routes, schedules, capacity and rates across 680+ airlines, book them, transmit the electronic air waybill, and track the shipment end to end. It sits in the middle of the air cargo chain as an aggregator between forwarders and their TMS vendors on one side and airline reservation and messaging systems on the other. Its API posture is genuinely public in documentation and sales-gated in access - the CargoCONNECT developer portal at cargoai.readme.io is open to anyone with no login and publishes a real OpenAPI 3.1 definition per operation, but an x-api-key is issued only after a commercial conversation with the CargoAi enterprise team. The published contract is a proprietary REST shape rather than an IATA ONE Record interface, though the payloads it carries are IATA-native - AWB numbers with airline prefixes, IATA airport and airline codes, Special Handling Codes, IATA cargo status event codes, FWB and FHL message content, and CO2 figures computed per IATA Recommended Practice 1678.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cargoai/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cargoai/refs/heads/main/apis.yml)

## Tags

- Logistics
- Supply Chain
- Singapore
- Air Cargo
- Freight Forwarding
- Track and Trace
- Booking
- Marketplace
- Standards

## Timestamps

- **Created:** 2026-07-30
- **Modified:** 2026-07-30

## APIs

### CargoAi Routes, Schedules and Rates API

Search live routes, schedules, capacity, availability and rates across CargoAi's airline network from a single POST /search call, returning quotable flight options with rate types, transit times and CO2 per option.

- **Human URL:** [https://cargoai.readme.io/reference/routes-schedules-and-rates-endpoint-post](https://cargoai.readme.io/reference/routes-schedules-and-rates-endpoint-post)
- **Base URL:** `https://api.cargoai.co/solutions`

#### Tags

- Quoting and Rating
- Capacity
- Air Cargo

#### Properties

- [OpenAPI](openapi/cargoai-routes-schedules-and-rates-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://cargoai.readme.io/reference/routes-schedules-and-rates)
- [Documentation](https://cargoai.readme.io/reference/rate-types)
- [Documentation](https://cargoai.readme.io/reference/rate-search-types-coloader-behaviour)
- [Documentation](https://cargoai.readme.io/reference/product-coverage)
- [Documentation](https://cargoai.readme.io/reference/search-response-objects-definition)
- [Documentation](https://cargoai.readme.io/reference/air-freight-calculations)
- [API Reference](https://cargoai.readme.io/reference/routes-schedules-and-rates-endpoint-post)

### CargoAi Booking API

Book a quoted air cargo option, read a booking back by flight UUID, and cancel a booking made through CargoCONNECT. Booking updates from the airline are pushed back on a customer-registered booking callback URL.

- **Human URL:** [https://cargoai.readme.io/reference/booking](https://cargoai.readme.io/reference/booking)
- **Base URL:** `https://api.cargoai.co/solutions`

#### Tags

- Booking
- Air Cargo

#### Properties

- [OpenAPI](openapi/cargoai-booking-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://cargoai.readme.io/reference/booking)
- [Documentation](https://cargoai.readme.io/reference/booking-status)
- [Documentation](https://cargoai.readme.io/reference/booking-payments)
- [Documentation](https://cargoai.readme.io/reference/booking-errors)
- [Documentation](https://cargoai.readme.io/reference/booking-callback)
- [Documentation](https://cargoai.readme.io/reference/flywindow)
- [Documentation](https://cargoai.readme.io/reference/flywindow-callback-details)
- [Documentation](https://cargoai.readme.io/reference/search-book-flow)
- [API Reference](https://cargoai.readme.io/reference/booking-endpoint-post)

### CargoAi Track & Trace API

Subscribe an air waybill to CargoAi's milestone tracking service and receive event updates by webhook callback and email, or unsubscribe. Supports interline subscriptions that merge two carriers' milestones into one de-duplicated timeline.

- **Human URL:** [https://cargoai.readme.io/reference/track-and-trace](https://cargoai.readme.io/reference/track-and-trace)
- **Base URL:** `https://api.cargoai.co/solutions`

#### Tags

- Track and Trace
- Webhooks
- Air Cargo

#### Properties

- [OpenAPI](openapi/cargoai-track-and-trace-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://cargoai.readme.io/reference/track-and-trace)
- [Documentation](https://cargoai.readme.io/reference/tracking-event-codes)
- [Documentation](https://cargoai.readme.io/reference/subscription-e-mail-and-url-updates)
- [Documentation](https://cargoai.readme.io/reference/interline-tracking)
- [Documentation](https://cargoai.readme.io/reference/track-trace-premium)
- [Documentation](https://cargoai.readme.io/reference/ai-tracking-predictive-alerts)
- [Documentation](https://cargoai.readme.io/reference/guide-to-track-trace-data)
- [Documentation](https://cargoai.readme.io/reference/airfreight-track-and-trace)
- [API Reference](https://cargoai.readme.io/reference/tracking-subscription-endpoint-post)

### CargoAi FWB & FHL API

Send master (FWB) and house (FHL) air waybill data to the airline handling a booking as JSON, with CargoAi parsing and formatting it into the IATA cargo message the airline expects, so the caller needs no in-house EDI expertise.

- **Human URL:** [https://cargoai.readme.io/reference/fwb-and-fhl](https://cargoai.readme.io/reference/fwb-and-fhl)
- **Base URL:** `https://api.cargoai.co/solutions`

#### Tags

- Documentation and eAWB
- EDI
- Air Cargo

#### Properties

- [OpenAPI](openapi/cargoai-fwb-fhl-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://cargoai.readme.io/reference/fwb-and-fhl)
- [Documentation](https://cargoai.readme.io/reference/eawb-data-format)
- [API Reference](https://cargoai.readme.io/reference/eawb-endpoint-post)

### CargoAi User Provisioning API

Create, read, update and delete the end users an integrator carries under its own CargoCONNECT API key, and mint a redirection token that drops a user into the CargoMART portal without a separate login.

- **Human URL:** [https://cargoai.readme.io/reference/user-provisioning](https://cargoai.readme.io/reference/user-provisioning)
- **Base URL:** `https://api.cargoai.co/solutions`

#### Tags

- User Management
- Provisioning

#### Properties

- [OpenAPI](openapi/cargoai-user-provisioning-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://cargoai.readme.io/reference/user-provisioning)
- [Documentation](https://cargoai.readme.io/reference/data-format)
- [API Reference](https://cargoai.readme.io/reference/create-user)
- [API Reference](https://cargoai.readme.io/reference/get-token)

### CargoAi Cargo2ZERO CO2 API

Return the CO2 emissions for an air waybill or a specific flight leg, calculated per IATA Recommended Practice 1678 using the exact routing and aircraft code rather than an origin-destination approximation.

- **Human URL:** [https://cargoai.readme.io/reference/co2calculation](https://cargoai.readme.io/reference/co2calculation)
- **Base URL:** `https://api.cargoai.co/solutions`

#### Tags

- Sustainability
- Emissions
- Air Cargo

#### Properties

- [OpenAPI](openapi/cargoai-cargo2zero-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [API Reference](https://cargoai.readme.io/reference/co2calculation)
- [Documentation](https://www.iata.org/en/programs/cargo/sustainability/carbon-footprint/)

### CargoAi CargoCOPILOT API

AI extraction endpoints that turn an air waybill image or raw shipment email text into structured JSON that can be fed straight into the quote, book and eAWB endpoints, removing manual re-keying between parties.

- **Human URL:** [https://cargoai.readme.io/reference/cargocopilot-api](https://cargoai.readme.io/reference/cargocopilot-api)
- **Base URL:** `https://api.cargoai.co/solutions`

#### Tags

- AI
- Document Extraction
- Air Cargo

#### Properties

- [OpenAPI](openapi/cargoai-cargocopilot-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://cargoai.readme.io/reference/cargocopilot-api)
- [API Reference](https://cargoai.readme.io/reference/awb-extraction)
- [API Reference](https://cargoai.readme.io/reference/shipment-extraction)

### CargoAi MCP Connector

A hosted Model Context Protocol server that wraps the CargoCONNECT endpoints as tools for AI assistants - track a shipment by AWB, search flight rates, look up airline contacts and ground handling agents, and manage tracking subscriptions. OAuth 2.0, restricted to CargoMART Premium and Ultimate offices.

- **Human URL:** [https://cargoai.readme.io/reference/cargoai-mcp-connector-setup-documentation](https://cargoai.readme.io/reference/cargoai-mcp-connector-setup-documentation)
- **Base URL:** `https://api.cargoai.co/mcp`

#### Tags

- MCP
- AI Agents
- Air Cargo

#### Properties

- [Documentation](https://cargoai.readme.io/reference/cargoai-mcp-connector-setup-documentation)

## Common Properties

- [Website](https://www.cargoai.co/)
- [Documentation](https://cargoai.readme.io/reference/introduction)
- [API Reference](https://cargoai.readme.io/reference/introduction)
- [LLMs.txt](https://cargoai.readme.io/llms.txt)
- [Change Log](https://cargoai.readme.io/reference/changelog)
- [Support Portal](https://help.cargoai.co/)
- [Blog](https://www.cargoai.co/blog/)
- [Product Page](https://www.cargoai.co/products/cargoconnect/)
- [Portal](https://app.cargoai.co)
- [Sign Up](https://connect.cargoai.co/)
- [Contact](https://cargoai.readme.io/reference/contact-us)
- [Coverage](https://bi.cargoai.co/superset/dashboard/API_Coverage)
- [GitHub Organization](https://github.com/cargoai)
- [Linked In](https://sg.linkedin.com/company/cargoai)

## Maintainers

**FN:** Kin Lane  
**Email:** kin@apievangelist.com
