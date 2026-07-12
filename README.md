# Juro (juro)

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
