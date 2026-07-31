# CargoAi (cargoai)

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
