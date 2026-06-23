# Evidence And Traceability

Use this reference whenever Mournival findings, role reviews, diagrams, vetoes,
or consolidated decisions depend on supplied inputs.

## Input Register

Track meaningful inputs by source type:

- User fact: stated directly by the user.
- Artifact: Knowledge Claim, Dirty Information item, contradiction, diagram,
  ADR, source excerpt, source fragment, conversation excerpt, review output, or
  architecture artifact.
- Tool result: command output, validation result, scan result, generated report,
  retrieval result, or pipeline state.
- External source: cited standard, documentation, policy, control, or public
  source.
- Gap: missing evidence needed for productive acceptance.

## Traceability Rules

- Preserve claim IDs, source IDs, fragment IDs, conversation excerpt IDs, file
  paths, finding IDs, decision labels, and status names exactly.
- Tie every role finding to evidence, inference, assumption, or gap.
- Do not accept AI-generated content as evidence by itself.
- Do not convert Dirty Information into productive knowledge without review
  state, evidence class, and traceability.
- If traceability is missing, block acceptance or require human review.

## Evidence Receipt

For substantial outputs, include a compact receipt:

| Finding Or Decision | Source/Input | Type | Confidence | Gap Or Follow-up |
| --- | --- | --- | --- | --- |

Use `gap` when source, evidence class, or decision context is missing.

## Verification Pattern

Follow the small-loop pattern:

1. Locate claim, artifact, source, evidence class, and intended next step.
2. Run the smallest scoped role review.
3. Verify the consolidated decision against traceability, vetoes, and allowed
   status values.

Avoid creating missing design content during governance review; hand design
creation back to the owning architecture skill.
