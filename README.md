# Vonage (vonage)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Vonage (part of Ericsson) provides cloud communications APIs for voice, SMS, messaging, video, and verification. The Vonage API platform enables businesses to embed communication capabilities into applications including voice calls, SMS, multi-channel messaging (WhatsApp, Messenger, Viber, RCS), video conferencing, and two-factor authentication. SDKs are available for Node.js, Python, Java, PHP, Ruby, .NET, Go, and Kotlin.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Communication
- Messaging
- Telecommunications
- Video Conferencing
- Voice
- SMS
- Verification

## Timestamps

- **Created:** 2025-02-08
- **Modified:** 2026-05-29

## APIs

### Vonage SMS API

Send and receive SMS messages globally using Vonage's SMS API. Supports text, binary, and unicode message types with delivery receipts and inbound message webhooks.

- **Human URL:** [https://developer.vonage.com/en/api/sms](https://developer.vonage.com/en/api/sms)
- **Base URL:** `https://rest.nexmo.com`

#### Tags

- Communication
- Messaging
- SMS
- Telecommunications

#### Properties

- [Documentation](https://developer.vonage.com/en/api/sms)
- [Base U R L](https://rest.nexmo.com)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vonage.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vonage.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Vonage Voice API

Create and control outbound and inbound voice calls using Vonage's Voice API. Supports PSTN, SIP, WebSocket, and VBC endpoints with NCCO (Vonage Call Control Object) for call flow management.

- **Human URL:** [https://developer.vonage.com/en/api/voice](https://developer.vonage.com/en/api/voice)
- **Base URL:** `https://api.nexmo.com/v1`

#### Tags

- Communication
- Telecommunications
- Voice
- VoIP

#### Properties

- [Documentation](https://developer.vonage.com/en/api/voice)
- [Base U R L](https://api.nexmo.com/v1)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [AsyncAPI](https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/asyncapi/vonage-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/vonage.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vonage.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Vonage Messages API

Multi-channel messaging API supporting SMS, WhatsApp, Facebook Messenger, Viber, MMS, and RCS. Send and receive messages across multiple channels with a unified API interface.

- **Human URL:** [https://developer.vonage.com/en/api/messages-olympus](https://developer.vonage.com/en/api/messages-olympus)
- **Base URL:** `https://api.nexmo.com/v1/messages`

#### Tags

- Communication
- Messaging
- Omnichannel
- WhatsApp
- RCS

#### Properties

- [Documentation](https://developer.vonage.com/en/api/messages-olympus)
- [Base U R L](https://api.nexmo.com/v1/messages)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vonage.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vonage.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Vonage Verify API

Two-factor authentication and phone verification API. Confirm user phone numbers via SMS, TTS, or WhatsApp verification codes to prevent fraud and authenticate users.

- **Human URL:** [https://developer.vonage.com/en/api/verify](https://developer.vonage.com/en/api/verify)
- **Base URL:** `https://api.nexmo.com`

#### Tags

- Authentication
- Communication
- Security
- Two-Factor Authentication
- Verification

#### Properties

- [Documentation](https://developer.vonage.com/en/api/verify)
- [Base U R L](https://api.nexmo.com)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vonage.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vonage.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Vonage Numbers API

Provision and manage virtual phone numbers globally. Search available numbers, purchase numbers for your account, and configure number behavior including inbound SMS and voice call routing.

- **Human URL:** [https://developer.vonage.com/en/api/numbers](https://developer.vonage.com/en/api/numbers)
- **Base URL:** `https://rest.nexmo.com`

#### Tags

- Communication
- Number Management
- Telecommunications
- Virtual Numbers

#### Properties

- [Documentation](https://developer.vonage.com/en/api/numbers)
- [Base U R L](https://rest.nexmo.com)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vonage.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vonage.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Vonage Application API

Configure Vonage application settings, webhook URLs, and authentication keys. Create and manage applications that group Vonage API capabilities including voice, messages, RTC, meetings, and video features.

- **Human URL:** [https://developer.vonage.com/en/api/application.v2](https://developer.vonage.com/en/api/application.v2)
- **Base URL:** `https://api.nexmo.com/v2/applications`

#### Tags

- API Management
- Communication
- Configuration
- Developer Tools

#### Properties

- [Documentation](https://developer.vonage.com/en/api/application.v2)
- [Base U R L](https://api.nexmo.com/v2/applications)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vonage.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vonage.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Vonage Conversations API

Build multi-channel conversation experiences with threading across SMS, voice, and messaging channels. Manage members, events, and legs within conversation contexts.

- **Human URL:** [https://developer.vonage.com/en/api/conversation](https://developer.vonage.com/en/api/conversation)
- **Base URL:** `https://api.nexmo.com/v1`

#### Tags

- Communication
- Conversations
- Messaging
- Real-Time

#### Properties

- [Documentation](https://developer.vonage.com/en/api/conversation)
- [Base U R L](https://api.nexmo.com/v1)
- [Postman Collection](collections/vonage.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vonage.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Vonage Reports API

Generate historical reports and lookup messages sent through your Vonage account. Access delivery receipts, call records, and usage data.

- **Human URL:** [https://developer.vonage.com/en/reports/overview](https://developer.vonage.com/en/reports/overview)
- **Base URL:** `https://api.nexmo.com/v2/reports`

#### Tags

- Analytics
- Communication
- Reporting

#### Properties

- [Documentation](https://developer.vonage.com/en/reports/overview)
- [Base U R L](https://api.nexmo.com/v2/reports)
- [Postman Collection](collections/vonage.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vonage.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Vonage Video API

Embed live, interactive video into web, mobile, and desktop applications using WebRTC. Supports sessions, tokens, broadcasting, recording, and SIP interconnect.

- **Human URL:** [https://developer.vonage.com/en/video/overview](https://developer.vonage.com/en/video/overview)
- **Base URL:** `https://api.opentok.com`

#### Tags

- Communication
- Telecommunications
- Video
- WebRTC

#### Properties

- [Documentation](https://developer.vonage.com/en/video/overview)
- [Portal](https://tokbox.com/developer/)
- [Base U R L](https://api.opentok.com)
- [Postman Collection](collections/vonage.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vonage.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/vonage)
- [Portal](https://developer.vonage.com/)
- [Documentation](https://developer.vonage.com/en/documentation)
- [Support](https://api.support.vonage.com/hc/en-us)
- [GitHub Organization](https://github.com/Vonage)
- [Portal](https://www.vonage.com/developer-center/)
- [Blog](https://developer.vonage.com/en/blog)
- [Community](https://vonage-community.slack.com/)
- [SDK](https://github.com/Vonage/vonage-node-sdk)
- [SDK](https://github.com/Vonage/vonage-python-sdk)
- [SDK](https://github.com/Vonage/vonage-java-sdk)
- [SDK](https://github.com/Vonage/vonage-php-sdk-core)
- [SDK](https://github.com/Vonage/vonage-ruby-sdk)
- [SDK](https://github.com/Vonage/vonage-dotnet-sdk)
- [SDK](https://github.com/Vonage/vonage-go-sdk)
- [SDK](https://github.com/Vonage/vonage-kotlin-sdk)
- [C L I](https://github.com/Vonage/vonage-cli)
- [Terms of Service](https://www.vonage.com/legal/)
- [Privacy Policy](https://www.vonage.com/legal/unified-communications/privacy-policy/)
- [Pricing](https://www.vonage.com/communications-apis/#pricing)
- [Features](undefined)
- [Integrations](https://developer.vonage.com/en/integrations)
- [M C P Server](https://github.com/Vonage/vonage-mcp-server-documentation)
- [L L Ms Txt](https://developer.vonage.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
