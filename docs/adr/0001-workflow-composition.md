# ADR 0001: workflow composition

Status: proposed. Date: 2026-10-25.


Context: The portfolio needs SDD without losing the existing ability to resume work and verify delivery.
Options: copy the complete private workflow; install multiple competing skill families; use one public scaffolder plus original project policy.
Proposed decision: pin Spec Kit 1.2.3, maintain an original constitution, and retain GitHub issue/PR and checkpoint conventions. Reuse concepts from prior work without redistributing private assets.
Consequences: fewer conflicting commands; policy and release checks remain our responsibility. Tool upgrades require an explicit diff and smoke test.
Validation: initialize the three repos, verify installed integration files, and use TF-01 as the first behavior-level pilot. Installation alone is not validation of agent behavior.
Revisit: command conflicts, repeated manual drift, or an upstream incompatible release.
