---
name: vonage-provision-number
description: Search for an available phone number, purchase it, and configure its settings.
api: openapi/vonage-numbers-api-openapi.yml
operations:
- searchAvailableNumbers
- buyNumber
- updateNumber
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/vonage-numbers-api-openapi.yml ; every operationId checked against the contract
---

# vonage-provision-number

Search for an available phone number, purchase it, and configure its settings.

## Steps

1. 1. Use `searchAvailableNumbers` with query parameters such as `country`, `type`, and `pattern` to find numbers.
2. 2. Use `buyNumber` with body fields `country`, `msisdn` (the number to purchase) and required authentication header.
3. 3. Use `updateNumber` with body fields like `country`, `msisdn`, and any configuration options (e.g., `voiceCallbackType`).

## Rules

- Authentication: Include either a `Authorization: Basic <credentials>` header for basicAuth or a `Authorization: Bearer <token>` header for bearerAuth.
