<!--
╔══════════════════════════════════════════════════════════════════╗
║              API CONTRACT — MASTER TEMPLATE v1.0                 ║
║  Covers: REST · GraphQL · gRPC · WebSocket                       ║
║  Compliance: GDPR · HIPAA · SOC 2 / ISO 27001                    ║
║  Lifecycle: Dev → Staging → Production → First 500 Customers     ║
╚══════════════════════════════════════════════════════════════════╝
-->

# 📖 How to Use This Template

> **Read this section first — it takes 3 minutes and saves hours.**

This file is your API's single source of truth. Every person on your team —
developer, designer, tester, manager, or AI agent — should be able to open
this file and immediately understand *what* the API does, *how* to call it,
*what* it returns, and *who* is allowed to do what.

## Who fills what

| Role | Fills which sections |
|---|---|
| **Product / Project Manager** | 1 · 2 · 16 · 18 |
| **Backend Engineer** | 3 · 4 · 5 · 6 · 7 · 8 · 9 · 10 · 11 |
| **Security / DevOps** | 4 · 12 · 11 |
| **QA / Test Engineer** | 15 |
| **Claude AI Agent** *(auto-fills, human reviews)* | 5 · 6 · 7 · 8 · 9 · 10 · 17 |
| **Everyone** | 18 (sign-off) |

## Symbols used throughout

| Symbol | Meaning |
|---|---|
| `[FILL]` | You must replace this with real information |
| `[AI]` | Claude can auto-generate this; a human must verify |
| `[OPTIONAL]` | Only fill if it applies to your project |
| `⚠️` | Important warning — do not skip |
| `✅` | Checkbox — tick when done |
| `🔒` | Security-sensitive field |

## How to fill a `[FILL]` field

1. Find every `[FILL]` placeholder (search for the word FILL in your editor).
2. Replace it with real information about **your** API.
3. Delete placeholder text that does not apply.
4. When Claude auto-fills a section marked `[AI]`, always read it carefully before committing.

## Golden rule

> If someone new joins your team tomorrow and reads only this file,
> they should be able to make their first successful API call within 15 minutes.

---

# Section 1 — API Identity & Overview

> # HOW TO FILL: Section 1
> Think of this like the cover page of a book. Give your API a name, describe
> what problem it solves in plain English, and list the people responsible for it.
> A 10-year-old should be able to read the description and understand what this
> API does at a high level.

## 1.1 Basic Information

| Field | Value |
|---|---|
| **API Name** | `[FILL: e.g., "User Authentication API"]` |
| **API Short Code** | `[FILL: e.g., "AUTH-API"]` (used in error codes and logs) |
| **Product / System** | `[FILL: e.g., "MyApp Platform"]` |
| **Purpose** | `[FILL: One sentence — what problem does this API solve?]` |
| **API Owner** | `[FILL: Name + email of the person responsible]` |
| **Technical Lead** | `[FILL: Name + email]` |
| **Created Date** | `[FILL: YYYY-MM-DD]` |
| **Last Updated** | `[FILL: YYYY-MM-DD]` |
| **Status** | `[ ] Draft  [ ] In Review  [ ] Approved  [ ] Deprecated` |

## 1.2 Plain-English Description

> # HOW TO FILL: 1.2
> Write 3–5 sentences. Pretend you are explaining this to a friend who is not a
> developer. What does this API do? Who uses it? Why does it exist?

```
[FILL: e.g., "The User Authentication API lets mobile and web applications
securely log users in and out. It issues short-lived access tokens so that
every other API knows who is making a request. It also handles password
resets and multi-factor authentication (MFA)."]
```

## 1.3 Key Stakeholders

> # HOW TO FILL: 1.3
> List everyone who needs to know about this API. Include at least one person
> from engineering, product, and security.

| Name | Role | Contact | Notification Preference |
|---|---|---|---|
| `[FILL]` | `[FILL]` | `[FILL: email]` | `[FILL: email / Slack / PagerDuty]` |
| `[FILL]` | `[FILL]` | `[FILL: email]` | `[FILL]` |

## 1.4 Related Documents

> # HOW TO FILL: 1.4
> Link to other documents that relate to this API. If they don't exist yet,
> write "TBD" and create them later.

| Document | Link | Status |
|---|---|---|
| Product Requirements Doc (PRD) | `[FILL: URL or "TBD"]` | `[FILL]` |
| System Architecture Diagram | `[FILL: URL or "TBD"]` | `[FILL]` |
| Data Flow Diagram | `[FILL: URL or "TBD"]` | `[FILL]` |
| OpenAPI / Swagger Spec | `[FILL: URL or "TBD"]` | `[FILL]` |
| Runbook / On-Call Guide | `[FILL: URL or "TBD"]` | `[FILL]` |

---

# Section 2 — API Type & Protocol

> # HOW TO FILL: Section 2
> Check the boxes that apply to your API. Most projects use REST only.
> If you are building a real-time feature (like a chat), also check WebSocket.
> If you are not sure, ask your technical lead.

## 2.1 Protocol(s) Used

- [ ] **REST** (HTTP/HTTPS with JSON) — standard web API
- [ ] **GraphQL** — flexible queries from a single `/graphql` endpoint
- [ ] **gRPC** — high-performance, used between backend services
- [ ] **WebSocket** — real-time, two-way communication

## 2.2 Protocol-Specific Metadata

### REST

| Field | Value |
|---|---|
| Base URL (Production) | `[FILL: e.g., https://api.myapp.com/v1]` |
| Content Type | `application/json` (default) |
| HTTP Methods Used | `[FILL: GET, POST, PUT, PATCH, DELETE — list only what you use]` |

### GraphQL `[OPTIONAL]`

| Field | Value |
|---|---|
| Endpoint | `[FILL: e.g., https://api.myapp.com/graphql]` |
| Schema URL | `[FILL: URL to .graphql schema file]` |
| Transport | `[ ] HTTP POST  [ ] WebSocket subscriptions` |

### gRPC `[OPTIONAL]`

| Field | Value |
|---|---|
| Proto file location | `[FILL: e.g., /proto/service.proto]` |
| Service package | `[FILL: e.g., com.myapp.auth.v1]` |
| TLS required | `[ ] Yes  [ ] No` |

### WebSocket `[OPTIONAL]`

| Field | Value |
|---|---|
| WebSocket URL | `[FILL: e.g., wss://api.myapp.com/ws]` |
| Protocol / Subprotocol | `[FILL: e.g., "chat-v1"]` |
| Message Format | `[ ] JSON  [ ] MessagePack  [ ] Binary` |

---

# Section 3 — Environments

> # HOW TO FILL: Section 3
> Your API runs in different "environments." Think of them like practice courts
> before the real game:
> - **Local**: your laptop
> - **Dev**: shared development server
> - **Staging**: exact copy of production — used for final testing
> - **Canary**: a small slice of real users get the new version first
> - **Production**: the real thing — real users, real data
>
> Fill in the URL for each environment. If an environment doesn't exist yet,
> write "TBD."

## 3.1 Environment URLs

| Environment | Base URL | Status | Notes |
|---|---|---|---|
| **Local** | `http://localhost:[FILL: port]` | `[FILL: Active / TBD]` | Developer machine only |
| **Dev** | `[FILL: https://dev-api.myapp.com/v1]` | `[FILL]` | `[FILL]` |
| **Staging** | `[FILL: https://staging-api.myapp.com/v1]` | `[FILL]` | Mirror of production |
| **Canary** | `[FILL: https://canary-api.myapp.com/v1]` | `[FILL]` | `[FILL: % traffic]`% of traffic |
| **Production** | `[FILL: https://api.myapp.com/v1]` | `[FILL]` | Live customers |

## 3.2 Environment Variables Required

> # HOW TO FILL: 3.2
> List every environment variable (a setting stored outside the code) that the
> API needs to run. Do NOT put the actual secret values here — just the names
> and what they are for. Real values go in your secrets manager (e.g., AWS
> Secrets Manager, Vault, Doppler).

| Variable Name | Description | Required? | Example Value |
|---|---|---|---|
| `[FILL: e.g., DATABASE_URL]` | `[FILL: Connection string to the database]` | `Yes / No` | `postgresql://...` |
| `[FILL: e.g., JWT_SECRET]` | `[FILL: Secret used to sign tokens]` | `Yes` | `[NEVER store here 🔒]` |
| `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |

## 3.3 Infrastructure Summary

| Component | Technology | Managed By |
|---|---|---|
| Hosting | `[FILL: e.g., AWS ECS / GCP Cloud Run / Vercel]` | `[FILL: Team name]` |
| Database | `[FILL: e.g., PostgreSQL 15]` | `[FILL]` |
| Cache | `[FILL: e.g., Redis 7 / None]` | `[FILL]` |
| Message Queue | `[FILL: e.g., RabbitMQ / SQS / None]` | `[FILL]` |
| CDN | `[FILL: e.g., Cloudflare / None]` | `[FILL]` |
| API Gateway | `[FILL: e.g., AWS API Gateway / Kong / None]` | `[FILL]` |

---

# Section 4 — Authentication & Authorization

> # HOW TO FILL: Section 4
> This section describes **who** is allowed to use your API and **how** they
> prove who they are. Think of it like the lock on a door:
> - **Authentication** = proving who you are (showing your ID)
> - **Authorization** = what you are allowed to do (what rooms you can enter)
>
> ⚠️ This section is reviewed by the security team. Be precise.

## 4.1 Authentication Methods

Check all that apply and fill in the details:

### 4.1.1 API Key

- [ ] **Used**: Yes / No

| Field | Value |
|---|---|
| Header Name | `[FILL: e.g., X-API-Key]` |
| Format | `[FILL: e.g., 32-character alphanumeric string]` |
| Scope | `[FILL: Server-to-server only / Public clients allowed]` |
| Rotation Policy | `[FILL: e.g., Every 90 days, or on breach]` |
| Revocation Mechanism | `[FILL: e.g., Dashboard / Admin API endpoint]` |

**Example request header:**
```http
GET /v1/users HTTP/1.1
Host: api.myapp.com
X-API-Key: [FILL: example_key_format_only_not_real]
```

---

### 4.1.2 OAuth 2.0 / OIDC (JWT Bearer Token)

- [ ] **Used**: Yes / No

| Field | Value |
|---|---|
| Authorization Server | `[FILL: e.g., Auth0 / Keycloak / AWS Cognito / Custom]` |
| Authorization URL | `[FILL: URL]` |
| Token URL | `[FILL: URL]` |
| JWKS URI | `[FILL: URL to public key set]` |
| Supported Grant Types | `[FILL: authorization_code / client_credentials / refresh_token]` |
| Token Lifetime (Access) | `[FILL: e.g., 15 minutes]` |
| Token Lifetime (Refresh) | `[FILL: e.g., 30 days]` |
| Required Scopes | `[FILL: e.g., read:users write:users]` |

**Example request header:**
```http
GET /v1/users HTTP/1.1
Host: api.myapp.com
Authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9...
```

---

### 4.1.3 Mutual TLS (mTLS)

- [ ] **Used**: Yes / No

| Field | Value |
|---|---|
| Certificate Authority (CA) | `[FILL: Internal CA / Let's Encrypt / DigiCert]` |
| Client Cert Required | `[ ] Yes  [ ] No` |
| Certificate Rotation | `[FILL: e.g., Every 12 months]` |
| Used For | `[FILL: Service-to-service calls only]` |

---

## 4.2 Authorization — Roles & Permissions (RBAC / ABAC)

> # HOW TO FILL: 4.2
> List every role that can use this API and exactly what each role can do.
> Use the format: ✅ = allowed, ❌ = not allowed, 🔒 = requires extra approval.

### 4.2.1 Roles

| Role Name | Description | Who has it? |
|---|---|---|
| `[FILL: e.g., admin]` | `[FILL: Full access to all resources]` | `[FILL: Internal staff only]` |
| `[FILL: e.g., user]` | `[FILL: Read and write own data only]` | `[FILL: Registered customers]` |
| `[FILL: e.g., service]` | `[FILL: Machine-to-machine access]` | `[FILL: Internal microservices]` |
| `[FILL: e.g., readonly]` | `[FILL: Read-only, no writes]` | `[FILL: Reporting tools]` |

### 4.2.2 Permission Matrix

| Endpoint / Resource | admin | user | service | readonly |
|---|---|---|---|---|
| `[FILL: GET /users]` | ✅ | ✅ (own) | ✅ | ✅ |
| `[FILL: POST /users]` | ✅ | ✅ | ✅ | ❌ |
| `[FILL: DELETE /users/{id}]` | ✅ | ❌ | ❌ | ❌ |
| `[FILL: add rows as needed]` | | | | |

---

# Section 5 — REST Endpoint Definitions `[AI auto-fills, human reviews]`

> # HOW TO FILL: Section 5
> List every REST API endpoint. If you are using Claude to help, it can
> generate this section from your code or OpenAPI spec — just paste the spec
> or describe the endpoint and ask Claude: "Fill Section 5 of my API contract
> for this endpoint."
>
> Copy the endpoint block below as many times as you need — one block per endpoint.
> **Bold** = required field. Everything else is optional.

---

## Endpoint Template (copy & paste for each endpoint)

### `[FILL: HTTP METHOD]` `/[FILL: path/to/endpoint]`

> **What it does** (plain English): `[FILL: e.g., "Returns a list of all users.
> Only admins can call this. Results are paginated — 20 per page by default."]`

| Property | Value |
|---|---|
| **Method** | `[FILL: GET / POST / PUT / PATCH / DELETE]` |
| **Path** | `[FILL: /v1/users]` |
| **Auth Required** | `[ ] Yes  [ ] No` |
| **Roles Allowed** | `[FILL: admin, service]` |
| **Idempotent?** | `[ ] Yes (same call = same result)  [ ] No` |
| **Rate Limit** | `[FILL: e.g., 100 req/min per API key]` |
| **Response Caching** | `[FILL: e.g., Cache-Control: max-age=60 / None]` |

#### Path Parameters

| Parameter | Type | Required | Description | Example |
|---|---|---|---|---|
| `[FILL: id]` | `string / integer` | Yes / No | `[FILL: User's unique ID]` | `"usr_abc123"` |

#### Query Parameters

| Parameter | Type | Required | Default | Description | Example |
|---|---|---|---|---|---|
| `[FILL: page]` | `integer` | No | `1` | `[FILL: Page number]` | `?page=2` |
| `[FILL: limit]` | `integer` | No | `20` | `[FILL: Results per page]` | `?limit=50` |

#### Request Headers

| Header | Required | Description | Example |
|---|---|---|---|
| `Authorization` | Yes | Bearer JWT token | `Bearer eyJ...` |
| `[FILL: X-Request-ID]` | No | Idempotency key | `"req_abc123"` |

#### Request Body (for POST / PUT / PATCH)

```json
// [AI] — Claude generates this from your model definition.
// Human: verify all fields, types, and required markers are correct.
{
  "[FILL: field_name]": "[FILL: type and description — e.g., string, user's email]",
  "[FILL: field_name]": "[FILL]"
}
```

**Required fields**: `[FILL: list them]`

#### Success Response

| Status Code | Description |
|---|---|
| `[FILL: 200 OK / 201 Created / 204 No Content]` | `[FILL: When this is returned]` |

```json
// [AI] — Claude generates example response. Human: verify it matches production.
{
  "data": {
    "[FILL: field]": "[FILL: example value]"
  },
  "meta": {
    "page": 1,
    "limit": 20,
    "total": 142
  }
}
```

#### Error Responses

| Status Code | Error Type | When it happens |
|---|---|---|
| `400` | Bad Request | `[FILL: e.g., Missing required field]` |
| `401` | Unauthorized | `[FILL: e.g., Token missing or expired]` |
| `403` | Forbidden | `[FILL: e.g., Role not permitted]` |
| `404` | Not Found | `[FILL: e.g., User ID does not exist]` |
| `429` | Too Many Requests | `[FILL: e.g., Rate limit exceeded]` |
| `500` | Internal Server Error | `[FILL: e.g., Unhandled exception]` |

> ⚠️ See **Section 10** for the full RFC 7807 error response format.

#### Sequence Diagram

```mermaid
sequenceDiagram
    participant C as Client
    participant G as API Gateway
    participant S as [FILL: Service Name]
    participant D as Database

    C->>G: [FILL: HTTP METHOD /path] + Auth Header
    G->>G: Validate token
    G->>S: Forward request
    S->>D: [FILL: Query or write]
    D-->>S: [FILL: Response]
    S-->>G: [FILL: HTTP status + body]
    G-->>C: [FILL: HTTP status + body]
```

---

<!-- REPEAT THE BLOCK ABOVE FOR EACH ENDPOINT -->

---

# Section 6 — GraphQL Schema `[OPTIONAL] [AI auto-fills, human reviews]`

> # HOW TO FILL: Section 6
> Skip this section if you are not using GraphQL.
> If you are, paste your schema here or ask Claude:
> "Generate Section 6 of my API contract from this GraphQL schema: [paste schema]"

## 6.1 Queries

```graphql
# [AI] Paste or generate your Query definitions here
# Example:
type Query {
  # [FILL: describe what it returns]
  user(id: ID!): User
  users(page: Int, limit: Int): UserPage
}
```

## 6.2 Mutations

```graphql
# [AI] Paste or generate your Mutation definitions here
type Mutation {
  # [FILL]
  createUser(input: CreateUserInput!): User
  updateUser(id: ID!, input: UpdateUserInput!): User
  deleteUser(id: ID!): Boolean
}
```

## 6.3 Subscriptions `[OPTIONAL]`

```graphql
# [AI]
type Subscription {
  # [FILL: e.g., real-time notifications]
  onUserUpdated(id: ID!): User
}
```

## 6.4 Types

```graphql
# [AI]
type User {
  id: ID!
  email: String!
  name: String
  # [FILL: add all fields]
  createdAt: String!
  updatedAt: String!
}
```

## 6.5 GraphQL-Specific Rate Limits

| Limit Type | Value |
|---|---|
| Max query depth | `[FILL: e.g., 5 levels]` |
| Max query complexity | `[FILL: e.g., 100 points]` |
| Requests per minute | `[FILL: e.g., 60 RPM per API key]` |

---

# Section 7 — WebSocket Events `[OPTIONAL] [AI auto-fills, human reviews]`

> # HOW TO FILL: Section 7
> Skip this section if your API does not use WebSockets.
> WebSockets are used for real-time features like chat, live notifications,
> or live dashboards.

## 7.1 Connection

| Field | Value |
|---|---|
| WebSocket URL | `[FILL: wss://api.myapp.com/ws]` |
| Authentication | `[FILL: Token sent in first message / Query param ?token=JWT]` |
| Heartbeat / Ping interval | `[FILL: e.g., 30 seconds]` |
| Max idle timeout | `[FILL: e.g., 5 minutes]` |
| Reconnect strategy | `[FILL: e.g., Exponential backoff starting at 1s, max 60s]` |

## 7.2 Event Catalog

> # HOW TO FILL: 7.2
> List every event that can be sent or received. Direction: Client→Server or Server→Client.

| Event Name | Direction | Description | Payload Example |
|---|---|---|---|
| `[FILL: user.connected]` | Client → Server | `[FILL: Client announces it is online]` | `{ "userId": "usr_abc" }` |
| `[FILL: message.new]` | Server → Client | `[FILL: New message delivered]` | `{ "id": "msg_1", "text": "Hello" }` |
| `[FILL: ping]` | Both | `[FILL: Keep-alive heartbeat]` | `{}` |

## 7.3 Event Schema

```json
// Standard envelope for all WebSocket messages
{
  "event": "[FILL: event name]",
  "payload": {
    // [FILL: event-specific fields]
  },
  "timestamp": "ISO-8601 timestamp",
  "requestId": "UUID for tracing"
}
```

---

# Section 8 — gRPC Service Definitions `[OPTIONAL] [AI auto-fills, human reviews]`

> # HOW TO FILL: Section 8
> Skip this section if your API does not use gRPC.
> gRPC is used for fast, internal service-to-service communication.
> Ask Claude: "Generate Section 8 of my API contract from this proto file: [paste proto]"

## 8.1 Proto File Reference

| Field | Value |
|---|---|
| Proto file path | `[FILL: e.g., proto/auth/v1/auth.proto]` |
| Package | `[FILL: e.g., myapp.auth.v1]` |
| Go/Java/Python generated stubs location | `[FILL: path]` |

## 8.2 Services & RPCs

```protobuf
// [AI] — Paste or generate your proto service definition
syntax = "proto3";
package [FILL: myapp.auth.v1];

service [FILL: AuthService] {
  // [FILL: describe what each RPC does]
  rpc Login (LoginRequest) returns (LoginResponse);
  rpc Logout (LogoutRequest) returns (LogoutResponse);
  rpc RefreshToken (RefreshRequest) returns (RefreshResponse);
}

message LoginRequest {
  string email = 1;
  string password = 2; // [FILL: adjust fields]
}

message LoginResponse {
  string access_token = 1;
  string refresh_token = 2;
  int64 expires_at = 3;
}
```

## 8.3 gRPC Error Codes

| gRPC Status | HTTP Equivalent | When Used |
|---|---|---|
| `OK` | 200 | Success |
| `INVALID_ARGUMENT` | 400 | Bad input |
| `UNAUTHENTICATED` | 401 | Missing / invalid credentials |
| `PERMISSION_DENIED` | 403 | Role not allowed |
| `NOT_FOUND` | 404 | Resource doesn't exist |
| `RESOURCE_EXHAUSTED` | 429 | Rate limit hit |
| `INTERNAL` | 500 | Server error |
| `[FILL: add custom codes]` | `[FILL]` | `[FILL]` |

---

# Section 9 — Data Schemas `[AI auto-fills, human reviews]`

> # HOW TO FILL: Section 9
> A schema is a blueprint of the data. Think of it like a form with specific
> fields — each field has a name, a type (text, number, true/false), and rules.
>
> For each resource (like "User" or "Order"), describe all its fields.
> Claude can generate these from your database models or TypeScript types.

## 9.1 Core Data Models

### Model: `[FILL: Resource Name, e.g., User]`

| Field | Type | Required | Description | Constraints | PII? 🔒 |
|---|---|---|---|---|---|
| `id` | `string (UUID)` | Yes | Unique identifier | UUID v4 format | No |
| `[FILL: email]` | `string` | Yes | `[FILL: User's email]` | `[FILL: Valid email, max 255 chars]` | Yes 🔒 |
| `[FILL: name]` | `string` | No | `[FILL: Display name]` | `[FILL: Max 100 chars]` | Yes 🔒 |
| `[FILL: status]` | `enum` | Yes | `[FILL: Account status]` | `active / suspended / deleted` | No |
| `created_at` | `string (ISO-8601)` | Yes | Creation timestamp | UTC timezone | No |
| `updated_at` | `string (ISO-8601)` | Yes | Last update timestamp | UTC timezone | No |

> PII 🔒 = Personally Identifiable Information. Any field marked PII must follow
> the GDPR and HIPAA rules in Section 12.

---

<!-- Add a Model block for every resource your API uses -->

---

# Section 10 — Error Handling (RFC 7807 Problem Details)

> # HOW TO FILL: Section 10
> This section defines how your API reports errors — the same way, every time.
> All errors follow the RFC 7807 standard, which is like a universal language
> for API errors. You need to define your own error "types" below.
>
> [AI] Claude can generate this table from your exception handling code.

## 10.1 Standard Error Envelope

Every error response from this API uses this exact format:

```json
{
  "type": "https://api.myapp.com/errors/[error-slug]",
  "title": "Human-readable error title",
  "status": 400,
  "detail": "Longer explanation of exactly what went wrong",
  "instance": "/v1/users/usr_abc123",
  "request_id": "req_01J8XYZABC",
  "timestamp": "2026-10-14T10:00:00Z",
  "errors": [
    {
      "field": "email",
      "message": "Must be a valid email address"
    }
  ]
}
```

**Field definitions:**

| Field | Description | Always Present? |
|---|---|---|
| `type` | URL pointing to docs for this error type | Yes |
| `title` | Short, consistent title (same for the same error type) | Yes |
| `status` | HTTP status code as an integer | Yes |
| `detail` | What specifically went wrong in this request | Yes |
| `instance` | The URL path that caused the error | Yes |
| `request_id` | Unique ID for this request — use for support tickets | Yes |
| `timestamp` | When the error occurred (UTC) | Yes |
| `errors` | Array of field-level validation errors | Only for 422 |

## 10.2 Error Code Catalog `[AI auto-fills, human reviews]`

> # HOW TO FILL: 10.2
> List every error your API can return. Use the format:
> `[API_SHORT_CODE]-[CATEGORY]-[NUMBER]`
> Example: `AUTH-API-AUTH-001`

| Error Code | HTTP Status | Title | When It Happens | Resolution Hint |
|---|---|---|---|---|
| `[FILL]-AUTH-001` | `401` | Unauthorized | `[FILL: Token missing]` | `[FILL: Include a valid Bearer token]` |
| `[FILL]-AUTH-002` | `401` | Token Expired | `[FILL: Token older than 15 min]` | `[FILL: Use /token/refresh to get a new token]` |
| `[FILL]-AUTH-003` | `403` | Insufficient Permissions | `[FILL: Role cannot perform action]` | `[FILL: Contact admin to update your role]` |
| `[FILL]-VAL-001` | `422` | Validation Error | `[FILL: Required field missing]` | `[FILL: Check the errors[] array for details]` |
| `[FILL]-RATE-001` | `429` | Rate Limit Exceeded | `[FILL: Too many requests]` | `[FILL: Wait and retry after Retry-After header value]` |
| `[FILL]-SRV-001` | `500` | Internal Server Error | `[FILL: Unhandled exception]` | `[FILL: Contact support with request_id]` |
| `[FILL: add rows]` | | | | |

## 10.3 Retry Policy

| Error Type | Retry? | Strategy |
|---|---|---|
| `401 / 403` | No | Fix credentials first |
| `429 Too Many Requests` | Yes | Wait for `Retry-After` header, then retry |
| `500 / 502 / 503` | Yes | Exponential backoff: 1s, 2s, 4s, 8s — max 3 attempts |
| `400 / 422` | No | Fix the request payload |

---

# Section 11 — Rate Limits & SLA

> # HOW TO FILL: Section 11
> Rate limits protect the API from being overwhelmed.
> SLA = Service Level Agreement — the promises you make about uptime and speed.
> Fill these in with real numbers from your infrastructure planning.

## 11.1 Rate Limits

### Global Limits

| Scope | Limit | Window | Enforcement |
|---|---|---|---|
| Per API Key | `[FILL: e.g., 1,000]` req | Per minute | HTTP 429 |
| Per User (JWT) | `[FILL: e.g., 200]` req | Per minute | HTTP 429 |
| Per IP (unauthenticated) | `[FILL: e.g., 30]` req | Per minute | HTTP 429 |

### Per-Endpoint Limits

| Endpoint | Limit | Window | Notes |
|---|---|---|---|
| `[FILL: POST /auth/login]` | `[FILL: 10]` req | Per minute per IP | Brute-force protection |
| `[FILL: GET /users]` | `[FILL: 100]` req | Per minute | Admin only |
| `[FILL: add rows]` | | | |

### Rate Limit Response Headers

Every response includes these headers:

```http
X-RateLimit-Limit: 1000
X-RateLimit-Remaining: 847
X-RateLimit-Reset: 1728902400
Retry-After: 12
```

## 11.2 Uptime SLA

| Environment | Uptime Target | Measurement Window | Exclusions |
|---|---|---|---|
| Production | `[FILL: e.g., 99.9%]` | Monthly | Scheduled maintenance |
| Staging | `[FILL: e.g., 95%]` | Monthly | Deployments |

> **What 99.9% uptime means**: Your API can be down for at most ~43 minutes per month.

### Planned Maintenance

| Field | Policy |
|---|---|
| Maintenance window | `[FILL: e.g., Sundays 02:00–04:00 UTC]` |
| Advance notice | `[FILL: e.g., 48 hours via status page]` |
| Status page | `[FILL: URL, e.g., status.myapp.com]` |

## 11.3 Latency SLO (Response Time Targets)

> SLO = Service Level Objective — internal performance goals.
> p50 = 50% of requests must be faster than this.
> p95 = 95% of requests must be faster than this.
> p99 = 99% of requests must be faster than this.

| Endpoint Group | p50 | p95 | p99 |
|---|---|---|---|
| Read endpoints (GET) | `[FILL: e.g., 80ms]` | `[FILL: 200ms]` | `[FILL: 500ms]` |
| Write endpoints (POST/PUT) | `[FILL: 150ms]` | `[FILL: 400ms]` | `[FILL: 800ms]` |
| Heavy/search endpoints | `[FILL: 300ms]` | `[FILL: 800ms]` | `[FILL: 2000ms]` |

## 11.4 Data Retention & Purge Policy

> # HOW TO FILL: 11.4
> How long does your API keep data? When is it deleted?
> This is required for GDPR and HIPAA compliance.

| Data Type | Retention Period | Deletion Method | Who Can Request Deletion |
|---|---|---|---|
| `[FILL: User accounts]` | `[FILL: Until user deletes / 3 years after inactivity]` | `[FILL: Hard delete / Anonymization]` | User, Admin, Legal request |
| `[FILL: API logs]` | `[FILL: e.g., 90 days]` | `[FILL: Automated purge]` | Ops team only |
| `[FILL: Audit logs]` | `[FILL: e.g., 7 years]` | `[FILL: Manual, legal approval required]` | Legal team only |
| `[FILL: PII fields]` | `[FILL: As per GDPR request]` | `[FILL: Anonymization within 30 days]` | User |

---

# Section 12 — Compliance & Data Privacy

> # HOW TO FILL: Section 12
> This section ensures your API follows the law. If you collect, store, or
> process any personal information about people (names, emails, health data,
> financial data), you must complete this section.
> ⚠️ Have your legal or compliance team review this section before launch.

## 12.1 Data Classification

| Data Category | Description | Examples | Classification Level |
|---|---|---|---|
| Public | No restriction | API documentation, status pages | Public |
| Internal | Internal use only | Usage metrics, internal IDs | Internal |
| Confidential | Business sensitive | Business logic, algorithms | Confidential |
| PII | Personal data | Name, email, phone, IP address | Restricted 🔒 |
| PHI | Health data (HIPAA) | Diagnoses, prescriptions, health records | Restricted 🔒 |
| Financial | Payment data | Card numbers, bank accounts | Restricted 🔒 |

## 12.2 GDPR Compliance Checklist

> Tick each item when implemented and verified.

- [ ] **Lawful basis for processing**: `[FILL: e.g., Consent / Legitimate interest / Contract]`
- [ ] **Privacy notice**: Users are informed at `[FILL: URL to privacy policy]`
- [ ] **Right to access**: Endpoint to export user data: `[FILL: e.g., GET /v1/me/export]`
- [ ] **Right to erasure**: Endpoint to delete user: `[FILL: e.g., DELETE /v1/me]`
- [ ] **Data portability**: Export format: `[FILL: JSON / CSV]`
- [ ] **Data minimization**: Only collecting fields listed in Section 9
- [ ] **Breach notification**: Procedure documented at `[FILL: internal link]`
- [ ] **Data Processing Agreement (DPA)**: Signed with `[FILL: list third-party processors]`
- [ ] **Cross-border transfers**: `[FILL: Data stays in EU / Standard Contractual Clauses used]`

## 12.3 HIPAA Compliance Checklist `[OPTIONAL — only if handling health data]`

- [ ] **BAA (Business Associate Agreement)**: Signed with `[FILL: covered entity name]`
- [ ] **PHI fields identified**: Listed in Section 9 with 🔒 marker
- [ ] **Encryption at rest**: `[FILL: AES-256 / Database-level encryption]`
- [ ] **Encryption in transit**: TLS 1.2 minimum (TLS 1.3 preferred)
- [ ] **Access logs for PHI**: Audit log retained for `[FILL: 6 years]`
- [ ] **Minimum necessary rule**: Endpoints expose only required PHI fields
- [ ] **Emergency access procedure**: `[FILL: documented at internal link]`

## 12.4 SOC 2 / ISO 27001 Controls

| Control Area | Implementation | Evidence Location |
|---|---|---|
| Access Control | `[FILL: e.g., RBAC as defined in Section 4]` | `[FILL: Link to access control policy]` |
| Audit Logging | `[FILL: e.g., All API calls logged to CloudWatch]` | `[FILL: Log location]` |
| Encryption | `[FILL: TLS 1.3 in transit, AES-256 at rest]` | `[FILL: Infra docs]` |
| Vulnerability Management | `[FILL: e.g., Weekly automated scans via Snyk]` | `[FILL: Scan reports]` |
| Incident Response | `[FILL: Runbook at URL]` | `[FILL: Link]` |
| Change Management | `[FILL: PR review required + staging deploy first]` | `[FILL: Link to process]` |

---

# Section 13 — Versioning & Deprecation Lifecycle

> # HOW TO FILL: Section 13
> APIs change over time. This section tracks which versions exist, what changed
> between them, and when old versions will stop working (be "sunset").
>
> A "breaking change" is any change that would cause an existing caller's code
> to stop working. Examples: removing a field, renaming a field, changing a
> field's type.

## 13.1 Versioning Strategy

| Field | Value |
|---|---|
| Versioning method | `[FILL: URL path (/v1/) / Header (Api-Version: 1) / Query param (?version=1)]` |
| Current stable version | `[FILL: e.g., v1]` |
| Pre-release version | `[FILL: e.g., v2-beta / None]` |
| Version support policy | `[FILL: e.g., "We support the last 2 major versions"]` |

## 13.2 Version Registry

| Version | Status | Release Date | Sunset Date | Migration Guide |
|---|---|---|---|---|
| `v1` | ✅ Stable | `[FILL: YYYY-MM-DD]` | `[FILL: YYYY-MM-DD or N/A]` | N/A |
| `v2` | 🔶 Beta | `[FILL]` | `[FILL]` | `[FILL: URL]` |
| `v0` | 🔴 Sunset | `[FILL]` | `[FILL]` | `[FILL: URL]` |

**Status legend**: ✅ Stable · 🔶 Beta · 🔵 Alpha · 🔴 Sunset · ⚫ Retired

## 13.3 Breaking Change Policy

> A breaking change requires:

1. **Minimum notice**: `[FILL: e.g., 90 days before sunset]`
2. **Notification channels**: `[FILL: e.g., Email to registered developers + status page + API header warning]`
3. **Deprecation header** added to affected responses immediately:

```http
Deprecation: true
Sunset: Sat, 01 Jan 2028 00:00:00 GMT
Link: <https://api.myapp.com/v2/docs>; rel="successor-version"
```

## 13.4 Breaking vs Non-Breaking Changes

| Change Type | Examples | Breaking? |
|---|---|---|
| **Non-breaking** | Adding a new optional field to response | ❌ No |
| **Non-breaking** | Adding a new optional query parameter | ❌ No |
| **Non-breaking** | Adding a new endpoint | ❌ No |
| **Breaking** | Removing a field from response | ✅ Yes |
| **Breaking** | Changing a field's type | ✅ Yes |
| **Breaking** | Renaming a field | ✅ Yes |
| **Breaking** | Changing HTTP status codes | ✅ Yes |
| **Breaking** | Making an optional field required | ✅ Yes |

## 13.5 Deprecation Announcement Template

> When deprecating, send this notice:

```
SUBJECT: [DEPRECATION NOTICE] [API Name] [Version] — Sunset on [DATE]

We are deprecating [API Name] [Version] effective [DATE].

Why: [FILL: reason — e.g., "Replaced by v2 with improved performance"]
What to do: [FILL: migration steps]
Migration guide: [URL]
Last supported date: [DATE]
Support contact: [email]
```

---

# Section 14 — AI Agent Workflow Integration

> # HOW TO FILL: Section 14
> This section explains how Claude and other AI tools interact with this API
> during development. It defines what Claude is allowed to auto-generate and
> what always requires a human to review.
>
> Think of this as the "rules of engagement" for AI in your dev pipeline.

## 14.1 AI Roles in This Project

| Task | AI Role | Human Role |
|---|---|---|
| Generate endpoint definitions | Claude drafts | Engineer reviews & approves |
| Generate request/response schemas | Claude drafts from DB models | Engineer verifies types & constraints |
| Generate error code table | Claude extracts from codebase | QA validates completeness |
| Generate changelog entries | Claude reads git diff | PM approves before merging |
| Security review | ❌ Not AI | Security engineer only |
| Sign-off approval | ❌ Not AI | Required humans listed in Section 18 |

## 14.2 Claude Prompt Templates

> # HOW TO FILL: 14.2
> Save these prompts. When you start a new project, run them in Claude to
> auto-fill the marked `[AI]` sections of this contract.

### Prompt: Generate Endpoint Definitions (Section 5)

```
You are filling Section 5 of my API Contract template (API_Contract.md).
API Style: [REST / GraphQL / gRPC / WebSocket]
Here is my [OpenAPI spec / router file / controller code]:

[PASTE CODE HERE]

For each endpoint, generate a complete Section 5 block including:
- HTTP method, path, description
- Auth requirements and roles
- Path, query, and header parameters
- Request body schema (JSON)
- Success response example (JSON)
- Error response table
Output in Markdown. Mark any field you are uncertain about with [NEEDS REVIEW].
```

### Prompt: Generate Data Schemas (Section 9)

```
You are filling Section 9 of my API Contract (Data Schemas).
Here are my database models / TypeScript interfaces:

[PASTE MODELS HERE]

For each model, generate a Section 9 table with:
- Field name, type, required, description, constraints
- Mark any field that contains PII (name, email, phone, health data, location) with 🔒
Output in Markdown table format.
```

### Prompt: Generate Changelog Entry (Section 17)

```
You are generating a changelog entry for Section 17 of my API Contract.
Here is the git diff / PR description for this change:

[PASTE DIFF OR PR DESCRIPTION]

Generate a changelog entry with:
- Version number, date, type (breaking / feature / fix / security)
- What changed, why, and migration steps if breaking
Keep it beginner-friendly — someone non-technical should understand it.
```

## 14.3 AI Quality Gates

> Before merging any AI-generated content into this contract, a human must
> verify the following:

- [ ] All `[NEEDS REVIEW]` markers are resolved
- [ ] No real secret values or credentials were included
- [ ] PII fields are correctly marked 🔒
- [ ] Error codes follow the format in Section 10.2
- [ ] Rate limits are confirmed with infrastructure team
- [ ] Security team has reviewed authentication flows

---

# Section 15 — Testing Requirements

> # HOW TO FILL: Section 15
> This section defines what must be tested before the API is deployed.
> A QA engineer fills this section, but developers write the tests.

## 15.1 Test Coverage Requirements

| Test Type | Minimum Coverage | Tool Used | Location |
|---|---|---|---|
| Unit tests | `[FILL: e.g., 80%]` | `[FILL: Jest / PyTest / Go test]` | `[FILL: /tests/unit]` |
| Integration tests | `[FILL: All endpoints]` | `[FILL: Supertest / Postman / Newman]` | `[FILL: /tests/integration]` |
| Contract tests | `[FILL: All schemas]` | `[FILL: Pact / Dredd]` | `[FILL: /tests/contract]` |
| Load tests | `[FILL: 2x expected peak]` | `[FILL: k6 / Locust]` | `[FILL: /tests/load]` |
| Security tests | `[FILL: OWASP Top 10]` | `[FILL: OWASP ZAP / Snyk]` | `[FILL: /tests/security]` |

## 15.2 Mandatory Pre-Launch Test Cases

> Each item below must pass before the API moves to production.

- [ ] `AUTH-TC-001`: Invalid token returns 401 with RFC 7807 body
- [ ] `AUTH-TC-002`: Expired token returns 401 with correct error code
- [ ] `AUTH-TC-003`: Wrong role returns 403
- [ ] `RATE-TC-001`: Exceeding rate limit returns 429 with `Retry-After` header
- [ ] `VAL-TC-001`: Missing required field returns 422 with `errors[]` array
- [ ] `SLA-TC-001`: p95 latency under load is within SLO defined in Section 11.3
- [ ] `SEC-TC-001`: SQL injection attempts return 400, not 500
- [ ] `SEC-TC-002`: XSS payloads in string fields are sanitized
- [ ] `SEC-TC-003`: HTTPS enforced — HTTP redirects to HTTPS
- [ ] `GDPR-TC-001`: `DELETE /me` removes all PII fields within `[FILL: X hours]`
- [ ] `[FILL: Add project-specific test cases]`

## 15.3 Performance Baselines

| Metric | Baseline (before optimization) | Target (after optimization) |
|---|---|---|
| Avg response time | `[FILL: measured value]` | `[FILL: target value]` |
| Requests/second (peak) | `[FILL]` | `[FILL]` |
| Error rate under load | `[FILL]` | `< 0.1%` |
| Memory usage (container) | `[FILL]` | `[FILL]` |

---

# Section 16 — Customer Rollout Milestones (0 → 500 Customers)

> # HOW TO FILL: Section 16
> This section tracks whether the API is ready for real customers.
> Think of it like a checklist before a rocket launch — every box must be ticked
> before you let the next group of customers in.
>
> Each milestone is a "gate." You cannot pass through a gate until all items
> in the previous gate are complete.

## 🚀 Gate 0: Internal Alpha (0 → 10 customers = Internal team only)

> Goal: Prove the API works end-to-end in a real environment.

**API Readiness:**
- [ ] All endpoints in Section 5 are deployed to staging
- [ ] Authentication flow tested by a human (not just unit tests)
- [ ] At least 1 full happy-path integration test passing per endpoint
- [ ] Error responses match RFC 7807 format in Section 10

**Infrastructure:**
- [ ] Staging environment is live and stable
- [ ] Basic monitoring and alerting is configured
- [ ] Logs are being captured and searchable

**Documentation:**
- [ ] This API Contract is approved (Section 18 signed)
- [ ] A "Getting Started" guide exists with a working curl example

**Compliance:**
- [ ] GDPR right-to-delete endpoint tested
- [ ] No real PII used in test data

**Gate 0 Sign-off Date**: `[FILL: YYYY-MM-DD]`  
**Signed by**: `[FILL: Name, Role]`

---

## 🚀 Gate 1: Private Beta (10 → 100 customers)

> Goal: Validate with a small, trusted group of external users.

**API Readiness:**
- [ ] All Section 15.2 mandatory test cases passed
- [ ] Rate limiting active and tested (Section 11.1)
- [ ] Versioning headers in place (Section 13)
- [ ] All environment URLs in Section 3 are correct and documented

**Performance:**
- [ ] Load test run at 2x expected Beta traffic
- [ ] p95 latency within SLO (Section 11.3)
- [ ] Auto-scaling configured and tested

**Security:**
- [ ] OWASP Top 10 security scan completed
- [ ] No critical or high severity vulnerabilities open
- [ ] mTLS or API key rotation policy communicated to beta users
- [ ] Penetration test: `[FILL: Scheduled / Completed on YYYY-MM-DD]`

**Compliance:**
- [ ] GDPR / HIPAA checklist (Section 12) fully ticked
- [ ] DPA signed with all third-party data processors
- [ ] Privacy policy updated and linked from API docs

**Monitoring & Incident Response:**
- [ ] Uptime monitoring active with alert to on-call team
- [ ] Incident runbook written and tested
- [ ] Status page live at `[FILL: URL]`

**Gate 1 Sign-off Date**: `[FILL: YYYY-MM-DD]`  
**Signed by**: `[FILL: Name, Role]`

---

## 🚀 Gate 2: Public Launch (100 → 500 customers)

> Goal: Open to all customers. This is production launch.

**API Readiness:**
- [ ] All Gate 0 and Gate 1 items complete
- [ ] Production environment deployed with zero downtime
- [ ] Canary deployment validated (Section 3)
- [ ] All breaking change notifications sent (Section 13.3)
- [ ] API changelog published (Section 17)

**Performance:**
- [ ] Load tested at 5x expected launch traffic
- [ ] Database query performance reviewed (no N+1 queries)
- [ ] CDN caching configured for cacheable endpoints
- [ ] Circuit breaker / fallback strategy for downstream dependencies

**Security:**
- [ ] Production secrets rotated from staging values 🔒
- [ ] WAF (Web Application Firewall) rules active
- [ ] DDoS protection enabled
- [ ] All API keys and OAuth credentials are production-grade

**Compliance:**
- [ ] Legal has approved the API's data handling
- [ ] HIPAA BAA in place with all applicable partners `[OPTIONAL]`
- [ ] SOC 2 audit scope updated to include this API `[OPTIONAL]`

**Business Readiness:**
- [ ] Support team briefed on common error codes (Section 10.2)
- [ ] API documentation is public at `[FILL: URL]`
- [ ] SLA communicated to customers (Section 11.2)
- [ ] Billing / metering for API usage is live `[OPTIONAL]`

**Post-Launch Monitoring (first 30 days):**
- [ ] Daily error rate reviewed by engineering lead
- [ ] Weekly performance report generated
- [ ] Customer feedback channel established
- [ ] Capacity planning review scheduled for `[FILL: date]`

**Gate 2 Sign-off Date**: `[FILL: YYYY-MM-DD]`  
**Signed by**: `[FILL: Name, Role]`

---

## 📊 Customer Milestone Tracker

| Milestone | Target Date | Actual Date | Status |
|---|---|---|---|
| First internal user | `[FILL]` | `[FILL]` | `[ ] Reached` |
| 10 customers (end of Gate 0) | `[FILL]` | `[FILL]` | `[ ] Reached` |
| 50 customers | `[FILL]` | `[FILL]` | `[ ] Reached` |
| 100 customers (end of Gate 1) | `[FILL]` | `[FILL]` | `[ ] Reached` |
| 250 customers | `[FILL]` | `[FILL]` | `[ ] Reached` |
| 500 customers (Gate 2 complete) | `[FILL]` | `[FILL]` | `[ ] Reached` |

---

# Section 17 — Changelog `[AI auto-fills, human reviews]`

> # HOW TO FILL: Section 17
> Record every change to this API here. Newest changes go at the top.
> Use the Claude prompt in Section 14.2 to auto-generate entries from git diffs.
> A human must read and approve each entry before it is merged.
>
> **Change types**: 🔴 Breaking · 🟡 Feature · 🟢 Fix · 🔒 Security · 📄 Docs

---

## [Unreleased]

| # | Type | Change | Author | Date |
|---|---|---|---|---|
| `[FILL]` | `[FILL]` | `[FILL: What changed and why]` | `[FILL]` | `[FILL]` |

---

## v1.0.0 — Initial Release

| # | Type | Change | Author | Date |
|---|---|---|---|---|
| 1 | 🟡 Feature | Initial API release with endpoints listed in Section 5 | `[FILL]` | `[FILL: YYYY-MM-DD]` |

---

<!-- Add a new version block above this line when you release a new version -->

---

# Section 18 — Review & Sign-off

> # HOW TO FILL: Section 18
> Before this API goes to any real users, the right people must review and
> approve it. Think of this like signatures on an important document.
> Every person listed below must review their relevant section and sign off.
>
> ⚠️ This contract is not valid without all required sign-offs.

## 18.1 Review Checklist

| Reviewer | Section(s) Reviewed | Required? | Status | Date | Signature / Initials |
|---|---|---|---|---|---|
| Technical Lead | All | ✅ Required | `[ ] Approved  [ ] Changes needed` | `[FILL]` | `[FILL]` |
| Security Engineer | 4, 10, 12, 15 | ✅ Required | `[ ] Approved  [ ] Changes needed` | `[FILL]` | `[FILL]` |
| Product Manager | 1, 2, 16 | ✅ Required | `[ ] Approved  [ ] Changes needed` | `[FILL]` | `[FILL]` |
| QA Lead | 15, 10 | ✅ Required | `[ ] Approved  [ ] Changes needed` | `[FILL]` | `[FILL]` |
| Legal / Compliance | 12 | ✅ Required | `[ ] Approved  [ ] Changes needed` | `[FILL]` | `[FILL]` |
| DevOps / Infrastructure | 3, 11 | ✅ Required | `[ ] Approved  [ ] Changes needed` | `[FILL]` | `[FILL]` |
| AI Review (Claude) | 5, 6, 7, 8, 9, 10, 17 | 🤖 Automated | `[ ] Verified  [ ] Flags raised` | `[FILL]` | Auto |

## 18.2 Outstanding Issues

> List any open issues, risks, or decisions that are not yet resolved.
> All issues must be closed before Gate 1 (Section 16).

| ID | Issue / Risk | Owner | Priority | Target Close Date | Status |
|---|---|---|---|---|---|
| `ISS-001` | `[FILL: e.g., Rate limits not yet confirmed with Infra team]` | `[FILL]` | `High / Medium / Low` | `[FILL]` | `Open / Closed` |

## 18.3 Contract Version History

| Contract Version | Status | Changed By | Date | Summary of Change |
|---|---|---|---|---|
| `v1.0` | `[FILL: Draft / Approved]` | `[FILL]` | `[FILL: YYYY-MM-DD]` | Initial draft |

---

# Appendix A — Quick Reference Card

> Cut this out and pin it to your team's wiki or Slack channel.

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  [FILL: API NAME] — Quick Reference
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  Production URL :  [FILL]
  Staging URL    :  [FILL]
  Docs URL       :  [FILL]
  Status Page    :  [FILL]
  Current Version:  [FILL: v1]
  Auth           :  [FILL: Bearer JWT]
  Rate Limit     :  [FILL: 1,000 req/min]

  ON-CALL CONTACT:  [FILL: name + phone / PagerDuty link]
  SUPPORT EMAIL  :  [FILL: api-support@myapp.com]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

# Appendix B — Glossary

| Term | Plain-English Definition |
|---|---|
| **API** | Application Programming Interface — a way for two apps to talk to each other |
| **REST** | A style of API that uses standard web links (URLs) and HTTP methods like GET and POST |
| **GraphQL** | An API language where you ask for exactly the data you need |
| **gRPC** | A fast API method used between servers, like a phone call instead of letters |
| **WebSocket** | A live, two-way connection — like a phone call vs. REST's letters |
| **JWT** | A secure digital token proving who you are |
| **OAuth 2.0** | A way to give an app permission to access your data without sharing your password |
| **mTLS** | Both sides of a connection prove who they are with certificates |
| **RBAC** | Role-Based Access Control — what you can do depends on your role |
| **RFC 7807** | An internet standard for how APIs describe errors |
| **SLA** | Service Level Agreement — the uptime promise made to customers |
| **SLO** | Service Level Objective — internal performance goals |
| **PII** | Personally Identifiable Information — data that identifies a real person |
| **PHI** | Protected Health Information — health data covered by HIPAA |
| **GDPR** | European law protecting people's personal data |
| **HIPAA** | US law protecting health data |
| **SOC 2** | A security certification audit for software companies |
| **Rate limiting** | Capping how many requests a caller can make in a time window |
| **Idempotent** | Calling the same endpoint multiple times gives the same result |
| **Breaking change** | A change that causes existing code using the API to stop working |
| **Canary deploy** | Releasing to a small % of users first to catch problems early |
| **p95 latency** | 95% of requests complete faster than this time |

---

*This document was generated using the AI Contract Template v1.0.*
*Powered by Claude (Anthropic) · AI-Driven Development Life Cycle.*
*Template last updated: 2026-10-14*
