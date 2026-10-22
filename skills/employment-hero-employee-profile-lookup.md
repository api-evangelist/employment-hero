---
name: employment-hero-employee-profile-lookup
description: Find an Employment Hero employee in an organisation and assemble their profile, job history, bank accounts and emergency contacts.
api: Employment Hero REST API
generated: 2026-10-20
method: generated
operations:
  - listEmployees
  - getEmployee
  - getJobHistories
  - getEmployeeBankAccounts
  - listEmergencyContacts
---

# employment-hero-employee-profile-lookup

Find an Employment Hero employee in an organisation and assemble their profile, job history, bank accounts and emergency contacts.

## Conventions
- Base URL: https://api.employmenthero.com. Authenticate with an OAuth 2.0 bearer token (authorize at https://oauth.employmenthero.com/oauth2/authorize). The token is obtained by a person through the documented OAuth flow; an agent never calls the token endpoint on its own.
- Every path is scoped to `/organisations/{organisation_id}`.
- Docs index: https://developer.employmenthero.com/llms.txt

## Steps
1. Call `listEmployees` with the `organisation_id` and page through the results to find the employee you want.
2. Call `getEmployee` with that employee's `id` to get the full record.
3. Call `getJobHistories` and `listEmergencyContacts` with the `employee_id`.
4. Call `getEmployeeBankAccounts` only if the task needs it, because it returns sensitive financial data.
