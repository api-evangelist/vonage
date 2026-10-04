---
name: vonage-verify-user
description: Verify a user by requesting a verification and then checking the verification code.
api: openapi/vonage-verify-api-openapi.yml
operations:
- requestVerification
- checkVerification
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/vonage-verify-api-openapi.yml ; every operationId checked against the contract
---

# vonage-verify-user

Verify a user by requesting a verification and then checking the verification code.

## Steps

1. 1. Call `requestVerification` with the required request body fields (e.g., number, brand) and include an Authorization header (basicAuth or bearerAuth).
2. 2. Call `checkVerification` with the verification request ID and the user‑provided code, also including an Authorization header.

## Rules

- Authentication: Provide an Authorization header using either basicAuth or bearerAuth as defined by the API.
- No idempotency key is required for these operations.
- No pagination applies to these endpoints.
