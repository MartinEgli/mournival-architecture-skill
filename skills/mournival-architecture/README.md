# Mournival Architecture

Single skill for architecture governance reviews through four steward
perspectives.

## Roles

- Architecture Decision Steward: keeps the system actionable.
- Architecture Risk Steward: protects against harmful consequences.
- Architecture Value Steward: makes outcomes usable.
- Architecture Assurance Steward: protects evidence and traceability.

## How Roles Work Together

Use `references/role-collaboration.md` for the full process.

- Assurance checks evidence, traceability, source binding, and overstatement
  first.
- Risk reviews material harm, misuse, compliance, security, semantic drift, and
  human-review triggers.
- Value checks whether the artifact is understandable, useful, and actionable
  without weakening evidence or hiding risk.
- Decision consolidates the result into allowed next steps, blocked next steps,
  required actions, and final status.

Decision must not override Assurance or Risk vetoes. If roles disagree, preserve
the disagreement and let the stricter evidence or risk position determine
productive-use status.

## Review Order

Internal evaluation:

1. Assurance
2. Risk
3. Value
4. Decision

Output order:

1. Decision Steward Review
2. Risk Steward Review
3. Value Steward Review
4. Assurance Steward Review
5. Consolidated Mournival Decision

## Modes

- `/mournival review-claim`
- `/mournival review-dirty-information`
- `/mournival review-contradiction`
- `/mournival review-artifact`
- `/mournival final-check`
- `/mournival clean-ai`
- `/mournival diagram`

## Diagrams

Use `/mournival diagram` for governance diagrams only: evidence traceability,
role finding flow, decision flow, veto maps, review states, and productive-use
gates in Mermaid or PlantUML.
