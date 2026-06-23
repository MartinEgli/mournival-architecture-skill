# Mournival Governance Diagrams

Use this reference for `/mournival diagram` or when the user asks for a
Mournival diagram.

## Scope

Create diagrams for review and governance only:

- evidence traceability from source to claim to decision
- role collaboration flow: Assurance, Risk, Value, Decision
- Dirty Information quarantine and promotion flow
- contradiction resolution flow
- review-state and productive-use gate diagrams
- veto maps and escalation paths
- Clean AI governance review flow
- allowed next steps, blocked next steps, and required actions

Do not create primary enterprise, security, software, or DDD design diagrams.
Hand those to `enterprise-architecture`, `enterprise-security-architecture`,
`software-architecture`, or `domain-driven-design`.

## Notation Choice

- Mermaid `flowchart` for review states, evidence flow, veto maps, and
  governance gates.
- Mermaid `stateDiagram-v2` for Dirty Information, candidate, accepted,
  blocked, and human-review states.
- Mermaid `sequenceDiagram` for review handoff or approval flows.
- PlantUML activity/state diagrams when the user wants persistent
  architecture-as-code for governance process.

## Diagram Rules

- Show evidence, inference, assumption, and gap as distinct concepts.
- Preserve IDs, source labels, finding IDs, and decision labels exactly.
- Do not make a claim appear accepted unless the consolidated decision allows
  it.
- Show vetoes and human-review triggers visibly.
- If evidence is missing, the diagram must show the gap instead of smoothing it
  away.

## Output Pattern

1. State review purpose and diagram type.
2. State notation used and why.
3. Provide diagram code.
4. List unresolved evidence gaps, risk blockers, and decision blockers.
5. State whether productive use is allowed, conditional, blocked, or requires
   human review.
