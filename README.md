# Autodesk Construction Cloud (autodesk-construction-cloud)

Autodesk Construction Cloud (ACC) is a unified platform connecting workflows, teams, and data across the construction project lifecycle, integrating preconstruction, design collaboration, project management, and field execution tools. ACC provides REST APIs through the Autodesk Platform Services (APS) for programmatic access to project management, issues, RFIs, submittals, cost management, model coordination, and data export capabilities.

**URL:** [https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/autodesk-construction-cloud/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Construction, BIM, Project Management, AEC, CAD, Architecture, Engineering, Field Management

## Timestamps

- **Created:** 2025-01-01
- **Modified:** 2026-04-19

## APIs

### Autodesk Construction Cloud Admin API

The Autodesk Construction Cloud Admin API provides programmatic management of ACC accounts, projects, users, and company settings. REST APIs enable automation of project provisioning, user access control, and account-level administration across ACC and BIM 360 deployments.

**Human URL:** [https://aps.autodesk.com/en/docs/acc/v1/overview/](https://aps.autodesk.com/en/docs/acc/v1/overview/)

#### Tags:

 - ACC, Administration, BIM, Construction, Project Management

#### Properties

- [Documentation](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [APIReference](https://aps.autodesk.com/en/docs/acc/v1/reference/http/admin-accounts-accountidprojects-GET/)
- [GettingStarted](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)
- [OpenAPI](openapi/acc-admin-openapi.yml)

### Autodesk Construction Cloud Issues API

The ACC Issues API enables creation, retrieval, and management of construction issues, observations, and punch list items. REST APIs integrate with field management workflows for quality control, safety reporting, and project closeout in Autodesk Construction Cloud.

**Human URL:** [https://aps.autodesk.com/en/docs/acc/v1/overview/](https://aps.autodesk.com/en/docs/acc/v1/overview/)

#### Tags:

 - BIM, Construction, Field Management, Issues, Quality

#### Properties

- [Documentation](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [APIReference](https://aps.autodesk.com/en/docs/acc/v1/reference/http/issues-issues-POST/)
- [GettingStarted](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)
- [OpenAPI](openapi/acc-issues-openapi.yml)
- [JSONSchema](json-schema/acc-issue-schema.json)
- [Example](examples/acc-issue-example.json)

### Autodesk Construction Cloud Cost Management API

The ACC Cost Management API provides access to budget codes, contract lifecycle management, and expense tracking in Autodesk Construction Cloud. REST APIs enable ERP integration, change order management, and financial reporting across construction project portfolios.

**Human URL:** [https://aps.autodesk.com/en/docs/acc/v1/overview/](https://aps.autodesk.com/en/docs/acc/v1/overview/)

#### Tags:

 - ACC, Budget, Construction, Contracts, Cost Management

#### Properties

- [Documentation](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [APIReference](https://aps.autodesk.com/en/docs/acc/v1/reference/http/cost-actions-POST/)
- [GettingStarted](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)

### Autodesk Construction Cloud Model Coordination API

The ACC Model Coordination API enables access to model sets, clash detection results, and coordination issues in Autodesk Construction Cloud. REST APIs support automated BIM coordination workflows, clash review automation, and model aggregation across design disciplines.

**Human URL:** [https://aps.autodesk.com/en/docs/acc/v1/overview/](https://aps.autodesk.com/en/docs/acc/v1/overview/)

#### Tags:

 - BIM, Clash Detection, Construction, IFC, Model Coordination

#### Properties

- [Documentation](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [APIReference](https://aps.autodesk.com/en/docs/acc/v1/reference/http/mc-modelset-service-v3-create-model-set-POST/)
- [GettingStarted](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)

### Autodesk Construction Cloud RFIs API

The ACC RFIs API enables management of Requests for Information (RFIs) in Autodesk Construction Cloud. REST APIs support RFI creation, tracking, response workflows, and reporting for construction project documentation and decision management.

**Human URL:** [https://aps.autodesk.com/en/docs/acc/v1/overview/](https://aps.autodesk.com/en/docs/acc/v1/overview/)

#### Tags:

 - ACC, Construction, Document Management, RFI

#### Properties

- [Documentation](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [APIReference](https://aps.autodesk.com/en/docs/acc/v1/reference/http/rfis-rfi-search-POST/)
- [GettingStarted](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)

### Autodesk Construction Cloud Submittals API

The ACC Submittals API provides programmatic access to submittal workflows in Autodesk Construction Cloud. REST APIs support submittal item creation, review routing, approval tracking, and specification section management for construction project compliance.

**Human URL:** [https://aps.autodesk.com/en/docs/acc/v1/overview/](https://aps.autodesk.com/en/docs/acc/v1/overview/)

#### Tags:

 - ACC, Construction, Document Management, Submittals

#### Properties

- [Documentation](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [APIReference](https://aps.autodesk.com/en/docs/acc/v1/reference/http/submittals-items-GET/)
- [GettingStarted](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)

### Autodesk Construction Cloud Data Connector API

The ACC Data Connector API enables bulk extraction of project data from Autodesk Construction Cloud for analytics and reporting. REST APIs support scheduled and on-demand data exports across issues, RFIs, submittals, assets, and other project modules for business intelligence integration.

**Human URL:** [https://aps.autodesk.com/en/docs/acc/v1/overview/](https://aps.autodesk.com/en/docs/acc/v1/overview/)

#### Tags:

 - ACC, Analytics, Construction, Data Export

#### Properties

- [Documentation](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [APIReference](https://aps.autodesk.com/en/docs/acc/v1/reference/http/data-connector-requests-POST/)
- [GettingStarted](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)

## Common Properties

- [Website](https://www.autodesk.com)
- [Portal](https://aps.autodesk.com/)
- [Documentation](https://aps.autodesk.com/developer/documentation)
- [GettingStarted](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)
- [Quickstart](https://get-started.aps.autodesk.com/)
- [TermsOfService](https://www.autodesk.com/company/legal-notices-trademarks/terms-of-service-autodesk360-web-services/forge-platform-web-services-api-terms-of-service)
- [PrivacyPolicy](https://www.autodesk.com/company/legal-notices-trademarks/privacy-statement)
- [StatusPage](https://health.autodesk.com/)
- [Support](https://aps.autodesk.com/contact-support)
- [ChangeLog](https://aps.autodesk.com/topics/platform-updates)
- [GitHubOrganization](https://github.com/autodesk-platform-services)

## Features

| Name | Description |
|------|-------------|
| Project Administration | Programmatic management of ACC accounts, projects, users, and company settings with automation of project provisioning and user access control. |
| Issues and Field Management | Creation, tracking, and management of construction issues, observations, punch lists, and quality control items through REST APIs. |
| Cost Management | Budget tracking, contract lifecycle management, change order processing, and financial reporting for construction project portfolios. |
| Model Coordination | Automated BIM coordination with clash detection, model set management, and coordination issue tracking across design disciplines. |
| RFI and Submittal Management | End-to-end management of Requests for Information and submittal review workflows with approval tracking and compliance reporting. |
| Data Connector | Bulk extraction of project data for analytics and business intelligence, supporting scheduled and on-demand exports across all ACC modules. |
| Webhooks | Event-driven notifications via webhooks for real-time integration with external systems when project data changes in ACC. |

## Use Cases

| Name | Description |
|------|-------------|
| ERP Integration | Connecting ACC cost management and project data with enterprise ERP systems for unified financial reporting and project accounting. |
| BIM Workflow Automation | Automating BIM coordination workflows including clash detection review, model set updates, and coordination issue resolution across teams. |
| Construction Project Reporting | Building custom dashboards and reports using the Data Connector API to aggregate project data across issues, RFIs, submittals, and costs. |
| Field Management Integration | Integrating ACC issues and punch list management with mobile field apps, IoT sensors, and safety management platforms. |
| Document Control Automation | Automating RFI and submittal routing, review reminders, and approval tracking to reduce administrative burden on project document control teams. |

## Integrations

| Name | Description |
|------|-------------|
| Autodesk Platform Services | Full integration with the Autodesk Platform Services (APS) ecosystem including Data Management, Model Derivative, and Authentication APIs. |
| Procore | Integration possibilities with Procore construction management platform for cross-platform project data synchronization. |
| Primavera P6 | Schedule data integration with Oracle Primavera P6 for project schedule management and reporting across enterprise construction portfolios. |
| SAP | Enterprise ERP integration with SAP for financial data synchronization, purchase order management, and project accounting workflows. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [ACC Admin OpenAPI](openapi/acc-admin-openapi.yml)
- [ACC Issues OpenAPI](openapi/acc-issues-openapi.yml)

### AsyncAPI

- [ACC Webhooks AsyncAPI](asyncapi/acc-webhooks-asyncapi.yml)

### JSON Schema

- [ACC Project Schema](json-schema/acc-project-schema.json)
- [ACC Issue Schema](json-schema/acc-issue-schema.json)

### JSON Structure

- [ACC Project Structure](json-structure/acc-project-structure.json)
- [ACC Issue Structure](json-structure/acc-issue-structure.json)

### JSON-LD

- [ACC Context](json-ld/acc-context.jsonld)

### Examples

- [ACC Project Example](examples/acc-project-example.json)
- [ACC Issue Example](examples/acc-issue-example.json)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
