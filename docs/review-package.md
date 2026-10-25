# Initial approval package

Status: ready for Manuel's review; approval pending.

The original roadmap requires constitution approval before using the first feature to validate the workflow. The following proposals make that decision concrete:

1. **Constitution v1:** spec-first work, GitHub Issues/PRs, proportional checks, recoverable checkpoints and independent releases.
2. **TenantFlow scope:** signed-in users can create organizations, manage existing-user memberships as an owner, and manage projects under owner/admin/member/viewer RBAC. No billing, SSO or invitation email in v1.
3. **TenantFlow architecture proposal:** React/TypeScript + Node/TypeScript modular monolith with PostgreSQL; server membership checks and database row-level isolation as defense in depth. Identity provider selected in TF-00 before auth code.
4. **DocuMind scope:** owner-scoped PDF/text uploads, private storage, durable processing, bounded retries and visible extraction results. PDF text extraction only; OCR and chat are excluded. Local fake-provider mode is visibly distinct from the live AI path.
5. **DocuMind architecture proposal:** React + Go API/worker, PostgreSQL job table and S3-compatible object storage. Start with a database queue; defer a broker and QueueCore until evidence warrants them.

These implementation choices are proposed additions to the supplied roadmap. They are not claims about prior ChatGPT agreements.

The AI provider, identity provider, hosting and spending caps are pending implementation decisions; this package does not authorize paid resources. They do not prevent drafting contracts or reviewing scope.

Approval record: pending. Once approved, record the date, source and any revisions in `docs/governance.md` in each repository and proceed with TF-00/TF-01.
