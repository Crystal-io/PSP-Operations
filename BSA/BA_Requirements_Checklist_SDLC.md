# BA Requirements Checklist (SDLC) — GitHub-ready

Use this as a **PR/analysis gate** to ensure requirements are complete before design/dev/test/release.

Legend:
- **Stage**: where this type is typically finalized (can start earlier)
- **Priority**: 🔴 Critical / 🟠 High / 🟡 Medium
- **Fill (what to write)**: concrete content checklist

---

## Checklist table

| # | Requirement type | Stage (SDLC) | Priority | Fill (what to write) |
|---:|---|---|---|---|
| 1 | **Business requirements** | Discovery / Initiation | 🔴 | Business goal; problem statement; target users/segment; value hypothesis; KPIs & success metrics; scope / out of scope; business constraints; risks; definition of done for business |
| 2 | **Stakeholder & user requirements** | Discovery | 🔴 | Stakeholder map; roles/personas; needs & pain points; expectations; high-level scenarios; conflicts/assumptions; glossary (domain terms) |
| 3 | **Constraints & assumptions** | Discovery | 🔴 | Constraints (time/budget/legal/legacy/vendor); assumptions; dependencies; what is **not** changing; impact if assumption fails; mitigation/decision log links |
| 4 | **Functional requirements (FR)** | Analysis | 🔴 | Use cases / user stories; main flow; alternative flows; error flows; business rules; validations; state model (statuses + transitions); permissions by role; notifications/events; audit needs |
| 5 | **Non-functional requirements (NFR)** | Analysis / Design | 🔴 | Performance (SLA/latency/throughput); availability; reliability; scalability; security baseline; privacy; logging/monitoring; maintainability; compatibility; localization/timezones (if needed) |
| 6 | **Data requirements** | Analysis / Design | 🟠 | Entities & attributes; mandatory/optional fields; data sources (SoT); validation rules; retention; masking/encryption; data quality rules; export/reporting needs; data lineage (where used) |
| 7 | **Integration requirements** | Design | 🟠 | Systems list; API contracts; auth method; request/response schema; webhooks/callbacks; idempotency rules; timeouts; retries/backoff; rate limits; error catalog; reconciliation approach; sandbox/prod differences |
| 8 | **Technical / system requirements** | Design | 🟠 | Architecture constraints; tech stack constraints; deployment model; environments; config management; versioning; migration strategy; observability (metrics/traces); feature flags; backward compatibility; DR/backup (if relevant) |
| 9 | **Regulatory / compliance requirements** | Discovery / Design | 🔴* | Applicable regulations; required checks (KYC/AML/PCI/GDPR…); audit trail; consent; reporting obligations; data residency; access control; retention per policy; evidence/logging requirements |
| 10 | **UX/UI requirements** | Design | 🟡 | Screen list; navigation; input rules; validation messages; empty/error states; accessibility; responsiveness; content/copy rules; localization; design references (Figma links) |
| 11 | **Acceptance criteria (AC)** | Analysis / Dev | 🔴 | Given/When/Then; positive & negative cases; edge cases; measurable outcomes; data setup/fixtures; acceptance by role (who signs off); NFR acceptance thresholds (link to NFR) |
| 12 | **Test requirements / scenarios** | Testing prep | 🟠 | Test scenarios per flow; boundary cases; integration tests; contract tests; regression scope; test data; mocking strategy; traceability to FR/AC |
| 13 | **Operational requirements** | Release | 🟠 | Monitoring/alerts; runbooks; support & escalation; incident playbooks; rollback plan; SLA/SLOs; access management; log retention; on-call responsibilities |
| 14 | **Post-launch improvement requirements** | Post-Release | 🟡 | Metrics dashboard; user feedback channels; known limitations; backlog items; experiment plan; A/B or feature adoption tracking; improvement KPIs |

\* 🔴 if regulated domain; otherwise can be 🟠/🟡.

---

## Quick “Go/No-Go” gate (copy into PR)

- [ ] #1 Business requirements documented and agreed
- [ ] #3 Constraints & assumptions captured (with owners)
- [ ] #4 FR complete for MVP scope (incl. error flows)
- [ ] #5 NFR defined with measurable thresholds
- [ ] #7 Integrations have contracts + error/retry/idempotency defined
- [ ] #11 Acceptance criteria written for all key stories/use cases
- [ ] #12 Test scenarios drafted and traceable to FR/AC
- [ ] #13 Ops readiness (monitoring/rollback/runbook) covered for release

---

## Traceability suggestion (lightweight)

Recommended mapping:
- BRD: #1–#3 (+ #9 if needed)
- SRS/FRD: #4–#8, #10–#11
- Test pack: #11–#12
- Release pack: #13
- Post-launch: #14
