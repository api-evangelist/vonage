# Vonage GraphQL Schema

## Overview

This document describes a conceptual GraphQL schema for the Vonage Communications API platform (part of Ericsson). Vonage provides cloud communications APIs spanning Voice, SMS, multi-channel Messaging, Video (WebRTC), Verify/2FA, Number management, and Account management. The schema unifies these REST/WebSocket/WebRTC APIs behind a single typed GraphQL interface.

## Provider

- **Name:** Vonage
- **Developer Portal:** https://developer.vonage.com/
- **GitHub:** https://github.com/Vonage
- **Base APIs:** Voice (api.nexmo.com/v1), SMS (rest.nexmo.com), Messages (api.nexmo.com/v1/messages), Verify (api.nexmo.com), Numbers (rest.nexmo.com), Application (api.nexmo.com/v2/applications), Video (api.opentok.com)

## Schema Source

Conceptual schema derived from:
- [Voice API Reference](https://developer.vonage.com/en/api/voice)
- [SMS API Reference](https://developer.vonage.com/en/api/sms)
- [Messages API Reference](https://developer.vonage.com/en/api/messages-olympus)
- [Verify API Reference](https://developer.vonage.com/en/api/verify)
- [Numbers API Reference](https://developer.vonage.com/en/api/numbers)
- [Application API Reference](https://developer.vonage.com/en/api/application.v2)
- [Video API Overview](https://developer.vonage.com/en/video/overview)
- [Conversations API Reference](https://developer.vonage.com/en/api/conversation)

## Types Summary

| Domain | Types |
|--------|-------|
| Voice / Calls | Call, CallDirection, CallStatus, CallRecord, Leg, LegStatus, DTMF, Recording, RecordingFormat, Transcription, SpeechRecognition, NCCOAction |
| Messaging | Message, MessageStatus, MessageChannel, SMSMessage, WhatsAppMessage, MessengerMessage, ViberMessage, MMSMessage, RCSMessage, InboundMessage |
| Verify / 2FA | Verify, VerifyRequest, VerifyStatus, VerifyCheck, TFA, OTP, OTPChannel |
| Applications | Application, Capability, VoiceCapability, MessagesCapability, RTCCapability, VideoCapability, WebhookEndpoint, ApplicationKey |
| Numbers | Number, NumberType, PhoneNumber, InboundNumber, OutboundNumber, NumberPorting, NumberFeature, Route |
| Insights | Insight, InsightSummary, InsightAdvanced, InsightRoaming, CarrierInfo, CallerIdentity, RoamingStatus |
| Video | MeetingSession, SessionParticipant, StreamUrl, ConnectionConfig, ArchiveRecord, BroadcastStream |
| Users | User, UserState, ConversationMember, MemberState |
| Account | Account, Balance, TopUp, UsageSummary, SubAccount, APISecret |

**Total named types: 58**

## Root Operations

### Query
- `call(id: ID!): Call` — Fetch a single call by ID
- `calls(status: CallStatus, pageSize: Int, recordIndex: Int): CallList` — List calls
- `callRecord(id: ID!): CallRecord` — Fetch a call recording record
- `message(id: ID!): Message` — Fetch a sent message
- `messages(channel: MessageChannel, status: MessageStatus, pageSize: Int): MessageList` — List messages
- `verifyRequest(requestId: ID!): VerifyRequest` — Get a verify request status
- `application(id: ID!): Application` — Get an application by ID
- `applications(pageSize: Int, page: Int): ApplicationList` — List all applications
- `number(msisdn: String!): PhoneNumber` — Get details for a phone number
- `numbers(country: String, pattern: String, searchPattern: Int): NumberList` — Search available numbers
- `ownedNumbers(country: String, applicationId: ID): OwnedNumberList` — List owned numbers
- `insight(number: String!, level: InsightLevel!): Insight` — Get number insight
- `meetingSession(sessionId: ID!): MeetingSession` — Get a video session
- `user(id: ID!): User` — Get a user by ID
- `account: Account` — Get account details and balance
- `subAccounts: SubAccountList` — List sub-accounts

### Mutation
- `createCall(input: CreateCallInput!): Call` — Initiate an outbound voice call
- `endCall(id: ID!): Call` — Terminate an active call
- `transferCall(id: ID!, destination: DestinationInput!): Call` — Transfer a call
- `sendDTMF(id: ID!, digits: String!): DTMFResult` — Send DTMF tones into a call
- `startRecording(callId: ID!, input: RecordingInput): Recording` — Start recording a call leg
- `stopRecording(recordingId: ID!): Recording` — Stop an in-progress recording
- `sendMessage(input: SendMessageInput!): Message` — Send a message on any channel
- `sendSMS(input: SendSMSInput!): SMSMessage` — Send an SMS message
- `requestVerify(input: VerifyInput!): VerifyRequest` — Initiate a verification workflow
- `checkVerify(requestId: ID!, code: String!): VerifyCheck` — Submit a verification code
- `cancelVerify(requestId: ID!): VerifyRequest` — Cancel a pending verification
- `createApplication(input: CreateApplicationInput!): Application` — Create a new Vonage application
- `updateApplication(id: ID!, input: UpdateApplicationInput!): Application` — Update an application
- `deleteApplication(id: ID!): Boolean` — Delete an application
- `searchNumbers(country: String!, type: NumberType, pattern: String): NumberList` — Search available numbers to buy
- `buyNumber(msisdn: String!, country: String!): PhoneNumber` — Purchase a phone number
- `cancelNumber(msisdn: String!, country: String!): Boolean` — Return/cancel a number
- `updateNumber(msisdn: String!, input: UpdateNumberInput!): PhoneNumber` — Update number configuration
- `createMeetingSession(input: CreateSessionInput!): MeetingSession` — Create a WebRTC video session
- `createUser(input: CreateUserInput!): User` — Create a conversation user
- `topUpBalance(input: TopUpInput!): TopUp` — Top up account balance
- `createAPISecret(apiKey: String!): APISecret` — Create a new API secret
- `deleteAPISecret(apiKey: String!, secretId: ID!): Boolean` — Delete an API secret

### Subscription
- `onCallEvent(callId: ID): Call` — Stream real-time call state changes
- `onMessageDelivery(messageId: ID): Message` — Stream delivery receipt events
- `onInboundMessage(number: String): InboundMessage` — Stream inbound messages to a number
- `onVerifyUpdate(requestId: ID!): VerifyRequest` — Stream verify request status changes
- `onSessionEvent(sessionId: ID!): MeetingSession` — Stream video session events

## Schema File

See [vonage-schema.graphql](vonage-schema.graphql) for the full type definitions.
