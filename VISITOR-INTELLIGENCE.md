# Rivet — Private Visitor Intelligence, Not Employee Surveillance

**Scope:** a separate, opt-in website/product visitor analytics system for an authorized *platform administrator*, rather than workspace operators or employees.

## What the code and recorded live tests establish

- Visitor identity is a **random pseudonymous browser-installation identifier**, not a detected physical device or reliably unique human.
- Before consent: no analytics identity/event; Accept and Decline are offered and Global Privacy Control is recognized.
- A separate platform-administrator grant is required. Being an owner of one Rivet workspace does **not** give access to all visitor reports.
- Authenticated owner and synthetic consenting-browser checks on October 26 reported 200 on the private dashboard, all **14 report views**, CSV and JSON exports, plus 401 for anonymous report/export access.
- Report categories include summary, sessions, visitors, testers, features, paths, funnel conversion, campaign/source attribution, structured feedback, opportunities and performance.
- Feature events exclude personnel form answers, AI prompts and responses, tokens, credentials and arbitrary URL payloads.
- Browser self-deletion and withdrawal were exercised in recorded synthetic tests. An internal browser was excluded from the default reporting totals.
- Replay and visual heatmaps remain **disabled**; no public demo mirror or recorder was installed.

## Retention and interpretation

Raw event retention defaults to **30 days**, summary facts to **90 days**. Engagement estimates are based on foreground interaction/heartbeat signals, *not verified attention*. A browser installation is not the same as a physical device; zero measured visits does not establish zero actual traffic because declining/GPC browsers and lost telemetry are outside the data.

The default funnel definitions cover arrival/access, first value, employee journey, AI draft review/acceptance, workflow publication/launch and integration connection. Conversion requires valid ordered evidence and a bounded window; *pending* or incomplete evidence is not claimed to be abandonment. Performance metrics are observations, not production SLAs.

## Recorded test vs current ongoing status

The October 26 handoff reports deployed backend/source and successful private synthetic browser/admin verification. **It does not verify genuine external visitor behavior, campaign attribution in a real marketing campaign, or concurrency stability at production traffic scale.** An earlier benchmark run intermittently missed a local p95 threshold despite a later passing run.

**Security and privacy:** analytics collection and deletion are outside the employee lifecycle database; no personal photos, private staff identifiers, or dashboard screenshots are included in this public-safe portfolio package.

Source evidence: `docs/visitor-intelligence-operator-guide.md`, `docs/verification/2026-10-26-visitor-intelligence.md`, `docs/handoffs/2026-10-26-visitor-intelligence-live-access.md`, feature-branch source at commit `d8c3cda80b10aa839127c5d0a0adc563457d13ba`.


## Public demonstration screenshots

The sanitized [Visitor Intelligence Summary](assets/visitor-intelligence-summary.png) and [Navigation Paths](assets/visitor-navigation-paths.png) images are genuine app screen captures supplied November 14, 2026. The audience counts, session identifiers and recorded paths were redacted from these public copies. See [SCREENSHOTS.md](SCREENSHOTS.md).
