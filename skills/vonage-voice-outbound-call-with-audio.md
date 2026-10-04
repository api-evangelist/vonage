---
name: vonage-voice-outbound-call-with-audio
description: Create an outbound call and play an audio stream into it.
api: openapi/vonage-voice-api-openapi.yml
operations:
- createCall
- playAudioStream
- stopAudioStream
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/vonage-voice-api-openapi.yml ; every operationId checked against the contract
---

# vonage-voice-outbound-call-with-audio

Create an outbound call and play an audio stream into it.

## Steps

1. 1. `createCall` – include the `Authorization` header (basicAuth or bearerAuth) and the required request body fields for the outbound call.
2. 2. `playAudioStream` – include the `Authorization` header and the required request body fields to specify the audio stream URL.
3. 3. `stopAudioStream` – include the `Authorization` header to stop the audio stream.

## Rules

- Use an `Authorization` header with either Basic or Bearer token as defined by the auth schemes.
- No rate limit is specified; exhaustion returns no specific HTTP status.
