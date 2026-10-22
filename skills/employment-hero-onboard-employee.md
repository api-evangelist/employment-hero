---
name: employment-hero-onboard-employee
description: Quick-add a new employee to an Employment Hero organisation and attach their onboarding documents.
api: Employment Hero REST API
generated: 2026-10-20
method: generated
operations:
  - quickAddEmployee
  - listEmployees
  - getEmployee
  - uploadEmployeeDocument
  - listEmployeeDocuments
---

# employment-hero-onboard-employee

Quick-add a new employee to an Employment Hero organisation and attach their onboarding documents.

## Conventions
- Base URL: https://api.employmenthero.com. Authenticate with an OAuth 2.0 bearer token (authorize at https://oauth.employmenthero.com/oauth2/authorize). The token is obtained by a person through the documented OAuth flow; an agent never calls the token endpoint on its own.
- Every path is scoped to `/organisations/{organisation_id}`.
- Docs index: https://developer.employmenthero.com/llms.txt

## Steps
1. Call `quickAddEmployee` with the `organisation_id` and the new hire's details. This is a write that is not idempotent: before retrying, call `listEmployees` and check the employee was not already created.
2. Call `getEmployee` to confirm the new record.
3. Call `uploadEmployeeDocument` to attach each onboarding document.
4. Call `listEmployeeDocuments` to verify the uploads.
