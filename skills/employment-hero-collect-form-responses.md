---
name: employment-hero-collect-form-responses
description: Read the forms in an Employment Hero organisation and the responses submitted to them.
api: Employment Hero REST API
generated: 2026-10-20
method: generated
operations:
  - listForms
  - getForm
  - listFormResponses
  - getFormResponse
---

# employment-hero-collect-form-responses

Read the forms in an Employment Hero organisation and the responses submitted to them.

## Conventions
- Base URL: https://api.employmenthero.com. Authenticate with an OAuth 2.0 bearer token (authorize at https://oauth.employmenthero.com/oauth2/authorize). The token is obtained by a person through the documented OAuth flow; an agent never calls the token endpoint on its own.
- Every path is scoped to `/organisations/{organisation_id}`.
- Docs index: https://developer.employmenthero.com/llms.txt

## Steps
1. Call `listForms` with the `organisation_id`.
2. Call `getForm` to read a form's structure.
3. Call `listFormResponses` and page through the results, then call `getFormResponse` for each response's detail.
