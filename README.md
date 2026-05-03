# Vonage

Vonage (part of Ericsson) provides cloud communications APIs for voice, SMS, messaging, video, and verification. The Vonage API platform enables businesses to embed communication capabilities into applications including voice calls, SMS, multi-channel messaging (WhatsApp, Messenger, Viber, RCS), video conferencing, and two-factor authentication. SDKs are available for Node.js, Python, Java, PHP, Ruby, .NET, Go, and Kotlin.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

Communication, Messaging, Telecommunications, Voice, SMS, Verification, Video Conferencing

## Timestamps

- **Created:** 2025-02-08
- **Modified:** 2026-05-03

---

## APIs

| API | Description | Base URL |
|-----|-------------|----------|
| [Vonage SMS API](https://developer.vonage.com/en/api/sms) | Send and receive SMS messages globally | `https://rest.nexmo.com` |
| [Vonage Voice API](https://developer.vonage.com/en/api/voice) | Create and control voice calls | `https://api.nexmo.com/v1` |
| [Vonage Messages API](https://developer.vonage.com/en/api/messages-olympus) | Multi-channel messaging (SMS, WhatsApp, Messenger, Viber, MMS, RCS) | `https://api.nexmo.com/v1/messages` |
| [Vonage Verify API](https://developer.vonage.com/en/api/verify) | Two-factor authentication and phone verification | `https://api.nexmo.com` |
| [Vonage Numbers API](https://developer.vonage.com/en/api/numbers) | Provision and manage virtual phone numbers | `https://rest.nexmo.com` |
| [Vonage Application API](https://developer.vonage.com/en/api/application.v2) | Configure application settings and webhooks | `https://api.nexmo.com/v2/applications` |
| [Vonage Conversations API](https://developer.vonage.com/en/api/conversation) | Multi-channel conversation threading | `https://api.nexmo.com/v1` |
| [Vonage Reports API](https://developer.vonage.com/en/reports/overview) | Historical records and message lookup | `https://api.nexmo.com/v2/reports` |
| [Vonage Video API](https://developer.vonage.com/en/video/overview) | WebRTC video sessions and broadcasting | `https://api.opentok.com` |

---

## OpenAPI Specifications

- [vonage-openapi.yml](openapi/vonage-openapi.yml) — Vonage Communications API (SMS, Voice, Messages, Verify, Numbers, Applications)

---

## Spectral Rules

- [vonage-rules.yml](rules/vonage-rules.yml) — Spectral ruleset enforcing Vonage API conventions

---

## Naftiko Capabilities

### Shared Per-API Definitions

| File | API |
|------|-----|
| [shared/sms-api.yaml](capabilities/shared/sms-api.yaml) | Vonage SMS API |
| [shared/voice-api.yaml](capabilities/shared/voice-api.yaml) | Vonage Voice API |
| [shared/messages-api.yaml](capabilities/shared/messages-api.yaml) | Vonage Messages API |
| [shared/verify-api.yaml](capabilities/shared/verify-api.yaml) | Vonage Verify API |
| [shared/numbers-api.yaml](capabilities/shared/numbers-api.yaml) | Vonage Numbers API |

### Workflow Capabilities

| File | Description | APIs Combined |
|------|-------------|---------------|
| [messaging-and-notifications.yaml](capabilities/messaging-and-notifications.yaml) | Send notifications via SMS and multi-channel messaging | SMS API + Messages API |
| [voice-communications.yaml](capabilities/voice-communications.yaml) | Create and manage programmatic voice calls | Voice API |
| [user-authentication.yaml](capabilities/user-authentication.yaml) | Phone verification and number management for 2FA | Verify API + Numbers API |

---

## JSON Schema

- [vonage-message-schema.json](json-schema/vonage-message-schema.json) — Vonage Messages API message schema
- [vonage-call-schema.json](json-schema/vonage-call-schema.json) — Vonage Voice API call schema

---

## JSON Structure

- [vonage-message-structure.json](json-structure/vonage-message-structure.json) — Vonage Messages API message structure documentation

---

## JSON-LD

- [vonage-context.jsonld](json-ld/vonage-context.jsonld) — Vonage API linked data context

---

## Examples

- [vonage-sendSms-example.json](examples/vonage-sendSms-example.json) — Send an SMS message
- [vonage-createCall-example.json](examples/vonage-createCall-example.json) — Create an outbound voice call
- [vonage-requestVerification-example.json](examples/vonage-requestVerification-example.json) — Request a phone verification
- [vonage-sendMessage-example.json](examples/vonage-sendMessage-example.json) — Send a WhatsApp message

---

## Vocabulary

- [vonage-vocabulary.yml](vocabulary/vonage-vocabulary.yml) — Vonage communications domain vocabulary

---

## SDKs

- [Node.js SDK](https://github.com/Vonage/vonage-node-sdk)
- [Python SDK](https://github.com/Vonage/vonage-python-sdk)
- [Java SDK](https://github.com/Vonage/vonage-java-sdk)
- [PHP SDK](https://github.com/Vonage/vonage-php-sdk-core)
- [Ruby SDK](https://github.com/Vonage/vonage-ruby-sdk)
- [.NET SDK](https://github.com/Vonage/vonage-dotnet-sdk)
- [Go SDK](https://github.com/Vonage/vonage-go-sdk)
- [Kotlin SDK](https://github.com/Vonage/vonage-kotlin-sdk)
- [CLI](https://github.com/Vonage/vonage-cli)

---

## Maintainers

**FN:** Kin Lane  
**Email:** kin@apievangelist.com
