# Rivet — Four-Platform Competitive Feature Comparison
**Current vendor positioning checked November 13, 2026.** Rivet compared with **Rippling, HiBob, BambooHR and Moxo**.

> **Positioning:** Rivet is a vendor-neutral execution/identity ledger layered above an ATS/HRIS. It is neither a new payroll provider nor a complete HCM platform. Moxo is the closest *orchestration* comparison; Rippling, HiBob and BambooHR are stronger *systems of record*.

## Interpretation and evidence standard

- **Rivet: Yes** means current source implements that category; live customer/provider readiness is a separate question.
- **Y** means competitor explicitly publishes a broadly comparable category; **R** means relevant capability but exact equivalence is unverified; **?** means not confirmed from the current public page (never an absence claim).
- **Not shipped** refers solely to the Rivet repository, not a claim about the other platforms.
- Competitor marketing documentation is not private code inspection, a security assessment, price quotation or a hands-on benchmark.

## Executive findings (65 decision points)

| Decision | Rivet | Competitor position |
|---|---|---|
| People data authority | Orchestration/ledger over existing records | Rippling, HiBob and BambooHR hold native employee records |
| Human workflow control | Explicit owner publication, approvals, exceptions and durable runs | **All four** offer approvals/workflows; Moxo is especially strong at AI-plus-human cross-organization execution |
| Identity review | Explicit source matching and non-destructive email-drift handling | Others have employee identity and integrations; exact identical matching semantics not established |
| Connector breadth | Three implemented credential-based adapters | Rippling and HiBob have much broader published integration ecosystems; Moxo has REST/webhook/MCP support |
| IT/payroll capabilities | Not implemented | Rippling strongest in integrated devices/provisioning/payroll; HiBob/BambooHR payroll also available in their supported markets |
| Customer delivery readiness | Deployed application, recorded tests, missing billing/SSO | Competitors have established commercial platforms and wider implementation support |

## Side-by-side: every decision

| # | Group | Capability / decision | **Rivet** | **Rippling** | **HiBob** | **BambooHR** | **Moxo** | Verified interpretation |
|---:|---|---|---|:-:|:-:|:-:|:-:|---|
| 1 | Positioning | Source-of-record HR platform | **No** | Y | Y | Y | No | Rivet and Moxo can sit above systems; Rippling, HiBob, BambooHR maintain employee records |
| 2 | Positioning | Vendor-neutral people-ops orchestration | **Yes** | R | R | R | Y | Moxo is the closest architectural competitor; others also automate integrated processes |
| 3 | Positioning | Employee record as sole primary authority | **No** | Y | Y | Y | R | Rivet deliberately does not replace source records |
| 4 | Core workflows | Onboarding workflows | **Yes** | Y | Y | Y | Y | Category tie |
| 5 | Core workflows | Offboarding workflows | **Yes** | Y | Y | Y | Y | Category tie |
| 6 | Core workflows | Role or employment transitions | **Yes** | Y | Y | Y | Y | Category tie |
| 7 | Core workflows | Leave/return process templates | **Yes** | Y | Y | Y | R | Rivet implementation; HRIS platforms have broader leave management |
| 8 | Core workflows | Editable workflow definitions | **Yes** | Y | Y | Y | Y | Category tie |
| 9 | Core workflows | Workflow draft/publish separation | **Yes** | R | R | R | Y | Source shows explicit Rivet publish gate; Moxo versions/publishes templates |
| 10 | Core workflows | Launch against named person | **Yes** | Y | Y | Y | Y | Broad category tie |
| 11 | Core workflows | Frozen run version / immutability | **Yes** | ? | ? | ? | R | Strong source control; competitor exact state model not tested |
| 12 | Core workflows | Durable per-step outcome ledger | **Yes** | Y | Y | Y | Y | All document workflow histories in broad terms |
| 13 | Core workflows | Pause and resume running work | **Yes** | R | R | R | R | Specific execution semantics not independently compared |
| 14 | Human governance | Manual approval of consequential steps | **Yes** | Y | Y | Y | Y | Not exclusive: Moxo is especially strong |
| 15 | Human governance | Approval prerequisite for offboarding/role change | **Yes** | R | R | R | Y | Rivet fail-closed dependency is source-specific |
| 16 | Human governance | Owner-only publish control | **Yes** | Y | Y | Y | Y | Category tie in role permissions |
| 17 | Human governance | Named actor on completed work | **Yes** | Y | Y | Y | Y | Audit/approval category standard |
| 18 | Human governance | Exception owner/severity/reason | **Yes** | R | R | R | Y | Moxo has explicit exception escalation and audit records |
| 19 | Human governance | Exception resolution event history | **Yes** | R | R | R | Y | Specific details not benchmarked |
| 20 | Human governance | Approve AI-proposed content before use | **Yes** | Y | Y | R | Y | Competitor AI assistance also involves governance |
| 21 | Identity | Staged external identity import | **Yes** | R | R | R | R | Source-mapped; peers have integrations and imports |
| 22 | Identity | Human chooses link/create/ignore | **Yes** | ? | ? | ? | ? | Rivet explicit non-destructive reconciliation design |
| 23 | Identity | Detect drift after email change | **Yes** | ? | ? | ? | ? | Cannot verify identical competitor rule from public materials |
| 24 | Identity | Reject duplicate source-to-person linking | **Yes** | ? | ? | ? | ? | Do not infer competitors lack collision protections |
| 25 | Identity | Keep separate stable source IDs | **Yes** | Y | R | R | R | Identity federation techniques differ by platform |
| 26 | Identity | Native employee directory + org chart | **No** | Y | Y | Y | R | HRIS systems lead by scope; Rivet has linked people list |
| 27 | Adaptive | Task/content/form/acknowledgment modules | **Yes** | Y | Y | Y | Y | Broad workflows supported by peers |
| 28 | Adaptive | Explicit dependency graph and cycle detection | **Yes** | R | R | R | Y | Specific Rivet validation; Moxo supports complex flow logic |
| 29 | Adaptive | Conditional branches from stored context | **Yes** | Y | Y | R | Y | Broad conditional automation |
| 30 | Adaptive | Owner/manager/IT/HR assignments | **Yes** | Y | Y | Y | Y | Category tie |
| 31 | Adaptive | Timezone-aware relative scheduling | **Yes** | R | R | R | Y | Exact DST rules not benchmarked |
| 32 | Adaptive | Participant-only expiring access link | **Yes** | ? | ? | ? | Y | Moxo externally accessible approval links |
| 33 | Adaptive | Owner revokes participant access | **Yes** | R | R | R | Y | Rivet capability token model differs from external portals |
| 34 | Adaptive | Scoped candidate.hired signed event ingress | **Yes — narrow** | R | R | R | Y | Specific HMAC intake exists; general vendor webhooks not shipped |
| 35 | Adaptive | Identity review before event-triggered launch | **Yes** | R | R | R | Y | No automatic identity merge or launch from candidate event |
| 36 | Adaptive | Durable reminder queue / unknown outcome | **Yes — provider dependent** | Y | Y | Y | Y | Provider-acceptance distinct from message delivery |
| 37 | Integrations | Slack user-directory read sync | **Yes — configured** | Y | Y | R | Y | Native integration breadth varies; Rivet uses customer bot token |
| 38 | Integrations | Ashby candidate read sync | **Yes — configured** | R | R | R | R | Customer API key; not a universal ATS connector |
| 39 | Integrations | BambooHR employee-directory read sync | **Yes — configured** | R | R | Y | R | Customer directory permissions may hide employees |
| 40 | Integrations | Outbound Slack message on owner approval | **Yes — configured** | Y | R | R | Y | Exact text/channel approved in Rivet |
| 41 | Integrations | General native OAuth connector setup | **Not shipped** | Y | Y | Y | Y | Competitors lead on integration breadth |
| 42 | Integrations | General inbound HRIS/ATS vendor webhooks | **Not shipped** | Y | R | Y | Y | Narrow candidate.hired source is not generic vendor ingress |
| 43 | Integrations | Automatic HRIS/ATS record write-back | **Not shipped** | Y | Y | Y | Y | Rivet intentionally read-only for HRIS/ATS |
| 44 | Integrations | Broad integration marketplace | **Not shipped** | Y | Y | Y | Y | Rippling advertises 650+ integrations |
| 45 | Integrations | Remote app account provisioning | **Not shipped** | Y | R | R | R | Rippling strength; Moxo can coordinate provider actions |
| 46 | Integrations | Automated device shipping/management | **Not shipped** | Y | R | R | R | Rippling native device capability |
| 47 | Integrations | Interactive Slack approval controls | **Not shipped** | R | R | R | R | Separate owner-approved Rivet send exists |
| 48 | AI | AI-suggested workflow structures | **Yes — configured** | Y | Y | R | Y | AI is not a Rivet-exclusive function |
| 49 | AI | Structured draft schema validation | **Yes** | R | R | R | R | Rivet source-evidenced; exact peer internals not accessible |
| 50 | AI | Human editing before publication | **Yes** | Y | Y | R | Y | Moxo and others support review |
| 51 | AI | Assistant automatically provisions accounts | **No** | Y | R | R | Y | Rivet AI stays in proposal/approval lane |
| 52 | Reporting | Operational completion/overdue counts | **Yes** | Y | Y | Y | Y | Category tie |
| 53 | Reporting | Saved lifecycle audit history | **Yes** | Y | Y | Y | Y | Category tie |
| 54 | Reporting | Baseline effort estimate (not measured savings) | **Yes — labeled** | R | R | R | R | Source is explicit about estimate limitations |
| 55 | Reporting | Visitor Intelligence private admin suite | **Yes — private** | R | R | R | R | Separate from people analytics; 14 views verified with synthetic traffic |
| 56 | Reporting | First-party opt-in visitor analytics | **Yes** | ? | ? | ? | ? | Not a basis to claim rivals cannot do consented web analytics |
| 57 | Reporting | Live replay or heatmaps | **Disabled** | ? | ? | ? | ? | Intentionally off; not a released product feature |
| 58 | Reporting | Pseudonymous browser deletion and withdrawal | **Yes** | ? | ? | ? | ? | Specific consent-engineering implementation |
| 59 | Platform | Hosted multi-tenant isolation | **Yes** | Y | Y | Y | Y | Category tie |
| 60 | Platform | PostgreSQL RLS for personnel workspaces | **Yes** | ? | ? | ? | ? | Specific architecture not competitor-verified |
| 61 | Platform | Enterprise SSO / SCIM | **Not shipped** | Y | Y | Y | Y | Commercial enterprise readiness gap |
| 62 | Platform | Native payroll | **Not shipped** | Y | Y | Y | No | HiBob native U.S./U.K.; BambooHR U.S. add-on |
| 63 | Platform | Commercial subscription billing | **Not shipped** | Y | Y | Y | Y | Rivet not marketed as a paid checkout-ready service |
| 64 | Platform | External multi-party process portals | **Limited participant links** | R | R | R | Y | Moxo materially stronger in client/vendor portals |
| 65 | Platform | Live end-to-end customer connector certification | **Unverified** | ? | ? | ? | ? | Fixture contract tests are not a real customer connector acceptance test |

## Five judgments an employer or customer can use

**Rivet lead (specific architecture, not proven marketplace superiority):** Explicit identity review without silent overwriting; versioned workflow execution records; scoped participant actions; conservative Slack outcome handling; a fully source-visible owner-publish gate.

**Tie / broadly available capability:** Human approval, onboarding/offboarding workflows, audit logs, people data, automated reminders, AI assistance and reports exist across the market. No claim of category exclusivity is supportable.

**Competitors' documented leads:** Rippling's HR/IT/payroll and device breadth; HiBob's native HRIS, U.S./U.K. payroll and agent suite; BambooHR's mature onboarding paperwork and U.S. payroll add-on; Moxo's sophisticated human/AI workflows, external stakeholders and process integrations.

**Rivet development gaps:** Generic OAuth connections, general inbound vendor webhooks, write-back, broad marketplace, enterprise identity, checkout, employee accounts and remote provisioning.

## Sources — official vendor publications

- [Rippling ecosystem and 650+ integrations](https://www.rippling.com/products)
- [Rippling Workflow Studio](https://www.rippling.com/products/it/platform/workflows)
- [HiBob workflows](https://www.hibob.com/platform/core/automation/)
- [HiBob AI agents](https://www.hibob.com/platform/core/ai/agents/)
- [HiBob payroll and integrations FAQ](https://www.hibob.com/faq/)
- [BambooHR pricing and U.S. payroll](https://www.bamboohr.com/pricing/)
- [BambooHR onboarding and e-sign](https://www.bamboohr.com/platform/onboarding/)
- [Moxo process orchestration](https://www.moxo.com/business-process-management)
- [Moxo AI/human approval operations](https://www.moxo.com/workflow/approvals)
- [Moxo official service features](https://www.moxo.com/legal/description-of-services)

**Rivet source:** private `https://github.com/Amishgangsta/Rivet` feature branch, deployed commit `87beafb281a0f6bdc66674b0dfb1af1235c5cf9b`; read [Methodology](METHODOLOGY.md) and [Verification](VERIFICATION-AND-STATUS.md).

**Scope:** not independently tested Rivet-to-vendor account integration, enterprise benchmarking, vendor commercial prices or exact per-feature rival behavior.
