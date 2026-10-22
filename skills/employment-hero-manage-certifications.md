---
name: employment-hero-manage-certifications
description: Create, update, archive and delete certification types in an Employment Hero organisation.
api: Employment Hero REST API
generated: 2026-10-20
method: generated
operations:
  - listCertifications
  - createCertification
  - getCertification
  - updateCertification
  - certificationArchiveStatus
  - deleteCertification
  - uploadCertificationFile
  - certificationPollingStatus
---

# employment-hero-manage-certifications

Create, update, archive and delete certification types in an Employment Hero organisation.

## Conventions
- Base URL: https://api.employmenthero.com. Authenticate with an OAuth 2.0 bearer token (authorize at https://oauth.employmenthero.com/oauth2/authorize). The token is obtained by a person through the documented OAuth flow; an agent never calls the token endpoint on its own.
- Every path is scoped to `/organisations/{organisation_id}`.
- Docs index: https://developer.employmenthero.com/llms.txt

## Steps
1. Call `listCertifications` to see the certifications that already exist and avoid duplicates.
2. Call `createCertification` to add a new one, or `updateCertification` to change an existing one.
3. Call `uploadCertificationFile` to add supporting files, then call `certificationPollingStatus` to track the upload.
4. Prefer `certificationArchiveStatus` over `deleteCertification`. Delete is destructive and needs explicit confirmation from the user.
