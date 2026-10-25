# Workflow audit — 2026-10-25

## Evidence and scope

Read-only comparison of current repository documentation and existing local references. This is not a runtime certification of Caronte hooks, existing Braundin automations or code quality.

| Reference | Revision inspected | Observation |
| --- | --- | --- |
| Braundin workflow and skill catalog | main at `011b8547dff7bc0c570eb2a032c47a38f277ec3b` | Context, acceptance, plans, issues, checkpoints and verification already exist |
| Caronte README | dev at `2a37310e7d0d9bd9d30b51e712b9a0574e91d0d0` | Current documented runtime is Claude Code; work tracking uses Linear and API wrappers |
| Earlier local Caronte study | `6f9171d82e75a4ab6996b8cb0990d82d3c885ae6` | Historical reference only; not the current runtime |
| GitHub Spec Kit | v1.2.3, `5ea8b1cf0a38699340a38e00d02770308997d8c0` | Selected public upstream for feature artifacts and agent integration |

## Composition decisions

| Concern | Keep as a concept | Adapt for this portfolio |
| --- | --- | --- |
| Context recovery | Project context and evidence-backed checkpoints | One package per feature; current GitHub issue and observed commit |
| Specification | Observable behavior and acceptance criteria | Spec Kit feature directories, distinct from technical plans |
| Planning | Dependencies, files/contracts and checks | Small PR-sized tasks with stable IDs |
| Tracking | A single task source of truth | GitHub Issues, not Linear or a second editable Markdown board |
| Execution | Bounded work and explicit handoffs | Independent apps/branches; no shared runtime dependency |
| Review | Verify findings and acceptance evidence | Tests appropriate to risk; separate review from deployment |
| Branch controls | Respect project policy | Feature branches to main after bootstrap; no inherited dev/staging/prod topology |
| Automation | Reproducible checks | Begin with transparent CI; no automatic merges or silent branch deletion |
| Skills | Narrow activation and portable context | One Spec Kit command family; avoid installing overlapping Braundin/Caronte skills |

SDD here means **spec-driven development**. Caronte's subagent-driven development is a separate execution technique; it can implement a spec but does not replace it.

No private source code, hooks, prompt text or customer material has been copied into these repositories. The conclusions above are a new summary. Braundin's mandatory colleague review applies to Braundin; the personal portfolio must state its own review policy.

## Public references

- [Spec Kit pinned source](https://github.com/github/spec-kit/tree/v1.2.3)
- [SDD quickstart](https://github.github.com/spec-kit/quickstart.html)
- [Installation](https://github.github.com/spec-kit/installation.html)
- [Codex integration](https://github.github.com/spec-kit/integrations/codex.html)

Private repositories were consulted with the owner's existing access. Their detailed contents remain outside the portfolio repositories.
