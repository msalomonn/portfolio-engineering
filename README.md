# Portfolio Engineering

Engineering workflow and architecture records for two independently deployable portfolio applications.

**Status:** foundation drafts prepared on October 25, 2026. Constitution and MVP approval pending. No application is deployed yet.

| Repository | Focus | Stack requested |
| --- | --- | --- |
| [TenantFlow](https://github.com/msalomonn/tenantflow) | Organizations, RBAC and multi-tenant projects | React + Node.js |
| [DocuMind](https://github.com/msalomonn/documind) | Document upload and asynchronous AI extraction | React + Go |
| This repository | Constitution, reusable workflow, ADRs and roadmap | Markdown + Spec Kit |

Start with the [constitution](.specify/memory/constitution.md), [roadmap](docs/roadmap.md), [workflow](docs/workflow.md) and [audit](docs/workflow-audit.md).

## Review package

- [Approval decisions](docs/review-package.md)
- [Architecture decision: workflow composition](docs/adr/0001-workflow-composition.md)
- [Architecture decision: independent repositories](docs/adr/0002-independent-repositories.md)
- [Reusable templates](templates/README.md)
- [Backlog](docs/backlog.md)
- [Spec Kit setup](docs/spec-kit.md)

The target release date is November 13, 2026, with 4–6 hours per weekday across both apps. Either app can release independently. QueueCore is deferred until a later iteration beginning no earlier than November 16.
