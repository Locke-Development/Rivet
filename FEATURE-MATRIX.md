# Rivet — Individual Feature and Gap Register

**Inspected November 13, 2026** · **Deployed source:** `87beafb281a0f6bdc66674b0dfb1af1235c5cf9b` on `feature/visitor-intelligence` · **Feature branch documentation HEAD:** `d8c3cda80b10aa839127c5d0a0adc563457d13ba`.

**433 atomic source-mapped checklist entries across 20 areas.** A checklist entry is one product capability or explicit missing feature; the count is not a count of live E2E tests, unique selling points, or verified competitor gaps.

**Evidence labels:** Source-implemented = source code and docs provide the behavior; source / configuration-dependent = real customer credentials/provider runtime needed; source + recorded live synthetic verification = first-party synthetic browser and authenticated admin checks recorded October 26; not shipped = explicitly not part of this Rivet release.

## Feature inventory

| Section | Individually identified items | Evidence |
|---|---:|---|
| Workspace structure / UX | 22 | `app/main.js` |
| People and basic employee journeys | 20 | `lifecycle-store.mjs` |
| Lifecycle workflow definitions | 22 | `operations-store.mjs` |
| Lifecycle run operations | 20 | `operations-store.mjs` |
| Exceptions and operational audit | 18 | `operations-store.mjs` |
| Identity imports and matching | 22 | `operations-store.mjs` |
| Adaptive definition builder | 31 | `journey-store.mjs` |
| Adaptive run coordination | 28 | `journey-store.mjs` |
| Participant access and scoped action | 19 | `journey-store.mjs` |
| Source-event and outbound reminders | 26 | `journey-store.mjs` |
| Slack connector | 20 | `connectors.mjs` |
| Ashby connector | 17 | `connectors.mjs` |
| BambooHR connector | 16 | `connectors.mjs` |
| Connector security and resilience | 18 | `connectors.mjs` |
| AI drafting and controlled publishing | 18 | `openai-workflows.mjs` |
| Hosted identity, tenancy, and releases | 24 | `hosted/auth.mjs` |
| Workspace operational analytics | 15 | `app/operations.js` |
| Visitor consent and privacy | 23 | `app/visitor-analytics.js` |
| Visitor Intelligence reporting | 34 | `app/visitor-intelligence.js` |
| Known non-shipped product areas | 20 | `README.md` |

**This register is not proof that the app is fully production-ready or that each vendor offers/does not offer every sub-behavior.** For current competitor category parity and limitations, use [COMPARISON.md](COMPARISON.md).

## Workspace structure / UX

**Source paths:** `app/main.js`, `app/operations.js`, `app/styles.css`. **Area classification:** Source-implemented.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 1 | Overview dashboard | Source-implemented |
| 2 | Lifecycle runs navigation | Source-implemented |
| 3 | Employee journeys navigation | Source-implemented |
| 4 | Exceptions navigation | Source-implemented |
| 5 | People directory navigation | Source-implemented |
| 6 | People matching navigation | Source-implemented |
| 7 | Workflow editor navigation | Source-implemented |
| 8 | Connections navigation | Source-implemented |
| 9 | Workspace Analytics navigation | Source-implemented |
| 10 | Audit navigation | Source-implemented |
| 11 | Settings navigation | Source-implemented |
| 12 | Adaptive journeys navigation | Source-implemented |
| 13 | Owner/operator gated actions | Source-implemented |
| 14 | Actual saved-record counts | Source-implemented |
| 15 | Empty-state messaging | Source-implemented |
| 16 | Status indicators | Source-implemented |
| 17 | Workflow detail expansion | Source-implemented |
| 18 | User-safe strings rendered with HTML escaping | Source-implemented |
| 19 | Record refresh after operation | Source-implemented |
| 20 | Responsive workspace shell | Source-implemented |
| 21 | Separate participant page | Source-implemented |
| 22 | Export-workspace download | Source-implemented |

## People and basic employee journeys

**Source paths:** `lifecycle-store.mjs`, `hosted/lifecycle-store.mjs`, `app/main.js`. **Area classification:** Source-implemented.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 23 | Create a person | Source-implemented |
| 24 | List saved people | Source-implemented |
| 25 | Retrieve selected person | Source-implemented |
| 26 | Store first name | Source-implemented |
| 27 | Store last name | Source-implemented |
| 28 | Store email | Source-implemented |
| 29 | Store role | Source-implemented |
| 30 | Store department | Source-implemented |
| 31 | Store hire/start date | Source-implemented |
| 32 | Create employee journey | Source-implemented |
| 33 | List journey tasks | Source-implemented |
| 34 | Complete employee task | Source-implemented |
| 35 | Add a journey task | Source-implemented |
| 36 | Change person start date | Source-implemented |
| 37 | Record actor on completed task | Source-implemented |
| 38 | Record AI proposal review | Source-implemented |
| 39 | Approve suggested task additions individually | Source-implemented |
| 40 | Show start-date adjustments | Source-implemented |
| 41 | Keep person and journey scoped to tenant | Source-implemented |
| 42 | Maintain person journey audit metadata | Source-implemented |

## Lifecycle workflow definitions

**Source paths:** `operations-store.mjs`, `app/operations.js`, `openai-workflows.mjs`. **Area classification:** Source-implemented.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 43 | Define onboarding workflow | Source-implemented |
| 44 | Define offboarding workflow | Source-implemented |
| 45 | Define role-change workflow | Source-implemented |
| 46 | Define leave workflow | Source-implemented |
| 47 | Define return workflow | Source-implemented |
| 48 | Set workflow name and description | Source-implemented |
| 49 | Define task title | Source-implemented |
| 50 | Define task owner | Source-implemented |
| 51 | Define step due offset | Source-implemented |
| 52 | Require step approval | Source-implemented |
| 53 | Save workflow as draft | Source-implemented |
| 54 | Edit workflow draft | Source-implemented |
| 55 | Edit published workflow into new draft | Source-implemented |
| 56 | Review draft before publication | Source-implemented |
| 57 | Publish workflow owner-only | Source-implemented |
| 58 | Validate definition before publication | Source-implemented |
| 59 | Preserve published definition version | Source-implemented |
| 60 | Select published definition to launch | Source-implemented |
| 61 | Freeze launched workflow step snapshot | Source-implemented |
| 62 | Reject unsupported lifecycle type | Source-implemented |
| 63 | Enforce workflow capacity limit | Source-implemented |
| 64 | Respect active-run ownership | Source-implemented |

## Lifecycle run operations

**Source paths:** `operations-store.mjs`, `app/operations.js`. **Area classification:** Source-implemented.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 65 | Launch lifecycle run for stored person | Source-implemented |
| 66 | Create durable run ID | Source-implemented |
| 67 | Record run lifecycle type | Source-implemented |
| 68 | Track due-date per step | Source-implemented |
| 69 | View open run steps | Source-implemented |
| 70 | Pause active run | Source-implemented |
| 71 | Resume paused run | Source-implemented |
| 72 | Prevent task completion while paused | Source-implemented |
| 73 | Approve gated step | Source-implemented |
| 74 | Block completion before approval | Source-implemented |
| 75 | Complete eligible task | Source-implemented |
| 76 | Show step status | Source-implemented |
| 77 | Derive run completion from steps | Source-implemented |
| 78 | Record run actor | Source-implemented |
| 79 | Record workflow version on run | Source-implemented |
| 80 | List overdue tasks | Source-implemented |
| 81 | Compute completion rate from persisted runs | Source-implemented |
| 82 | Record state transition audit | Source-implemented |
| 83 | Cancel run where adaptive workflow supported | Source-implemented |
| 84 | Prevent stale version update | Source-implemented |

## Exceptions and operational audit

**Source paths:** `operations-store.mjs`, `app/operations.js`. **Area classification:** Source-implemented.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 85 | Raise exception | Source-implemented |
| 86 | Assign exception owner | Source-implemented |
| 87 | Set exception severity | Source-implemented |
| 88 | Write exception detail | Source-implemented |
| 89 | Set exception status | Source-implemented |
| 90 | Resolve exception | Source-implemented |
| 91 | Retain resolution explanation | Source-implemented |
| 92 | List open exceptions | Source-implemented |
| 93 | Filter exception list | Source-implemented |
| 94 | Show open exceptions on overview | Source-implemented |
| 95 | Preserve audit actor ID | Source-implemented |
| 96 | Preserve actor role | Source-implemented |
| 97 | Preserve object ID | Source-implemented |
| 98 | Record prior and next version | Source-implemented |
| 99 | Record sanitized changed field names | Source-implemented |
| 100 | Export audit with workspace backup | Source-implemented |
| 101 | Read latest activity list | Source-implemented |
| 102 | Guard owner-only sensitive operations | Source-implemented |

## Identity imports and matching

**Source paths:** `operations-store.mjs`, `connectors.mjs`, `docs/full-workspace.md`. **Area classification:** Source-implemented.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 103 | Stage external records before linking | Source-implemented |
| 104 | Import bounded JSON batch | Source-implemented |
| 105 | Require external source ID | Source-implemented |
| 106 | Require email for matching | Source-implemented |
| 107 | Normalize email case | Source-implemented |
| 108 | Preserve source-specific identifier | Source-implemented |
| 109 | List unmatched source records | Source-implemented |
| 110 | View candidate-to-person matching | Source-implemented |
| 111 | Explicitly link existing person | Source-implemented |
| 112 | Explicitly create person from source | Source-implemented |
| 113 | Explicitly ignore source record | Source-implemented |
| 114 | Record match outcome | Source-implemented |
| 115 | Reject duplicate source link to one person | Source-implemented |
| 116 | Detect email drift in linked record | Source-implemented |
| 117 | Invalidate stale email link | Source-implemented |
| 118 | Raise exception on drift | Source-implemented |
| 119 | Keep source record provenance | Source-implemented |
| 120 | Keep conflicting records separate | Source-implemented |
| 121 | Prevent direct overwrite of authoritative person | Source-implemented |
| 122 | Do not infer start date from incomplete vendor data | Source-implemented |
| 123 | Limit manual import batch size | Source-implemented |
| 124 | Tenant-scoped match actions | Source-implemented |

## Adaptive definition builder

**Source paths:** `journey-store.mjs`, `journey-validation.mjs`, `app/adaptive.js`. **Area classification:** Source-implemented.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 125 | Create adaptive definition | Source-implemented |
| 126 | Edit adaptive draft | Source-implemented |
| 127 | Publish validated definition | Source-implemented |
| 128 | Keep immutable launched definition version | Source-implemented |
| 129 | Select lifecycle type | Source-implemented |
| 130 | Use task module | Source-implemented |
| 131 | Use content module | Source-implemented |
| 132 | Use form module | Source-implemented |
| 133 | Use acknowledgment module | Source-implemented |
| 134 | Use approval module | Source-implemented |
| 135 | Assign employee role | Source-implemented |
| 136 | Assign manager role | Source-implemented |
| 137 | Assign IT role | Source-implemented |
| 138 | Assign HR role | Source-implemented |
| 139 | Set relative due-day offset | Source-implemented |
| 140 | Set reminder interval | Source-implemented |
| 141 | Define module dependencies | Source-implemented |
| 142 | Validate dependency target exists | Source-implemented |
| 143 | Reject dependency cycles | Source-implemented |
| 144 | Define conditional step | Source-implemented |
| 145 | Support equals condition | Source-implemented |
| 146 | Support not-equals condition | Source-implemented |
| 147 | Support person context fields | Source-implemented |
| 148 | Support prior-form answer conditions | Source-implemented |
| 149 | Block on missing conditional value | Source-implemented |
| 150 | Validate required text answer | Source-implemented |
| 151 | Validate select answer options | Source-implemented |
| 152 | Validate required checkbox | Source-implemented |
| 153 | Limit modules per definition | Source-implemented |
| 154 | Require approval dependency for consequential work | Source-implemented |
| 155 | Prevent publishing invalid definitions | Source-implemented |

## Adaptive run coordination

**Source paths:** `journey-store.mjs`, `journey-worker.mjs`, `app/adaptive.js`. **Area classification:** Source-implemented.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 156 | Launch published adaptive definition | Source-implemented |
| 157 | Require selected stored person | Source-implemented |
| 158 | Require explicit manager assignment | Source-implemented |
| 159 | Validate assigned participant emails | Source-implemented |
| 160 | Capture signed-off anchor date | Source-implemented |
| 161 | Apply valid IANA timezone | Source-implemented |
| 162 | Compute due date at local 9am | Source-implemented |
| 163 | Account for timezone offset and DST | Source-implemented |
| 164 | Evaluate dependencies before step ready | Source-implemented |
| 165 | Mark waiting dependency | Source-implemented |
| 166 | Mark scheduled step | Source-implemented |
| 167 | Mark ready step | Source-implemented |
| 168 | Block missing condition input | Source-implemented |
| 169 | Mark false-condition step skipped | Source-implemented |
| 170 | Display skipped reason | Source-implemented |
| 171 | Prevent action while paused | Source-implemented |
| 172 | Pause adaptive run | Source-implemented |
| 173 | Resume adaptive run | Source-implemented |
| 174 | Cancel adaptive run | Source-implemented |
| 175 | Change future anchor schedule | Source-implemented |
| 176 | Preserve completed-step history | Source-implemented |
| 177 | Complete form module | Source-implemented |
| 178 | Record acknowledgment | Source-implemented |
| 179 | Require assigned approver to approve | Source-implemented |
| 180 | Maintain run version and audit | Source-implemented |
| 181 | Derive readiness from completed modules | Source-implemented |
| 182 | Process due tenants with worker tick | Source-implemented |
| 183 | Keep notification work independent of browser | Source-implemented |

## Participant access and scoped action

**Source paths:** `journey-store.mjs`, `app/participant.js`, `server.mjs`. **Area classification:** Source-implemented.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 184 | Issue scoped participant access link | Source-implemented |
| 185 | Encode role-specific access grant | Source-implemented |
| 186 | Hash bearer token at rest | Source-implemented |
| 187 | Expire participant grant | Source-implemented |
| 188 | Revoke participant grant | Source-implemented |
| 189 | Enforce assigned module visibility | Source-implemented |
| 190 | Exclude other employees and roles | Source-implemented |
| 191 | Allow participant to complete owned task | Source-implemented |
| 192 | Allow participant to submit owned form | Source-implemented |
| 193 | Allow participant to acknowledge guidance | Source-implemented |
| 194 | Allow manager approval for owned step | Source-implemented |
| 195 | Deny unassigned approval | Source-implemented |
| 196 | Deny expired token | Source-implemented |
| 197 | Deny revoked token | Source-implemented |
| 198 | Keep token out of URL server path using fragment | Source-implemented |
| 199 | Clear token fragment after load | Source-implemented |
| 200 | Keep bearer token in memory rather than local storage | Source-implemented |
| 201 | Protect participant endpoint against workspace escalation | Source-implemented |
| 202 | Do not treat scoped participant as full employee account | Source-implemented |

## Source-event and outbound reminders

**Source paths:** `journey-store.mjs`, `journey-worker.mjs`, `mailer.mjs`, `server.mjs`. **Area classification:** Source-implemented; conditional delivery.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 203 | Register purpose-specific source | Source / configuration-dependent |
| 204 | Generate source signing secret | Source / configuration-dependent |
| 205 | Revoke event source | Source / configuration-dependent |
| 206 | Accept candidate.hired event type | Source / configuration-dependent |
| 207 | Validate HMAC SHA-256 signature | Source / configuration-dependent |
| 208 | Verify event timestamp freshness | Source / configuration-dependent |
| 209 | Reject event replay | Source / configuration-dependent |
| 210 | Deduplicate repeated event | Source / configuration-dependent |
| 211 | Persist event in identity_pending | Source / configuration-dependent |
| 212 | Require owner identity review | Source / configuration-dependent |
| 213 | Bind source event to existing person explicitly | Source / configuration-dependent |
| 214 | Avoid automatic creation/launch on event | Source / configuration-dependent |
| 215 | Queue first-step invitation | Source / configuration-dependent |
| 216 | Queue timed reminder | Source / configuration-dependent |
| 217 | Reserve notification ID before send | Source / configuration-dependent |
| 218 | Preserve outbound encrypted delivery material | Source / configuration-dependent |
| 219 | Mark delivery queued | Source / configuration-dependent |
| 220 | Mark provider-accepted state | Source / configuration-dependent |
| 221 | Mark outcome unknown when uncertain | Source / configuration-dependent |
| 222 | Avoid automatic resend of unknown outcome | Source / configuration-dependent |
| 223 | Bound reminder count | Source / configuration-dependent |
| 224 | Send only with configured mail provider | Source / configuration-dependent |
| 225 | Perform outbound send outside database lock | Source / configuration-dependent |
| 226 | Use participant-specific invitation link | Source / configuration-dependent |
| 227 | Track notification status in UI | Source / configuration-dependent |
| 228 | Do not represent provider acceptance as inbox delivery | Source / configuration-dependent |

## Slack connector

**Source paths:** `connectors.mjs`, `docs/connector-contracts.md`, `operations-store.mjs`. **Area classification:** Implemented adapter; live credentials conditional.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 229 | Verify Slack bot token via auth.test | Source / configuration-dependent |
| 230 | Read Slack users.list | Source / configuration-dependent |
| 231 | Paginate Slack cursor | Source / configuration-dependent |
| 232 | Exclude bot accounts | Source / configuration-dependent |
| 233 | Exclude deleted accounts | Source / configuration-dependent |
| 234 | Normalize user ID and email | Source / configuration-dependent |
| 235 | Normalize name/title | Source / configuration-dependent |
| 236 | Read sync directory | Source / configuration-dependent |
| 237 | Require users:read and optional users:read.email | Source / configuration-dependent |
| 238 | Accept exact destination channel ID | Source / configuration-dependent |
| 239 | Require chat:write permission in real customer tenant | Source / configuration-dependent |
| 240 | Require owner approval for message | Source / configuration-dependent |
| 241 | Require exact message text approval | Source / configuration-dependent |
| 242 | Persist send request ID before posting | Source / configuration-dependent |
| 243 | Use chat.postMessage | Source / configuration-dependent |
| 244 | No automatic retries of ambiguous send | Source / configuration-dependent |
| 245 | Preserve outcome-unknown on timeout | Source / configuration-dependent |
| 246 | Sanitize transport failures | Source / configuration-dependent |
| 247 | Encrypt stored credential | Source / configuration-dependent |
| 248 | Allow disconnect | Source / configuration-dependent |

## Ashby connector

**Source paths:** `connectors.mjs`, `docs/connector-contracts.md`. **Area classification:** Implemented adapter; live credentials conditional.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 249 | Verify candidate.list endpoint | Source / configuration-dependent |
| 250 | Use customer API key basic authentication | Source / configuration-dependent |
| 251 | Require candidatesRead entitlement | Source / configuration-dependent |
| 252 | Fetch candidate records read-only | Source / configuration-dependent |
| 253 | Paginate nextCursor with moreDataAvailable | Source / configuration-dependent |
| 254 | Normalize candidate external ID | Source / configuration-dependent |
| 255 | Normalize primary email | Source / configuration-dependent |
| 256 | Normalize person name | Source / configuration-dependent |
| 257 | Normalize position to role | Source / configuration-dependent |
| 258 | Stage candidate rather than auto-hire | Source / configuration-dependent |
| 259 | Do not invent department | Source / configuration-dependent |
| 260 | Do not invent start date | Source / configuration-dependent |
| 261 | Bounds on pages | Source / configuration-dependent |
| 262 | Reject malformed provider records | Source / configuration-dependent |
| 263 | Prevent unauthorized vendor write-back | Source / configuration-dependent |
| 264 | Encrypt stored credential | Source / configuration-dependent |
| 265 | Expose verify and sync statuses | Source / configuration-dependent |

## BambooHR connector

**Source paths:** `connectors.mjs`, `docs/connector-contracts.md`. **Area classification:** Implemented adapter; live credentials conditional.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 266 | Verify customer subdomain format | Source / configuration-dependent |
| 267 | Reject URL or malicious subdomain | Source / configuration-dependent |
| 268 | Read employee directory endpoint | Source / configuration-dependent |
| 269 | Use customer API key | Source / configuration-dependent |
| 270 | Respect customer directory permission | Source / configuration-dependent |
| 271 | Normalize employee ID | Source / configuration-dependent |
| 272 | Normalize work email | Source / configuration-dependent |
| 273 | Normalize job title | Source / configuration-dependent |
| 274 | Normalize department | Source / configuration-dependent |
| 275 | Avoid assuming directory is full payroll roster | Source / configuration-dependent |
| 276 | Avoid inferring missing hire date | Source / configuration-dependent |
| 277 | Stage directory records for identity review | Source / configuration-dependent |
| 278 | Perform read-only sync | Source / configuration-dependent |
| 279 | Reject invalid provider response | Source / configuration-dependent |
| 280 | Encrypt stored credential | Source / configuration-dependent |
| 281 | Allow connection revoke | Source / configuration-dependent |

## Connector security and resilience

**Source paths:** `connectors.mjs`, `operations-store.mjs`, `hosted/config.mjs`. **Area classification:** Source-implemented.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 282 | Use AES-256-GCM for stored credentials | Source-implemented |
| 283 | Redact secrets from responses | Source-implemented |
| 284 | Exclude secrets from exported JSON | Source-implemented |
| 285 | Reject arbitrary connector base URLs | Source-implemented |
| 286 | Use fixed Slack/Ashby API origins | Source-implemented |
| 287 | Construct constrained BambooHR host | Source-implemented |
| 288 | Disallow HTTP redirects | Source-implemented |
| 289 | Bound request timeout | Source-implemented |
| 290 | Bound response bytes | Source-implemented |
| 291 | Bound provider pagination | Source-implemented |
| 292 | Reject repeated pagination cursor | Source-implemented |
| 293 | Reject malformed entire sync batch | Source-implemented |
| 294 | Avoid partial staging on failed sync | Source-implemented |
| 295 | Sanitize provider errors | Source-implemented |
| 296 | Keep connection limited to configured tenant | Source-implemented |
| 297 | No native vendor OAuth implemented | Not shipped |
| 298 | No generic inbound vendor-signed webhooks implemented | Not shipped |
| 299 | No ATS/HRIS record write-back implemented | Not shipped |

## AI drafting and controlled publishing

**Source paths:** `openai-workflows.mjs`, `openai-journey.mjs`, `server.mjs`. **Area classification:** Configured-provider dependent.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 300 | Accept free-text workflow goal | Source / configuration-dependent |
| 301 | Generate suggested workflow structure | Source / configuration-dependent |
| 302 | Use available OpenAI model | Source / configuration-dependent |
| 303 | Restrict model output schema | Source / configuration-dependent |
| 304 | Reject malformed AI draft | Source / configuration-dependent |
| 305 | Show proposed steps before save | Source / configuration-dependent |
| 306 | Permit owner edits | Source / configuration-dependent |
| 307 | Prevent implicit save | Source / configuration-dependent |
| 308 | Prevent implicit publish | Source / configuration-dependent |
| 309 | Owner review before publish | Source / configuration-dependent |
| 310 | Human review each proposed journey task | Source / configuration-dependent |
| 311 | Do not include existing personnel records in generic workflow prompt | Source / configuration-dependent |
| 312 | Restrict AI request length | Source / configuration-dependent |
| 313 | Apply daily tenant AI quota | Source / configuration-dependent |
| 314 | Apply service-wide AI quota | Source / configuration-dependent |
| 315 | Report provider unavailable | Source / configuration-dependent |
| 316 | Avoid model output executing connector sends | Source / configuration-dependent |
| 317 | Record AI draft-review event | Source / configuration-dependent |

## Hosted identity, tenancy, and releases

**Source paths:** `hosted/auth.mjs`, `hosted/db.mjs`, `hosted/migrate.mjs`, `hosted/migrations/001_hosted_preview.sql`, `permissions.mjs`. **Area classification:** Source-implemented; deployed.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 318 | Hosted PostgreSQL mode | Source-implemented |
| 319 | Local SQLite mode | Source-implemented |
| 320 | Tenant row-level security | Source-implemented |
| 321 | Restricted rivet_runtime database role | Source-implemented |
| 322 | Separate privileged migration runner | Source-implemented |
| 323 | Require SESSION_SECRET | Source-implemented |
| 324 | Separate invitation secret | Source-implemented |
| 325 | Encrypt connector data per hosted secret | Source-implemented |
| 326 | Owner role | Source-implemented |
| 327 | Operator role | Source-implemented |
| 328 | Enforce owner-only sensitive actions server-side | Source-implemented |
| 329 | Resolve current membership on every request | Source-implemented |
| 330 | Invite tester into separate empty tenant | Source-implemented |
| 331 | Redeem invitation | Source-implemented |
| 332 | Maintain existing session compatibility | Source-implemented |
| 333 | Logout session | Source-implemented |
| 334 | Restrict cross-tenant read | Source-implemented |
| 335 | Restrict cross-tenant write | Source-implemented |
| 336 | Validate request origin for mutations | Source-implemented |
| 337 | Readiness endpoint | Source-implemented |
| 338 | Schema-version readiness | Source-implemented |
| 339 | Private migrations 001-004 | Source-implemented |
| 340 | Use Railway production service | Source-implemented |
| 341 | Keep migration secrets off web service | Source-implemented |

## Workspace operational analytics

**Source paths:** `app/operations.js`, `operations-store.mjs`, `docs/full-workspace.md`. **Area classification:** Source-implemented.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 342 | Count people from records | Source-implemented |
| 343 | Count active workflow runs | Source-implemented |
| 344 | Count completed steps | Source-implemented |
| 345 | Count overdue steps | Source-implemented |
| 346 | Count pending approvals | Source-implemented |
| 347 | Count open exceptions | Source-implemented |
| 348 | Compute completion percentage | Source-implemented |
| 349 | Show time-based workflow dashboard | Source-implemented |
| 350 | Display recorded activity | Source-implemented |
| 351 | Calculate baseline effort estimate | Source-implemented |
| 352 | Use workspace baseline setting | Source-implemented |
| 353 | Separate baseline estimates from measured savings | Source-implemented |
| 354 | Do not invent reported success for incomplete steps | Source-implemented |
| 355 | Export saved workspace JSON | Source-implemented |
| 356 | Keep operational metrics separate from visitor analytics | Source-implemented |

## Visitor consent and privacy

**Source paths:** `app/visitor-analytics.js`, `hosted/migrations/004_visitor_intelligence.sql`, `docs/visitor-intelligence-operator-guide.md`. **Area classification:** Deployed; synthetic live verification.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 357 | Require explicit Accept analytics | Source + recorded live synthetic verification |
| 358 | Allow Decline analytics | Source + recorded live synthetic verification |
| 359 | Respect Global Privacy Control | Source + recorded live synthetic verification |
| 360 | Create no tracking ID before consent | Source + recorded live synthetic verification |
| 361 | Use first-party HttpOnly Secure cookies after consent | Source + recorded live synthetic verification |
| 362 | Track only approved safe event types | Source + recorded live synthetic verification |
| 363 | Exclude employee form field values | Source + recorded live synthetic verification |
| 364 | Exclude AI prompts and answers | Source + recorded live synthetic verification |
| 365 | Exclude credentials and tokens | Source + recorded live synthetic verification |
| 366 | Exclude participant portal | Source + recorded live synthetic verification |
| 367 | Exclude admin portal | Source + recorded live synthetic verification |
| 368 | Allow withdrawal | Source + recorded live synthetic verification |
| 369 | Allow browser data deletion | Source + recorded live synthetic verification |
| 370 | Allow associated account deletion | Source + recorded live synthetic verification |
| 371 | Mark internal test browser | Source + recorded live synthetic verification |
| 372 | Exclude internal device from default reports | Source + recorded live synthetic verification |
| 373 | Prevent arbitrary referrer URL retention | Source + recorded live synthetic verification |
| 374 | Use opaque campaign key | Source + recorded live synthetic verification |
| 375 | Use 30-day raw default retention | Source + recorded live synthetic verification |
| 376 | Use 90-day reporting fact default retention | Source + recorded live synthetic verification |
| 377 | Keep replay disabled | Source + recorded live synthetic verification |
| 378 | Keep heatmaps disabled | Source + recorded live synthetic verification |
| 379 | Report unknown geography accurately | Source + recorded live synthetic verification |

## Visitor Intelligence reporting

**Source paths:** `app/visitor-intelligence.js`, `visitor-analytics/store.mjs`, `docs/visitor-intelligence-operator-guide.md`. **Area classification:** Private admin only; synthetic live verified.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 380 | Dedicated platform-administrator grant | Source + recorded live synthetic verification |
| 381 | Do not infer admin from workspace owner | Source + recorded live synthetic verification |
| 382 | Private reports require authentication | Source + recorded live synthetic verification |
| 383 | Private exports require separate platform grant | Source + recorded live synthetic verification |
| 384 | Summary report | Source + recorded live synthetic verification |
| 385 | Visitor/installation report | Source + recorded live synthetic verification |
| 386 | Testers/account association report | Source + recorded live synthetic verification |
| 387 | Session drill-down | Source + recorded live synthetic verification |
| 388 | Feature-entry report | Source + recorded live synthetic verification |
| 389 | Navigation-path report | Source + recorded live synthetic verification |
| 390 | Control activation report | Source + recorded live synthetic verification |
| 391 | Attempt/outcome report | Source + recorded live synthetic verification |
| 392 | Estimated foreground engagement | Source + recorded live synthetic verification |
| 393 | Day/week/month trends | Source + recorded live synthetic verification |
| 394 | Conversion funnel report | Source + recorded live synthetic verification |
| 395 | Custom allowlisted funnel definition | Source + recorded live synthetic verification |
| 396 | Funnel evidence windows | Source + recorded live synthetic verification |
| 397 | Pending versus matured-abandonment distinction | Source + recorded live synthetic verification |
| 398 | Structured visitor feedback | Source + recorded live synthetic verification |
| 399 | Improvement-opportunity ranking | Source + recorded live synthetic verification |
| 400 | Performance metric report | Source + recorded live synthetic verification |
| 401 | Campaign attribution report | Source + recorded live synthetic verification |
| 402 | Traffic source categories | Source + recorded live synthetic verification |
| 403 | Device/browser category filtering | Source + recorded live synthetic verification |
| 404 | Feature/date/visitor/tester filtering | Source + recorded live synthetic verification |
| 405 | CSV export | Source + recorded live synthetic verification |
| 406 | JSON export | Source + recorded live synthetic verification |
| 407 | Export size and row bounds | Source + recorded live synthetic verification |
| 408 | Spreadsheet formula escaping | Source + recorded live synthetic verification |
| 409 | Audited admin export access | Source + recorded live synthetic verification |
| 410 | No replay recording | Source + recorded live synthetic verification |
| 411 | No visual heatmap capture | Source + recorded live synthetic verification |
| 412 | Do not treat browser installations as physical devices | Source + recorded live synthetic verification |
| 413 | Do not treat estimated active time as verified attention | Source + recorded live synthetic verification |

## Known non-shipped product areas

**Source paths:** `README.md`, `docs/full-workspace.md`, `docs/connector-contracts.md`. **Area classification:** Not implemented / not certified.

| # | Individual behavior, control or gap | Rivet assessment |
|---:|---|---|
| 414 | Native generic vendor OAuth | Not shipped / not established |
| 415 | Generic signed vendor HRIS webhooks | Not shipped / not established |
| 416 | Direct BambooHR employee write-back | Not shipped / not established |
| 417 | Direct Ashby candidate write-back | Not shipped / not established |
| 418 | Automated device procurement/provisioning | Not shipped / not established |
| 419 | Automated app account provisioning | Not shipped / not established |
| 420 | Native payroll processing | Not shipped / not established |
| 421 | Native benefits administration | Not shipped / not established |
| 422 | Interactive Slack approval buttons | Not shipped / not established |
| 423 | Enterprise SSO | Not shipped / not established |
| 424 | SCIM user provisioning | Not shipped / not established |
| 425 | Paid subscription checkout | Not shipped / not established |
| 426 | Customer billing/invoicing | Not shipped / not established |
| 427 | Wide connector marketplace | Not shipped / not established |
| 428 | Dedicated employee identity accounts | Not shipped / not established |
| 429 | Employee mobile push app | Not shipped / not established |
| 430 | SMS/WhatsApp process channels | Not shipped / not established |
| 431 | External independent security certification | Not shipped / not established |
| 432 | Production performance SLA | Not shipped / not established |
| 433 | Unrestricted public Visitor Intelligence dashboard | Not shipped / not established |

## Audit conclusions

- **433 rows** in 20 groups, including explicit missing capabilities. The total deliberately includes separate controls and data-handling behaviors, not merely navigation labels.
- Baseline workspace flows, adaptive journey orchestration and private Visitor Intelligence have distinct release and proof requirements.
- Connector contract tests used injected HTTP fixtures; customer Slack/Ashby/BambooHR credentials and scopes were not independently exercised for this package.
- The narrow HMAC-signed candidate event receiver is real; generic inbound vendor webhook integrations are not shipped.
- Existing primary evidence: [current status](VERIFICATION-AND-STATUS.md), [architecture](ENGINEERING.md), [vendor comparison](COMPARISON.md), [methodology](METHODOLOGY.md).
