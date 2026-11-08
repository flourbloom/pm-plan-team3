# Scrum setup · Realtime Quiz

## Roles

| Role            | Person       | Accountable for                                                                                                                                              | Not responsible for                                                                                                                     |
| --------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------- |
| Product owner   | Student A    | Maximizing product value, managing and prioritizing the Product Backlog, defining the Sprint Goal, and accepting completed backlog items                     | Dictating technical architecture, assigning daily tasks to developers, managing developer hours, or project budget governance           |
| Scrum master    | Student B    | Facilitating Scrum events, removing team impediments, coaching team in Scrum practices, and promoting continuous improvement                                 | Managing product backlog priorities, technical implementation decisions, accepting user stories, or project managerial authority        |
| Developers      | Students A-D | Creating the Sprint Backlog, delivering high-quality Done increments meeting the Definition of Done, executing technical design, and daily self-organization | Prioritizing business backlog items, external stakeholder management, phase gate sign-offs, or overall project financial accounting     |
| Project manager | Lecturer     | Phase gate reviews (G1-G4), hours and budget tracking (490 h / $200), stakeholder alignment, risk register, and formal academic governance                   | Daily sprint coordination, writing user story acceptance criteria, assigning user story point estimates, or micro-managing sprint tasks |
| Sponsor         | Head of IT   | Authorizing the project charter, allocating budget and VPS resources, evaluating milestone demos at phase gates, and strategic approval                      | Attending Daily Scrums, refining product backlog items, story-level sprint planning, or reviewing daily code commits                    |

When a Product Owner also develops code, a conflict of interest emerges between prioritizing high-value user stories and favoring technically appealing tasks or cutting quality to rush deliverables; we limit this by keeping the backlog ordering transparent for Scrum Master review and strictly enforcing automated Definition of Done checks that developers cannot bypass.

## Sprint goal (sprint 1, weeks 4-5)

Deliver the core project skeleton, authentication, and basic quiz creation so users can log in and author questions.

## Event calendar · sprint 1 (2026-10-20 to 2026-11-02)

| Event                | Date(s)              | Time  | Timebox | Attendees         | Output                                                    |
| -------------------- | -------------------- | ----- | ------- | ----------------- | --------------------------------------------------------- |
| Sprint planning      | Tue 2026-10-20       | 10:00 | 2 h     | PO, SM, devs      | sprint goal, sprint backlog                               |
| Daily scrum          | Mon-Fri 10-21..11-02 | 09:00 | 15 min  | devs (+SM)        | updated plan, impediment log                              |
| Backlog refinement   | Wed 2026-10-28       | 14:00 | 1 h     | PO, SM, devs      | refined stories meeting Definition of Ready               |
| Sprint review        | Mon 2026-11-02       | 14:00 | 1 h     | team, PM, sponsor | working increment demo, feedback, updated product backlog |
| Sprint retrospective | Mon 2026-11-02       | 15:30 | 1 h     | PO, SM, devs      | actionable process improvement plan                       |

## Definition of ready

1. **FR id:** The item is mapped to a valid functional requirement ID (e.g. FR-A1, FR-Q1) from the baselined MoSCoW catalog or documented as an agreed system architecture enabler.
2. **Acceptance criteria:** The item has clear, testable acceptance criteria written in Given/When/Then format covering key functional outcomes.
3. **Estimate:** The item has been estimated by the developers using Fibonacci story points (1, 2, 3, 5, 8) and is sized at 8 points or fewer so it fits within a single sprint.
4. **Dependencies:** All technical, architectural, and data dependencies are identified, documented, and confirmed unblocked before sprint commitment.
5. **Sketch:** Any story with user interaction includes an approved UI sketch, wireframe, or form field layout demonstrating the intended interface.

## Definition of done

1. The project compiles cleanly and `./mvnw clean verify` completes with zero errors or warnings in the CI pipeline (CI).
2. All unit and integration tests execute and pass with 100% green status on the CI pipeline (CI).
3. Line coverage of new service code is >= 80% in the JaCoCo report on the CI pipeline (CI).
4. Static code analysis via SpotBugs and Checkstyle passes with zero critical or high-severity warnings on the CI pipeline (CI).
5. Every pull request receives at least one approving peer review from another developer before merging into the main branch.
6. User-facing interfaces are demonstrated and verified on both a desktop (1920x1080) and a phone-sized (375x667) viewport without horizontal scroll or broken layout.
7. All Given/When/Then acceptance criteria specified in the backlog item are demonstrated and verified in a running environment.
8. API documentation, README setup instructions, and database migration scripts are updated and committed.
9. The application container builds successfully and starts in the staging environment with clean health check logs.

Planning velocity: 30 points · capacity: 4 x 10 h x 2 weeks = 80 h
