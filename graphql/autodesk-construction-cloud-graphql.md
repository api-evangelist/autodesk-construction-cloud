# Autodesk Construction Cloud GraphQL Schema

This document describes a conceptual GraphQL schema for the Autodesk Construction Cloud (ACC) platform, derived from the Autodesk Platform Services (APS) REST APIs. It is intended to illustrate the domain model and relationships across ACC modules including Admin, Issues, RFIs, Submittals, Cost Management, Model Coordination, and Data Connector.

## Source APIs

The schema is derived from the following APS REST APIs:

- [ACC Admin API](https://aps.autodesk.com/en/docs/acc/v1/reference/http/admin-accounts-accountidprojects-GET/)
- [ACC Issues API](https://aps.autodesk.com/en/docs/acc/v1/reference/http/issues-issues-POST/)
- [ACC RFIs API](https://aps.autodesk.com/en/docs/acc/v1/reference/http/rfis-rfi-search-POST/)
- [ACC Submittals API](https://aps.autodesk.com/en/docs/acc/v1/reference/http/submittals-items-GET/)
- [ACC Model Coordination API](https://aps.autodesk.com/en/docs/acc/v1/reference/http/mc-modelset-service-v3-create-model-set-POST/)
- [ACC Data Connector API](https://aps.autodesk.com/en/docs/acc/v1/reference/http/data-connector-requests-POST/)
- [ACC Cost Management API](https://aps.autodesk.com/en/docs/acc/v1/reference/http/cost-actions-POST/)

## Schema File

The full GraphQL schema is defined in [`autodesk-construction-cloud-schema.graphql`](autodesk-construction-cloud-schema.graphql).

## Domain Overview

### Account and Project Hierarchy

The top-level domain object is an `Account` (hub) which contains multiple `Project` records. Projects have rich configuration via `ProjectDetails` including geolocation, job number, type, and phase. Project status is enumerated as `ProjectStatus` (ACTIVE, ARCHIVED, SUSPENDED, PENDING, INACTIVE).

### Document Management

Documents are organized through `Folder` objects containing `Item` records. Each item tracks versions via `ItemVersion`, linking to `File` and `Storage` objects for binary content management. Folders support hierarchical nesting with `FolderDetails` for permission model metadata.

### Issues

`Issue` is a core field management type capturing quality, safety, and punch-list items. Issues connect to `IssueType`, `IssueOwner`, `IssueLocation`, `IssueRootCause`, and `IssuePhoto` objects. Status transitions flow through `IssueStatus` (DRAFT through CLOSED/VOID). Issue scope is bounded by an `IssueContainer` at the project level.

### RFIs

`RFI` (Request for Information) tracks construction clarification requests through their lifecycle. The `RFIStatus` enum mirrors issue statuses for consistency. `RFIDetails` extends the core type with distribution lists, co-reviewers, and custom attributes.

### Submittals

`Submittal` manages the review and approval workflow for material and equipment submittals. `SubmittalDetails` captures reviewer routing, disposition, and specification section linkage.

### Meetings

`Meeting` records structured project meetings with agenda and action items via `MeetingItem`. `MeetingDetails` adds video conference URLs and timezone data.

### Checklists

`Checklist` supports quality control and safety inspection workflows, structured as `ChecklistSection` containers holding `ChecklistItem` questions. Items can be linked to Issues for follow-up tracking.

### Daily Logs

`DailyLog` captures daily field records including weather conditions. `LogEntry` records individual labor, equipment, and notes entries within a log, with optional company and location linkage.

### Assets

`Asset` tracks physical equipment and materials on a project. `AssetDetails` extends the type with maintenance scheduling and custom attribute support, linked to `Location` for spatial context.

### Locations

Two location types are provided. `Location` is a flat spatial reference with coordinates. `LocationNode` supports hierarchical Location Breakdown Structure (LBS) trees common in ACC field management.

### Model Coordination

`Model` represents a model set in ACC Model Coordination. `ModelVersion` captures coordination snapshots and links to `ModelViewable` derivatives for viewer integration via URN/GUID.

### Members and Companies

`Member` represents users with project or account access, connected to `MemberRole` (ACCOUNT_ADMIN through GUEST). `MemberDetails` extends with contact info and last sign-in tracking. `Company` is the organizational unit within an account, with `CompanyDetails` for trade and tax information.

### Webhooks

`Webhook` subscriptions enable event-driven integration. The `WebhookEvent` enum covers file versioning, folder changes, issues, RFIs, submittals, and checklists.

### Reports

`Report` represents Data Connector export requests with `ReportStatus` tracking (PENDING through FAILED). `ReportDetails` provides download URLs and output metadata.

### Forms

`Form` supports dynamic form submissions tied to templates. `FormDetails` captures field values as JSON and links to issues and locations.

### API Access

`APIKey` represents server-to-server credentials and `Token` represents OAuth 2.0 bearer tokens used for APS authentication.

### Properties

`Property` and `PropertyDetails` define custom attribute schemas applicable across ACC entities, with support for data types, allowed values, and read-only constraints.

### Partners

`Partner` and `PartnerDetails` represent third-party integration partners registered with the Autodesk Platform Services ecosystem.

## Type Summary

| Category | Types |
|---|---|
| Account | Account, AccountDetails |
| Project | Project, ProjectDetails, ProjectStatus, ProjectType |
| Documents | Folder, FolderDetails, Item, ItemDetails, ItemVersion, File, FileDetails, Storage, StorageDetails |
| Issues | Issue, IssueDetails, IssueType, IssueStatus, IssueOwner, IssueLocation, IssueRootCause, IssuePhoto, IssueContainer |
| RFIs | RFI, RFIDetails, RFIStatus |
| Submittals | Submittal, SubmittalDetails |
| Meetings | Meeting, MeetingDetails, MeetingItem |
| Checklists | Checklist, ChecklistDetails, ChecklistSection, ChecklistItem |
| Daily Logs | DailyLog, LogEntry |
| Assets | Asset, AssetDetails |
| Locations | Location, LocationNode |
| Models | Model, ModelVersion, ModelViewable |
| Properties | Property, PropertyDetails |
| Members | Member, MemberDetails, MemberRole |
| Companies | Company, CompanyDetails |
| Partners | Partner, PartnerDetails |
| Webhooks | Webhook, WebhookEvent |
| Reports | Report, ReportDetails |
| Forms | Form, FormDetails |
| Auth | APIKey, Token |

Total named types: 66

## Query Examples

### Fetch a Project with Issues

```graphql
query GetProjectIssues($projectId: ID!) {
  project(id: $projectId) {
    id
    name
    status
    issues(status: OPEN, limit: 25) {
      id
      title
      status
      dueDate
      issueType {
        title
      }
      owner {
        name
        email
      }
      location {
        locationName
      }
    }
  }
}
```

### List RFIs by Project

```graphql
query GetOpenRFIs($projectId: ID!) {
  rfis(projectId: $projectId, status: OPEN, limit: 50) {
    id
    title
    number
    status
    dueDate
    assignedTo
    costImpact
    costImpactAmount
  }
}
```

### Create an Issue

```graphql
mutation CreateIssue($projectId: ID!, $input: JSON!) {
  createIssue(projectId: $projectId, input: $input) {
    id
    title
    status
    createdAt
    issueType {
      title
    }
  }
}
```

### Register a Webhook

```graphql
mutation RegisterWebhook($scopeId: ID!, $callbackUrl: URL!) {
  createWebhook(
    scopeId: $scopeId
    event: ISSUE_CREATED
    callbackUrl: $callbackUrl
  ) {
    id
    event
    callbackUrl
    status
    createdAt
  }
}
```

### Request a Data Export Report

```graphql
mutation RequestExport($projectId: ID!) {
  requestReport(
    projectId: $projectId
    input: {
      type: "issues"
      exportedEntities: ["issues", "rfis", "submittals"]
    }
  ) {
    id
    status
    createdAt
  }
}
```

## Authentication

All queries and mutations require OAuth 2.0 authentication via Autodesk Platform Services. A `Token` is obtained using either three-legged (user context) or two-legged (server-to-server) flows. The bearer token is passed via the `Authorization` HTTP header.

```
Authorization: Bearer {access_token}
```

Scopes required vary by operation:

- `data:read` for Query operations
- `data:write` for Mutation operations creating or modifying project data
- `account:read` / `account:write` for Account and Admin operations

## References

- [APS Developer Portal](https://aps.autodesk.com/)
- [ACC API Overview](https://aps.autodesk.com/en/docs/acc/v1/overview/)
- [Getting Started with ACC APIs](https://aps.autodesk.com/en/docs/acc/v1/tutorials/getting-started)
- [APS Authentication](https://aps.autodesk.com/en/docs/oauth/v2/overview/)
