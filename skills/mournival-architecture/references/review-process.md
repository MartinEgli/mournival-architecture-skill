# Review Process

Internal review order:

1. Assurance Steward checks whether the claim or artifact is supportable.
2. Risk Steward checks what can go wrong if it is used.
3. Value Steward checks whether the result is usable for the target audience.
4. Decision Steward turns analysis into a next step.

Output order:

1. Decision Steward Review
2. Risk Steward Review
3. Value Steward Review
4. Assurance Steward Review
5. Consolidated Mournival Decision
6. Required Actions
7. Blocked Next Steps
8. Allowed Next Steps

## Veto Strength

1. Assurance Steward: strongest veto for missing origin, evidence, or
   traceability.
2. Risk Steward: veto for high risk, unclear data classification, compliance
   risk, or severe misuse risk.
3. Decision Steward: veto for broken process, missing review, or non-approved
   pipeline state.
4. Value Steward: usually soft veto; hard veto only when the artifact is
   practically unusable for its intended purpose.

## Decision Status Values

- `accepted`
- `accepted_with_conditions`
- `blocked`
- `requires_human_review`
- `rejected`

## Risk Level Values

- `low`
- `medium`
- `high`
- `critical`

## Evidence Discipline

- Evidence must point to supplied material or verified sources.
- Inference must remain marked as inference.
- Assumptions must not become facts.
- Gaps must become required actions when they affect productive use.
