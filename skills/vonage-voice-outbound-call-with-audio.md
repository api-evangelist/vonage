---
name: vonage-voice-outbound-call-with-audio
description: Place an outbound call from an application, stream audio or speak text into it, and hang it up.
api: openapi/vonage-voice-openapi.yml
operations:
- createCall
- startStream
- stopStream
- startTalk
- stopTalk
- updateCall
generated: '2026-10-08'
method: generated
source: openapi/vonage-voice-openapi.yml ; every operationId checked against the contract
---

# vonage-voice-outbound-call-with-audio

Place an outbound call from an application, stream audio or speak text into it, and hang it up.

## Steps

1. Mint an application JWT for the application that owns the calling number (Bearer auth).
2. Call `createCall` (POST /v1/calls) with `to[]`, `from`, and either `ncco[]` inline or `answer_url`; keep the returned call `uuid`.
3. Call `startStream` (PUT /v1/calls/{uuid}/stream) with `stream_url[]` to play an audio file, or `startTalk` (PUT /v1/calls/{uuid}/talk) with `text` and `language` for TTS.
4. Call `stopStream` / `stopTalk` to interrupt, and `updateCall` (PUT /v1/calls/{uuid}) with `action: hangup` to end the call.

## Rules

- The maximum throughput is 3 calls per second (CPS), shared across all Voice products (rate-limits/).
- updateCall with action hangup is the reversal for createCall and works while the call is in progress (conventions/).
- Call events (answered, completed, ...) arrive on the application event webhook (asyncapi/vonage-webhooks.yml).
