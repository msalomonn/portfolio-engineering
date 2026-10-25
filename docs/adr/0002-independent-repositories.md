# ADR 0002: independent repositories

Status: accepted with the initial architecture approval. Date: 2026-10-25.


Context: The deadline should not couple the two application releases.
Options: one monorepo; separate apps plus an engineering reference repo; shared framework and runtime packages.
Proposed decision: portfolio-engineering owns shared policy/templates; tenantflow and documind own their complete app specifications, code, CI and deploy instructions. Governance snapshots are explicitly versioned.
Consequences: some setup duplication, but no cross-repo runtime or release dependency. Updates to policy require deliberate adoption.
Validation: each app must clone, configure, test and run without a sibling checkout when implemented.
Revisit: real shared behavior appears in both apps, or QueueCore becomes an independently useful project after Nov 16.
