---
name: vonage-provision-number
description: Search for an available phone number, buy it, and attach it to a Vonage application so Voice and Messages
  webhooks route to you.
api: openapi/vonage-numbers-openapi.yml
operations:
- getAvailableNumbers
- buyANumber
- updateANumber
- cancelANumber
generated: '2026-10-08'
method: generated
source: openapi/vonage-numbers-openapi.yml ; every operationId checked against the contract
---

# vonage-provision-number

Search for an available phone number, buy it, and attach it to a Vonage application so Voice and Messages webhooks route to you.

## Steps

1. Use Basic auth (API key:secret) — the Numbers API is account-scoped.
2. Call `getAvailableNumbers` (GET /number/search) with `country` (ISO 3166-1 alpha-2) and optional `features` (SMS,VOICE,MMS) and `pattern`.
3. Call `buyANumber` (POST /number/buy) with `country` and `msisdn` from the search result; the response `error-code` is 200 on success.
4. Call `updateANumber` (POST /number/update) with `app_id` to link the number to your application, or set `moHttpUrl` / `voiceCallbackValue` directly.
5. To release the number later call `cancelANumber` (POST /number/cancel).

## Rules

- Numbers API is limited to 3 API requests per second (180 per minute); GET /account/numbers is 1 per second (rate-limits/).
- buyANumber charges the account; there is no dry-run. cancelANumber is the reversal, with no stated window (conventions/ reversibility).
- US long numbers need a registered 10DLC brand and campaign before sending SMS.
