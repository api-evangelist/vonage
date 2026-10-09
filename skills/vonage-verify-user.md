---
name: vonage-verify-user
description: 'Verify a user''s phone number with Verify v2: start a verification, check the code the user enters,
  cancel inside the window if they abandon it.'
api: openapi/vonage-verify-v2-openapi.yml
operations:
- newRequest
- checkCode
- cancelRequest
generated: '2026-10-08'
method: generated
source: openapi/vonage-verify-v2-openapi.yml ; every operationId checked against the contract
---

# vonage-verify-user

Verify a user's phone number with Verify v2: start a verification, check the code the user enters, cancel inside the window if they abandon it.

## Steps

1. Mint an application JWT (RS256, exp <= 24h) or use Basic auth; both are declared on the Verify v2 contract.
2. Call `newRequest` (POST /v2/verify) with `brand` and a `workflow[]` of channels (sms, whatsapp, voice, email, silent_auth); keep the returned `request_id`.
3. When the user submits a code call `checkCode` (POST /v2/verify/{request_id}) with `code`; a 200 means verified, a 400 with `invalid_code` means retry.
4. If the user abandons, call `cancelRequest` (DELETE /v2/verify/{request_id}).

## Rules

- Cancellation is only possible 30 seconds after the start of the verification request and before the second event (either TTS or SMS) has taken place.
- Default throughput is 30 Verify API requests per second per account (rate-limits/).
- No idempotency key: do not retry `newRequest` blindly, re-use the `request_id` you already hold.
- Errors arrive as RFC 7807 application/problem+json (errors/).
