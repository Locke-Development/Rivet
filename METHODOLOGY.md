# Rivet — Evidence and Competitive Comparison Method

**Prepared November 13, 2026. No new code changes, deployment, customer account operations, or production writes were made.**

## First-party Rivet evidence

- GitHub: [private Rivet repository](https://github.com/Amishgangsta/Rivet); deployed app SHA `87beafb281a0f6bdc66674b0dfb1af1235c5cf9b`, private feature-branch HEAD `d8c3cda80b10aa839127c5d0a0adc563457d13ba`. The former is the authoritative deployed application version, while the latter incorporates later documentation updates.
- Current source files: `README.md`, `server.mjs`, `operations-store.mjs`, `journey-store.mjs`, `journey-validation.mjs`, `journey-worker.mjs`, `lifecycle-store.mjs`, `connectors.mjs`, `openai-workflows.mjs`, `app/operations.js`, `app/adaptive.js`, `hosted/auth.mjs`, `hosted/migrations/001–004`, `app/visitor-intelligence.js`.
- Release documentation: `docs/full-workspace.md`, `docs/connector-contracts.md`, `docs/visitor-intelligence-operator-guide.md`, `docs/verification/2026-10-26-visitor-intelligence.md`, `docs/handoffs/2026-10-26-visitor-intelligence-railway-release.md`, `docs/handoffs/2026-10-26-visitor-intelligence-live-access.md`.
- Railway: project Rivet; web and migrations services show successful October 26 deployed SHA `87beafb281a0f6bdc66674b0dfb1af1235c5cf9b`. GitHub PR #1 inspected as open/draft and unmerged.

## Competitor-owned primary sources, checked November 2026

| Vendor | Official material | What it confirms |
|---|---|---|
| Rippling | [Product ecosystem](https://www.rippling.com/products), [Workflow Studio](https://www.rippling.com/products/it/platform/workflows) | HRIS + IT + payroll + device management, automations and 650+ published integrations |
| HiBob | [Core automation](https://www.hibob.com/platform/core/automation/), [AI agents](https://www.hibob.com/platform/core/ai/agents/), [FAQ](https://www.hibob.com/faq/) | Role-aware workflows, AI contextual agents, integrations, native US/UK payroll |
| BambooHR | [Plan details](https://www.bamboohr.com/pricing/), [onboarding](https://www.bamboohr.com/platform/onboarding/) | HRIS, paperwork/onboarding/e-signatures, approval workflows, US payroll add-on |
| Moxo | [Business process management](https://www.moxo.com/business-process-management), [human approvals](https://www.moxo.com/workflow/approvals), [service description](https://www.moxo.com/legal/description-of-services) | AI/human orchestration, versioned flows, external portals, approvals/exceptions, integrations and audit |

## Comparison rules

- **Source-implemented:** the current Rivet code supports a behavior. This does not mean newly executed customer-facing production proof.
- **Source / configuration-dependent:** live vendor credentials, mail/AI service, role and entitlements affect operation. Fixture adapter tests cannot prove a real customer's API access.
- **Y:** competitor documents the broad functional category; **R:** related published feature, exact equivalence not established; **?:** not verified. `?` never means absent or worse.
- No ranking on legal/security compliance, productivity ROI, enterprise procurement success, price or performance was performed. No competing vendor customer account or private code was inspected.

## Claims deliberately excluded

- Rivet does not offer full native HRIS, payroll, automated IT provisioning, broad enterprise SSO, generic OAuth or commercial paid checkout.
- The signed `candidate.hired` ingress is **not** general signed vendor webhook ingestion.
- The site analytics `estimated devices` metric counts pseudonymous browser installations, not hardware devices. Estimated time is not verified attention.
- Baseline effort estimates multiply an entered assumption by completed work; they are **not independently measured hours or money saved**.
- A Railway SUCCESS state and recorded local tests do not constitute a fresh end-to-end customer integration, performance or security certification.

## Public/private boundary

This package contains **authored marketing text, evidence references, and an illustrative HTML architecture flow only**. It contains **no employee records, authenticated screenshots, code, connection credentials, internal visitor data, or proprietary HR process templates**. The private production repository was left unchanged.


## Screenshot provenance (November 14, 2026 update)

Five screenshots of the Rivet app were provided directly by the project owner in this conversation: People Operations Overview, Employee Journeys, Workflows, Visitor Intelligence Summary, and Visitor Intelligence Navigation Paths. Public archive images are redacted/cropped versions of these originals to protect account emails, participant details and private analytics. The additional five-screen collage was a generated *design composite using these screenshots as references*, not a literal pixel-identical screenshot. None represents a fresh authenticated capture taken by the reviewer. The existing recorded test/deployment claims are unchanged.
