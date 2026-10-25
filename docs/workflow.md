# Development workflow v1 — draft

1. **Resume:** read repository instructions, constitution, issue, feature spec and checkpoint. Inspect branch, status and HEAD. Verify already-completed work before repeating it.
2. **Specify:** describe user outcomes, exclusions, acceptance IDs and negative cases in `specs/<id>-<feature>/spec.md`. Resolve consequential unknowns with Manuel.
3. **Plan:** write architecture, data/API contracts, dependencies, ADRs and validation in `plan.md`. Use the constitution as a live constraint. Select infrastructure only as required by the spec.
4. **Tasks:** break the plan into bounded changes in `tasks.md`, with dependencies and acceptance IDs. Issues track progress; the file records the intended decomposition and issue links.
5. **Analyze:** check that each requirement has a planned implementation and meaningful verification. Resolve conflicting artifacts before dependent work.
6. **Implement:** one coherent change per PR. Each agent receives a repository, scope and contract. Preserve unrelated work. Do not implement unapproved initial MVP scope.
7. **Verify and review:** reproduce the user flow and negative cases; inspect the diff. Record evidence and limitations. Compare implementation to spec and add only demonstrated missing work.
8. **Release and handoff:** check CI, deployment and post-deploy flow separately. Update docs and checkpoint; close the issue only when its acceptance criteria are satisfied.

## Artifact layout

```text
.specify/memory/constitution.md
specs/001-feature/{spec.md,plan.md,tasks.md}
docs/adr/0001-decision.md
docs/checkpoints/YYYY-MM-DD-topic.md
```

Spec Kit provides feature scaffolding and analysis; GitHub Issues/PRs provide tracking and review. We retain explicit release evidence beyond the generation workflow. See [tool setup](spec-kit.md) for exact installation and active-feature handling.

## Minimal work brief

Include issue URL, approved spec revision, acceptance IDs, branch/base, files or interfaces owned, dependencies, expected verification and stop conditions. Parallel tasks may overlap only through reviewed contracts, not concurrent edits to the same files.

## Exceptions

A narrow bug fix can use reproduction, cause, change and regression evidence in the issue. Documentation-only changes need link/content checks, not invented application tests. Existing authorization remains valid within its scope. Record new decisions only when behavior, cost, data exposure or acceptance changes materially.
