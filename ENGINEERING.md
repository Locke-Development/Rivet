# Rivet — Architecture and Control Boundaries

**Current inspected application:** `https://github.com/Amishgangsta/Rivet` · deployed `87beafb281a0f6bdc66674b0dfb1af1235c5cf9b` · November 13, 2026.

## Architecture in one diagram

```text
 Customer ATS / HRIS / Slack directories
       |  customer credential; bounded READ
       v
 [Vendor adapter / normalize] --> [Staged external records]
                                     |
                                     v
                         [Human link / create / ignore]
                                     |
                                     v
                           [Person context + ledger]
                                     |
      [AI drafts] ---> [Review / owner publish] 
                                     |
                                     v
                          [Frozen workflow version]
                                     |
                     [Conditions + dependencies]
                                     |
             +-----------------------+----------------------+
             |                       |                      |
       [Employee forms]      [Manager approvals]      [HR / IT tasks]
             |                       |                      |
             +------------- [Durable run] ------------------+
                                     |
                      [Outbox + exceptions + audit]
                                     |
                     [Analytics / status / export]
```

## Four authority boundaries

**A. External records are evidence, not truth by fiat.** Slack, Ashby and BambooHR provide normalized snapshots; imports are staged and explicitly linked. Email drift invalidates a link and opens exception review. No external directory update automatically overwrites Rivet's linked person record.

**B. Drafting is not publication.** A schema-bounded model proposal must be reviewed. Publish is a separate owner-only action; run launch follows another explicit choice. The adaptive definition validator requires approval dependencies for consequential offboarding/role-change workflows and rejects dependency cycles.

**C. Participant role access is not broad staff authentication.** Expiring scoped links bind to a run and role, revealing assigned modules only. Public user accounts for all employees, team-wide SSO and SCIM are not included in this release.

**D. An external side effect has an outcome, not a hopeful retry.** The Slack adapter reserves a request identifier before sending. An uncertain response remains unknown; it is not automatically resent. An adaptive reminder can be queued, provider-accepted or unknown. Neither means confirmed human receipt.

## Narrow signed source-event ingress

The current application implements an HMAC-signed `candidate.hired` source endpoint. It stores a verified event as `identity_pending`; a human must link the candidate to a real person and approve workflow launch. **This is not general ATS/HRIS webhook ingestion**, which the README and release boundary explicitly list as unshipped.

## State and scheduling

- **Tenant isolation:** hosted PostgreSQL with enforced row-level security and a restricted runtime database role; separate migrations and maintenance credentials.
- **Local evaluation:** SQLite-compatible local store; local records and secrets are not imported into hosted mode automatically.
- **Adaptive state:** versions/definitions/runs/events/access grants/deliveries; per-tenant serialized work, revision checks and audit entries.
- **Schedule:** due offsets from verified anchor dates at a 9 AM local time in a valid IANA timezone, including offset/DST handling.
- **Worker:** scheduled reminders and escalation are independent of an open browser; delivery is not assumed after a timeout.
- **Connectors:** fixed trusted vendor hosts, redirect blocking, bounded payload/timeout/page counts and AES-GCM credential storage.

## Operational versus Visitor Intelligence analytics

**Workspace Analytics:** derived from saved employee runs/tasks (completion, overdue, approvals, baseline effort). **Visitor Intelligence:** separate first-party opt-in, platform-admin-only usage analytics, with privacy notices, retention/deletion and synthetic live verification. It is **not** a public dashboard and should never expose personnel form data or AI prompt content. See [VISITOR-INTELLIGENCE.md](VISITOR-INTELLIGENCE.md).

## Release / implementation limitation

Although the running Railway services have a successful feature-branch deployment, the GitHub default `main` remains older and draft PR #1 remains unmerged. The documentation-head SHA is not the deployed application SHA. None of these facts establish a production SLA, vendor-account integration certification, or commercial subscription readiness.

[Atomic features](FEATURE-MATRIX.md) · [Exact status](VERIFICATION-AND-STATUS.md) · [Sources](METHODOLOGY.md)
