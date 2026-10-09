---
name: vonage-send-message-with-failover
description: Send a message on WhatsApp or RCS through the Messages API, and fall back to SMS with the Dispatch
  API when it is not delivered.
api: openapi/vonage-messages-openapi.yml
operations:
- SendMessage
- UpdateMessage
generated: '2026-10-08'
method: generated
source: openapi/vonage-messages-openapi.yml ; every operationId checked against the contract
---

# vonage-send-message-with-failover

Send a message on WhatsApp or RCS through the Messages API, and fall back to SMS with the Dispatch API when it is not delivered.

## Steps

1. Mint an application JWT (recommended; Basic auth works but does not support webhooks or ACLs).
2. Call `SendMessage` (POST /v1/messages) with `channel`, `message_type`, `to`, `from`, and the channel payload; keep the returned `message_uuid`. Add `client_ref` to correlate status webhooks.
3. For channel failover, use the Dispatch API `createWorkflow` (openapi/vonage-dispatch-openapi.yml): a `workflow[]` of `from/to/channel` attempts with `failover[]` expiry and condition rules.
4. To revoke an outbound message on channels that support it, call `UpdateMessage` (PATCH /v1/messages/{message_uuid}) with `status: revoked`; to mark inbound messages read use `status: read`.

## Rules

- Try the channels first in the Messages API Sandbox (free, allow-listed recipients, 1 message/second, 100 messages/month) — sandbox/.
- Regional endpoints: https://{api-region}.nexmo.com/v1 with api, api-eu, api-us, api-ap.
- Message status errors use the Messages API numeric codes (1000 Throttled ...) in errors/vonage-error-codes.yml; HTTP errors are RFC 7807.
