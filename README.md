# Juro (juro)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Juro is an AI-native contract automation and contract lifecycle management (CLM) platform where legal, sales, HR, and finance teams create, negotiate, sign, and manage contracts in one browser-based workspace. Juro exposes a documented public REST API (v3, base `https://api.juro.com/v3`, with a sandbox at `https://api-sandbox.juro.io/v3`) authenticated with an `x-api-key` header. The API lets external systems initiate contracts from templates, upload PDFs, edit smart fields, send contracts for e-signature, download signed PDFs, and subscribe to contract lifecycle webhook events.

**Access model:** Juro's API is **plan-gated**. API access is included with a Juro subscription and enabled through your Customer Success Manager, and the monthly request quota depends on your plan (roughly 100 requests/month on free access, roughly 30,000/month on paid). Live calls require an eligible plan and an issued `x-api-key`. This catalog entry was built from Juro's public API reference ([api-docs.juro.com](https://api-docs.juro.com/)) and help center; the Contracts, Templates, and Signatures endpoints are confirmed there, while the programmatic Webhooks-management endpoints are **modeled** (webhooks are primarily configured in the Juro app) and flagged as such.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/juro/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/juro/refs/heads/main/apis.yml)

## Tags

- Contract Management
- CLM
- Contract Lifecycle
- Contract Automation
- Legal
- LegalTech
- E-Signature
- Contracts

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

### Juro Contracts API

Create, retrieve, list, update, and delete contracts. Initiate a contract from a Juro template with smart-field data, upload an existing PDF to create a contract, patch contract properties, list contracts with skip/limit pagination, and download the generated or signed PDF as binary. This is the core surface for the contract management use case.

- **Human URL:** [https://api-docs.juro.com/](https://api-docs.juro.com/)
- **Base URL:** `https://api.juro.com/v3`

#### Tags

- Contract Management
- CLM
- Contracts
- Contract Lifecycle

#### Properties

- [Documentation](https://api-docs.juro.com/)
- [API Reference](https://api-docs.juro.com/)
- [OpenAPI](openapi/juro-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/juro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/juro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Juro Templates API

List the contract templates available to the API key holder and retrieve a specific template, including its smart fields, so external systems know what data to supply when initiating a new contract via the Contracts API.

- **Human URL:** [https://api-docs.juro.com/](https://api-docs.juro.com/)
- **Base URL:** `https://api.juro.com/v3`

#### Tags

- Templates
- Contract Management
- CLM

#### Properties

- [Documentation](https://api-docs.juro.com/)
- [OpenAPI](openapi/juro-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/juro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/juro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Juro Signatures API

Drive the e-signature stage of the contract lifecycle. Apply a signature to a contract, send a signing request to a signing side, and send a signing request to a specific signatory — moving a contract from drafted to fully executed without leaving your own system.

- **Human URL:** [https://api-docs.juro.com/](https://api-docs.juro.com/)
- **Base URL:** `https://api.juro.com/v3`

#### Tags

- E-Signature
- Signatures
- Contract Lifecycle
- Legal

#### Properties

- [Documentation](https://api-docs.juro.com/)
- [OpenAPI](openapi/juro-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/juro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/juro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Juro Webhooks API

Subscribe to real-time contract lifecycle events and receive them as outbound webhooks — `contract.created`, `contract.signed`, `contract.edit`, `contract.pdf_generated`, `contract.viewed`, `contract.commented`, and the full approval-request event set. Webhooks are configured in the Juro app under Settings > Integrations > Webhooks; the programmatic registration endpoints are **modeled** from Juro's help-center guidance and flagged `endpointsModeled` where not confirmed in the public reference. Payloads support Basic auth or HMAC-SHA256 signature validation.

- **Human URL:** [https://api-docs.juro.com/](https://api-docs.juro.com/)
- **Base URL:** `https://api.juro.com/v3`

#### Tags

- Webhooks
- Events
- Contract Lifecycle
- CLM

#### Properties

- [Documentation](https://api-docs.juro.com/)
- [OpenAPI](openapi/juro-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/juro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/juro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Authentication](authentication/juro-authentication.yml)
- [LinkedIn](https://www.linkedin.com/company/juro)
- [Website](https://juro.com)
- [Documentation](https://api-docs.juro.com/)
- [Plans](plans/juro-plans-pricing.yml)
- [Rate Limits](rate-limits/juro-rate-limits.yml)
- [Fin Ops](finops/juro-finops.yml)
- [Pricing](https://juro.com/pricing)
- [Terms of Service](https://juro.com/terms/api-terms)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
