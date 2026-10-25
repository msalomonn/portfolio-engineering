# Initial approval package

Status: approved by Manuel on 2026-10-25 in the Codex conversation.

The original roadmap requires constitution approval before using the first feature to validate the workflow. The approved decisions are:

1. **Constitution v1:** spec-first work, GitHub Issues/PRs, proportional checks, recoverable checkpoints and independent releases.
2. **TenantFlow scope:** signed-in users can create organizations, manage existing-user memberships as an owner, and manage projects under owner/admin/member/viewer RBAC. No billing, SSO or invitation email in v1.
3. **TenantFlow architecture proposal:** React/TypeScript + Node/TypeScript modular monolith with PostgreSQL; server membership checks and database row-level isolation as defense in depth. Identity library selected in TF-00 before auth code (Better Auth; recorded in the TenantFlow ADR).
4. **DocuMind scope:** owner-scoped PDF/text uploads, private storage, durable processing, bounded retries and visible extraction results. PDF text extraction only; OCR and chat are excluded. Local fake-provider mode is visibly distinct from the live AI path.
5. **DocuMind architecture proposal:** React + Go API/worker, PostgreSQL job table and S3-compatible object storage. Start with a database queue; defer a broker and QueueCore until evidence warrants them.

These implementation choices extend the supplied roadmap and were approved in this Codex conversation. They are not claims about prior ChatGPT agreements.

The AI provider, hosting and spending caps remain pending implementation decisions; this package does not authorize paid resources. TenantFlow selected Better Auth during TF-00; see its identity ADR.

Approval recorded in `docs/governance.md` in all three repositories. Proceed with TF-00/TF-01.
