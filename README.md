# Autodesk Construction Cloud (autodesk-construction-cloud)

Autodesk Construction Cloud (ACC) is a unified platform connecting workflows, teams, and data across the construction project lifecycle, integrating preconstruction, design collaboration, project management, and field execution tools. ACC provides REST APIs through the Autodesk Platform Services (APS) for programmatic access to project management, issues, RFIs, submittals, cost management, model coordination, and data export capabilities.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Construction
- BIM
- Project Management
- AEC
- CAD
- Architecture
- Engineering
- Field Management

## Timestamps

- **Created:** 2025-01-01
- **Modified:** 2026-05-19

## APIs

### Autodesk Construction Cloud Admin API

The Autodesk Construction Cloud Admin API provides programmatic management of ACC accounts, projects, users, and company settings. REST APIs enable automation of project provisioning, user access control, and account-level administration across ACC and BIM 360 deployments.

- **Human URL:** [https://aps.autodesk.com/en/docs/acc/v1/overview/](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- **Base URL:** `https://developer.api.autodesk.com`

#### Tags

- ACC
- Administration
- BIM
- Construction
- Project Management

#### Properties

- [Documentation](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [API Reference](https://aps.autodesk.com/en/docs/acc/v1/reference/http/admin-accounts-accountidprojects-GET/)
- [Getting Started](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/openapi/acc-admin-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/acc-admin.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/acc-admin.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/acc-issues.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/acc-issues.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Autodesk Construction Cloud Issues API

The ACC Issues API enables creation, retrieval, and management of construction issues, observations, and punch list items. REST APIs integrate with field management workflows for quality control, safety reporting, and project closeout in Autodesk Construction Cloud.

- **Human URL:** [https://aps.autodesk.com/en/docs/acc/v1/overview/](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- **Base URL:** `https://developer.api.autodesk.com`

#### Tags

- BIM
- Construction
- Field Management
- Issues
- Quality

#### Properties

- [Documentation](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [API Reference](https://aps.autodesk.com/en/docs/acc/v1/reference/http/issues-issues-POST/)
- [Getting Started](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/openapi/acc-issues-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [JSON Schema](https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/json-schema/acc-issue-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/examples/acc-issue-example.json)
- [Postman Collection](collections/acc-admin.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/acc-admin.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/acc-issues.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/acc-issues.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Autodesk Construction Cloud Cost Management API

The ACC Cost Management API provides access to budget codes, contract lifecycle management, and expense tracking in Autodesk Construction Cloud. REST APIs enable ERP integration, change order management, and financial reporting across construction project portfolios.

- **Human URL:** [https://aps.autodesk.com/en/docs/acc/v1/overview/](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- **Base URL:** `https://developer.api.autodesk.com`

#### Tags

- ACC
- Budget
- Construction
- Contracts
- Cost Management

#### Properties

- [Documentation](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [API Reference](https://aps.autodesk.com/en/docs/acc/v1/reference/http/cost-actions-POST/)
- [Getting Started](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)
- [Postman Collection](collections/acc-admin.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/acc-admin.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/acc-issues.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/acc-issues.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Autodesk Construction Cloud Model Coordination API

The ACC Model Coordination API enables access to model sets, clash detection results, and coordination issues in Autodesk Construction Cloud. REST APIs support automated BIM coordination workflows, clash review automation, and model aggregation across design disciplines.

- **Human URL:** [https://aps.autodesk.com/en/docs/acc/v1/overview/](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- **Base URL:** `https://developer.api.autodesk.com`

#### Tags

- BIM
- Clash Detection
- Construction
- IFC
- Model Coordination

#### Properties

- [Documentation](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [API Reference](https://aps.autodesk.com/en/docs/acc/v1/reference/http/mc-modelset-service-v3-create-model-set-POST/)
- [Getting Started](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)
- [Postman Collection](collections/acc-admin.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/acc-admin.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/acc-issues.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/acc-issues.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Autodesk Construction Cloud RFIs API

The ACC RFIs API enables management of Requests for Information (RFIs) in Autodesk Construction Cloud. REST APIs support RFI creation, tracking, response workflows, and reporting for construction project documentation and decision management.

- **Human URL:** [https://aps.autodesk.com/en/docs/acc/v1/overview/](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- **Base URL:** `https://developer.api.autodesk.com`

#### Tags

- ACC
- Construction
- Document Management
- RFI

#### Properties

- [Documentation](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [API Reference](https://aps.autodesk.com/en/docs/acc/v1/reference/http/rfis-rfi-search-POST/)
- [Getting Started](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)
- [Postman Collection](collections/acc-admin.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/acc-admin.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/acc-issues.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/acc-issues.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Autodesk Construction Cloud Submittals API

The ACC Submittals API provides programmatic access to submittal workflows in Autodesk Construction Cloud. REST APIs support submittal item creation, review routing, approval tracking, and specification section management for construction project compliance.

- **Human URL:** [https://aps.autodesk.com/en/docs/acc/v1/overview/](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- **Base URL:** `https://developer.api.autodesk.com`

#### Tags

- ACC
- Construction
- Document Management
- Submittals

#### Properties

- [Documentation](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [API Reference](https://aps.autodesk.com/en/docs/acc/v1/reference/http/submittals-items-GET/)
- [Getting Started](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)
- [Postman Collection](collections/acc-admin.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/acc-admin.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/acc-issues.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/acc-issues.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Autodesk Construction Cloud Data Connector API

The ACC Data Connector API enables bulk extraction of project data from Autodesk Construction Cloud for analytics and reporting. REST APIs support scheduled and on-demand data exports across issues, RFIs, submittals, assets, and other project modules for business intelligence integration.

- **Human URL:** [https://aps.autodesk.com/en/docs/acc/v1/overview/](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- **Base URL:** `https://developer.api.autodesk.com`

#### Tags

- ACC
- Analytics
- Construction
- Data Export

#### Properties

- [Documentation](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [API Reference](https://aps.autodesk.com/en/docs/acc/v1/reference/http/data-connector-requests-POST/)
- [Getting Started](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)
- [Postman Collection](collections/acc-admin.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/acc-admin.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/acc-issues.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/acc-issues.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/autodesk-construction-cloud)
- [Website](https://www.autodesk.com)
- [Portal](https://aps.autodesk.com/)
- [Documentation](https://aps.autodesk.com/developer/documentation)
- [Getting Started](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)
- [Quickstart](https://get-started.aps.autodesk.com/)
- [Terms of Service](https://www.autodesk.com/company/legal-notices-trademarks/terms-of-service-autodesk360-web-services/forge-platform-web-services-api-terms-of-service)
- [Privacy Policy](https://www.autodesk.com/company/legal-notices-trademarks/privacy-statement)
- [Status Page](https://health.autodesk.com/)
- [Support](https://aps.autodesk.com/contact-support)
- [Changelog](https://aps.autodesk.com/topics/platform-updates)
- [GitHub Organization](https://github.com/autodesk-platform-services)
- [AsyncAPI](https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/asyncapi/acc-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [JSON Schema](https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/json-schema/acc-project-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/json-ld/acc-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
