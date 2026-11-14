# Rivet — Verification and Current Release Status

**Verified November 13, 2026 from private GitHub, Railway and the project's recorded tests.**

| Item | Exact evidence / qualification |
|---|---|
| Repository | `https://github.com/Amishgangsta/Rivet`, **private** |
| Default main | `2e3065d97b68f621b314771371cd1ccec44ff65b`, October 18 |
| Feature branch | `feature/visitor-intelligence`, current HEAD `d8c3cda80b10aa839127c5d0a0adc563457d13ba`; later updates primarily documentation |
| Production web and migrations | Railway project `Rivet`; both services **SUCCESS** on **`87beafb281a0f6bdc66674b0dfb1af1235c5cf9b`**, October 26 |
| Public host | [https://rivet-production-7d9c.up.railway.app/](https://rivet-production-7d9c.up.railway.app/); authenticated application; no unauthenticated test evidence provided here |
| PR status | [Draft PR #1](https://github.com/Amishgangsta/Rivet/pull/1), still open and unmerged on inspection |
| Most recent recorded local suite | **233 passed, 0 failed, 0 skipped**, October 26, disposable PostgreSQL test cluster |
| Browser verification | Synthetic browser at desktop, tablet and mobile; all 14 private report views and related controls checked locally |
| Later production synthetic verification | Private dashboard/admin exports, session recording, internal exclusion, withdrawal and deletion documented as working with authorized account |
| Vendor API account tests | **Not verified** for live Slack/Ashby/BambooHR customer entitlements; connector adapter tests use fixtures |
| Remote provisioning/payroll | **Not shipped** |
| OAuth / generic vendor webhooks / HRIS writes | **Not shipped**; specific signed candidate.hired ingress implemented separately |
| Enterprise SSO/SCIM and commercial billing | **Not shipped** |
| Subscription price / ARR / enterprise customer adoption | **Cannot verify from available current sources** |
| Independent security certification | **Cannot verify from available current sources** |
| Live `/health` `/ready` reachability in this package session | **Not newly HTTP-probed**; Railway deployment SUCCESS is not an active endpoint response |

## What was actually tested

The project's October 26 report ran the full Node test suite against an isolated PostgreSQL 18.3 cluster with schema/role setup. A separate Playwright preview inspected responsive dashboard layouts, privacy/report controls and CSV/JSON exports. The production handoff then recorded login, 14 reports, admin permissions, opt-in session activity, an internal-device exclusion, deletion and withdrawal in a **synthetic** browser. The current brochure has not re-executed those tests or any real enterprise connector workflow.

## Material distinction: current feature branch versus default branch

The richer implementation is deployed from a **feature branch** but not merged into `main`; simply reading README on `main` misses adaptive/visitor features. The latest branch HEAD is **not** a newer app deployment; the successful Railway app SHA is pinned to `87beafb281a0`. A public portfolio may describe the deployed SHA accurately while keeping its private source untouched.

## Go-to-market risk register

| Risk | Status | Consequence |
|---|---|---|
| Self-serve billing and enterprise provisioning | **Not shipped** | Not yet an autonomous paid HR platform |
| Connector market breadth | **Three bounded adapters** | Not comparable to Rippling's 650+ integration marketplace |
| Customer-source-of-truth write-back | **Deliberately absent** | Manual coordination is required for HRIS/ATS changes |
| Generic vendor OAuth/inbound webhook standards | **Not shipped** | Integration onboarding needs customer credentials or source-specific adapters |
| Enterprise SSO/SCIM | **Not shipped** | Enterprise procurement/readiness gap |
| Real visitor behavior and external-scale SLA | **Not established** | Synthetic verification is not measured market adoption |
| Draft PR vs deployed branch divergence | **Verified** | Requires deliberate release-management reconciliation |

[Portfolio](README.md) · [Detailed capabilities](FEATURE-MATRIX.md) · [Research methodology](METHODOLOGY.md)


## User-supplied visual evidence (November 14, 2026)

Five genuine screenshots of the running Rivet interface were supplied by the project owner for this portfolio update. They show Overview, Employee Journeys, Workflows, Visitor Intelligence Summary, and Navigation Paths. Public versions are redacted and can be reviewed in [SCREENSHOTS.md](SCREENSHOTS.md); they are **not independently recaptured or functionally re-tested** by this report. The designed composite in the portfolio is illustrative, not unaltered evidence.
