
# Governance Plan · Realtime Quiz

## 1. Stage gates

The Realtime Quiz project uses a hybrid life cycle with four formal stage gates. The sponsor controls the project through measurable evidence at each gate. The project manager prepares the evidence and recommends whether the project should continue.

### G1 · Project plan approval · Week 3 · 2026-10-19

- [ ] Project charter is signed by the Head of IT (evidence: approved project charter).
- [ ] All 8 Must requirements are baselined (evidence: `lab02/moscow-list.md`).
- [ ] Work Breakdown Structure is completed to level 2 (evidence: WBS document).
- [ ] Four consecutive 14-day sprints and the week 14 pilot are included in the approved schedule (evidence: `lab03/life-cycle.mmd`).
- [ ] Risk register contains at least 5 identified risks, each with an owner and mitigation (evidence: risk register).

**Inputs:** Project charter, stakeholder register, MoSCoW list, WBS, project schedule and risk register.

**Decision maker:** Sponsor (Head of IT), supported by the Project Manager.

**Outcomes:** Continue / Continue with changes / Stop / Repeat.

### G2 · MVP checkpoint · Week 7 · 2026-11-16

- [ ] A complete quiz round supports joining, answering and scoring with at least 10 test players (evidence: sprint review demonstration and test report).
- [ ] At least 4 of the 8 Must requirements are accepted (evidence: updated Product Backlog and acceptance records).
- [ ] User registration, authentication and role-based access tests pass (evidence: automated test report).
- [ ] Data Protection Officer has reviewed the personal data collection list (evidence: signed data protection review).
- [ ] No open critical defect blocks the MVP demonstration (evidence: issue tracker).

**Inputs:** Sprint 1 and 2 review notes, accepted backlog items, automated test reports, defect list and data protection review.

**Decision maker:** Sponsor (Head of IT), supported by the Project Manager.

**Outcomes:** Continue / Continue with changes / Stop / Repeat.

### G3 · Feature complete · Week 11 · 2026-12-14

- [ ] All 8 Must requirements are accepted (evidence: Product Backlog acceptance records).
- [ ] Load test completes with 50 simulated players (evidence: load test report).
- [ ] At least 95% of answers are displayed within 2 seconds (evidence: load test performance results).
- [ ] Zero open critical security findings remain (evidence: security checklist signed by the security team).
- [ ] All new service code has at least 80% line coverage (evidence: JaCoCo CI report).

**Inputs:** Sprint 3 and 4 review notes, Product Backlog, CI reports, load test results and security review.

**Decision maker:** Sponsor (Head of IT), supported by the Project Manager and Security Team.

**Outcomes:** Continue / Continue with changes / Stop / Repeat.

### G4 · Pilot result and release decision · Week 14 · 2027-01-04

- [ ] Pilot has been completed with 50 students (evidence: pilot attendance and test records).
- [ ] At least 80% of pilot quiz sessions finish without a crash (evidence: pilot monitoring report).
- [ ] Zero open critical defects remain (evidence: final defect report).
- [ ] IT Operations has accepted the application handover documentation (evidence: signed handover record).
- [ ] Final sponsor acceptance and release decision are recorded (evidence: signed acceptance report).

**Inputs:** Pilot results, final test report, defect report, security checklist, deployment documentation and handover record.

**Decision maker:** Sponsor (Head of IT), supported by IT Operations and the Project Manager.

**Outcomes:** Continue / Continue with changes / Stop / Repeat.

---

## 2. Tolerances (Manage by Exception)

The project manager monitors schedule, effort, scope, quality and risk throughout the four stages.

The approved effort baseline is 490 hours. The four-student team's theoretical maximum capacity is 560 hours (4 × 10 hours × 14 weeks). The additional capacity is not automatic permission to increase the approved effort.

| Area         | Stage 1 (W1-3)                                                      | Stage 2 (W4-7)                                          | Stage 3 (W8-11)                                                                                     | Stage 4 (W12-14)                                                   |
| ------------ | ------------------------------------------------------------------- | ------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| Time         | Up to 5 working days delay                                          | Up to 3 working days delay                              | Up to 2 working days delay                                                                          | 0 days delay to the pilot date                                     |
| Cost (hours) | Up to 10% above stage effort baseline                               | Up to 10% above stage effort baseline                   | Up to 5% above stage effort baseline                                                                | 0% overrun; no overtime during pilot                               |
| Scope        | 8 Must requirements baselined; 0 unapproved changes                 | 8 Musts retained; at most 2 approved Should items added | All 8 Musts retained; no unapproved Must changes                                                    | No new features; only agreed release fixes                         |
| Quality      | Build passes; all planned charter and requirement reviews completed | 100% critical authentication and quiz-round tests pass  | At least 80% service-code coverage; 95% of answers displayed within 2 seconds in the 50-player test | At least 80% crash-free pilot sessions; zero open critical defects |
| Risk         | At most 3 high risks without an active mitigation                   | At most 2 high risks without an active mitigation       | At most 1 high risk without an active mitigation                                                    | 0 unresolved critical risks affecting the pilot                    |

### Escalation path

Developers → Scrum Master → Project Manager → Sponsor.

1. Developers identify a deviation and inform the Scrum Master.
2. The Scrum Master checks whether the team can resolve it within the sprint.
3. If the deviation exceeds the agreed tolerance, the Project Manager assesses its impact on schedule, effort, scope, quality and risk.
4. The Project Manager prepares an exception report and submits it to the sponsor.
5. The sponsor decides whether to continue, continue with changes, stop or repeat the relevant stage.

**Exception trigger:** An exception report is required whenever an actual or forecast result is expected to exceed any agreed tolerance, or when a critical security, data protection or operational issue threatens a phase gate or the week 14 pilot. The team must not silently change the approved baseline.

---

## 3. Reporting

### Weekly highlight report

The Project Manager prepares one highlight report every Friday and shares it with the sponsor and project team.

The report should be no longer than one page and contain four headings:

| Heading          | Information required                                                           |
| ---------------- | ------------------------------------------------------------------------------ |
| Done             | Completed activities, accepted requirements and measurable results             |
| Next             | Planned activities and upcoming milestones for the following week              |
| Risks            | Current risks, their impact, owners and mitigation actions                     |
| Tolerance status | Actual time, effort, scope, quality and risk compared with approved tolerances |

### Sprint review

A sprint review takes place at the end of each 14-day sprint. The Developers demonstrate the working increment to the Product Owner, Project Manager and relevant stakeholders. The sponsor is invited to review progress and provide feedback.

The Project Manager uses the sprint review to check progress against the approved project plan, identify risks and prepare evidence for the next stage gate.

### Exception report

An exception report is submitted to the sponsor when a tolerance is forecast to be exceeded.

The report uses three main lines:

1. **Deviation:** Describe the current or forecast problem, its impact and the tolerance exceeded.
2. **Options:** List possible corrective actions, including their effect on time, effort, scope, quality and risk.
3. **Recommendation:** State the recommended action and the decision required from the sponsor.

---

## 4. Closure criteria

The project can close only when the sponsor has accepted the pilot results, IT Operations has accepted the handover, lessons learned have been documented and administrative work is completed.

| Area                   | Criterion                                                                                                                                                 | Verified by          | Owner           |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------- | --------------- |
| Acceptance             | Pilot completed with 50 students, at least 80% of sessions finished without a crash, and zero open critical defects. Sponsor acceptance is documented.    | Sponsor (Head of IT) | Product Owner   |
| Hand-over              | Source-code repository, VPS credentials transferred securely to IT Operations, deployment instructions and an operational runbook delivered and accepted. | IT Operations        | Developers      |
| Lessons learned        | All sprint retrospective records and the final closure workshop are documented. Improvement actions have owners and follow-up status.                     | Project Manager      | Scrum Master    |
| Administrative closure | Final effort and budget records completed, project documentation archived, outstanding issues recorded and closure approval signed.                       | Sponsor (Head of IT) | Project Manager |

### Final closure approval

The Project Manager prepares the final closure report containing:

- Final project deliverables and acceptance status.
- Actual effort and financial expenditure compared with the approved baselines.
- Remaining defects, risks and known limitations.
- Handover confirmation from IT Operations.
- Lessons learned from all sprint retrospectives and the closure workshop.

The sponsor reviews the closure report and provides final approval. The project is considered formally closed only after this approval is recorded.
