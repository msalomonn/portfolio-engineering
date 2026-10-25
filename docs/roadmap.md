# Portfolio Engineering — roadmap

Source: Manuel's supplied ChatGPT plan, adopted as the execution baseline on 2026-10-25.
Dates use America/Mexico_City. Targets are tentative, not fixed commitments. Budget: 4–6 hours/day, 20–30 hours/week, 60–90 hours total. Parallel agents do not double the human review budget.

| Week | Dates | Outcome | Acceptance |
| --- | --- | --- | --- |
| 1 | Oct 26–30 | Engineering Workflow v1 | Three repositories, SDD workflow, constitution and two approved MVP packages |
| 2 | Nov 2–6 | Local MVPs | Both principal flows execute end-to-end locally; critical tests pass |
| 3 | Nov 9–13 | Portfolio Release v1 | Per-app CI green, demos, English documentation and deployed smoke evidence |

## Week 1 — foundations and a real validation slice

- Mon 26: review the Braundin/Caronte comparison and Engineering Constitution v1.
- Tue 27: approve MVP boundaries and core ADRs; validate Spec Kit setup; convert backlogs into issues.
- Wed 28: begin TenantFlow TF-01 (authenticated organization/project access with tenant isolation) after approval.
- Thu 29: verify negative isolation cases; refine workflow based on the actual diff and review.
- Fri 30: review Workflow v1 milestone, confirm DocuMind contracts and order the next implementation tasks.

Preparation completed on Oct 25 may bring these dates forward. Do not spend the whole week writing process documents.

## Week 2 — independent implementation

TenantFlow: authentication, organizations, memberships/RBAC and projects, with isolation verified on the server and database boundary.
DocuMind: upload, private storage, durable jobs, worker recovery, schema-validated AI extraction and visible status/results.
Use independent implementation branches and contracts. Integrate in small PRs; review daily. Prefer a thin working slice before broad feature coverage.

## Week 3 — hardening and publication

- Nov 9–10: integration/E2E negative cases, recovery checks and dependency analysis.
- Nov 11: deployment rehearsal, migrations, health checks and rollback/restore instructions.
- Nov 12: English READMEs, architecture diagrams, ADRs, screenshots, synthetic sample data and demo scripts.
- Nov 13: independent release review, public repository readiness and GitHub profile presentation.

## Capacity and scope control

Reserve approximately 25% of capacity for integration, review and unexpected fixes. Reduce optional scope before reducing security checks. TenantFlow excludes billing, enterprise SSO and invitation email. DocuMind excludes OCR, RAG/chat, arbitrary file formats and large-scale queue infrastructure.

If one application misses the date, publish the ready application and retain the other's honest status. Do not call a mocked extraction a live AI demo. QueueCore is a separate decision after Nov 16; first evaluate whether DocuMind's job subsystem provides a useful extraction boundary.
