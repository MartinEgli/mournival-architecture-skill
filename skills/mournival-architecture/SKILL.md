---
name: mournival-architecture
description: >
  Architecture governance review skill for Knowledge Claims, Dirty Information,
  contradictions, architecture artifacts, optimization candidates, release gates,
  and pipeline decisions. Use when the user asks for Mournival review, steward
  review, architecture assurance, evidence and traceability checks, risk review,
  value review, Clean AI governance review, go/no-go recommendations, or
  consolidated architecture decisions, including governance diagrams, evidence
  traceability diagrams, decision flow diagrams, risk/value/assurance maps, and
  Mermaid or PlantUML review diagrams.
---

# Mournival Architecture

## Purpose

Run a controlled architecture review through four steward perspectives:
Decision, Risk, Value, and Assurance. Produce separate role reviews and one
consolidated decision.

## When to Use

Use for architecture governance reviews involving:

- Knowledge Claims or Knowledge Claim Candidates
- Dirty Information
- contradictory statements or competing versions
- architecture artifacts
- optimization or re-run candidates
- AI-generated claims or Clean AI governance checks
- release gates and pipeline decisions
- evidence, traceability, risk, value, or go/no-go assessment
- governance, evidence traceability, decision flow, or review-state diagrams

## Do Not Use When

Do not use when the user only needs a simple explanation, implementation task,
or unstructured brainstorming without review or decision need.

Do not use to create the primary enterprise, security, software, or DDD design.
Use `enterprise-architecture`, `enterprise-security-architecture`,
`software-architecture`, or `domain-driven-design` for design creation, then use
this skill for evidence, risk, value, assurance, and go/no-go review.

## Mandatory Rules

- Evaluate internally in this order: Assurance, Risk, Value, Decision.
- Output role sections in this order: Decision, Risk, Value, Assurance.
- Use `references/role-collaboration.md` to coordinate the four roles and
  consolidate their findings.
- Always end with Consolidated Mournival Decision.
- Separate evidence, inference, assumption, and gap.
- Keep every finding, veto, status, diagram element, and consolidated decision
  traceable to source IDs, supplied artifacts, or explicitly marked gaps.
- Never accept unsupported truth claims as productive knowledge.
- Never lower evidence requirements for convenience.
- Never allow Dirty Information into productive use without review state,
  evidence class, and traceability.
- Escalate high-risk decisions to Human Architect review.
- Preserve user-provided IDs, labels, paths, commands, source names, and error
  strings exactly.
- If evidence class, source, decision context, or intended next step is missing,
  block productive acceptance and mark the missing item as a gap.
- Hand design creation back to the relevant architecture skill instead of
  filling missing design content during governance review.
- When creating diagrams, create review/governance diagrams only and read
  `references/diagrams.md`.

## Inputs Expected

Helpful inputs:

- claim or artifact under review
- source IDs, fragment IDs, conversation excerpt IDs
- evidence class
- execution context
- target audience
- intended next step
- pipeline stage or release gate
- data classification

If inputs are missing, mark them as gaps. Do not invent them.

## Modes

### /mournival review-claim

Review a Knowledge Claim or Knowledge Claim Candidate. Load:

- `references/role-collaboration.md`
- `references/prompts/review-knowledge-claim.md`
- `references/rubrics/assurance-rubric.md`
- `references/rubrics/risk-rubric.md`

### /mournival review-dirty-information

Review uncertain, unverified, or contaminated information before it becomes a
candidate. Load:

- `references/role-collaboration.md`
- `references/prompts/review-dirty-information.md`
- `references/rubrics/assurance-rubric.md`
- `references/rubrics/risk-rubric.md`

### /mournival review-contradiction

Review conflicting claims, source conflicts, version conflicts, or context
splits. Load:

- `references/role-collaboration.md`
- `references/prompts/review-contradiction.md`
- `references/rubrics/assurance-rubric.md`
- `references/rubrics/decision-rubric.md`

### /mournival review-artifact

Review an architecture artifact for evidence, risk, usefulness, and decision
readiness. Load:

- `references/role-collaboration.md`
- `references/prompts/review-artifact.md`
- `references/rubrics/value-rubric.md`
- `references/rubrics/decision-rubric.md`

### /mournival final-check

Run final gate review before productive use, release, training dataset
inclusion, RAG ingestion, or decision record publication. Load:

- `references/role-collaboration.md`
- `references/review-process.md`
- `references/rubrics/assurance-rubric.md`
- `references/rubrics/risk-rubric.md`
- `references/rubrics/value-rubric.md`
- `references/rubrics/decision-rubric.md`

### /mournival clean-ai

Review AI-generated or AI-assisted architecture claims and artifacts for
evidence, provenance, traceability, risk, value, human control, and acceptance
decision. Load:

- `references/role-collaboration.md`
- `references/prompts/review-clean-ai.md`
- `references/rubrics/assurance-rubric.md`
- `references/rubrics/risk-rubric.md`
- `references/rubrics/value-rubric.md`
- `references/rubrics/decision-rubric.md`

### /mournival diagram

Create or review governance diagrams using Mermaid or PlantUML: evidence
traceability, role finding flow, decision flow, veto map, review-state map, or
productive-use gate. Load:

- `references/diagrams.md`
- `references/role-collaboration.md`
- `references/review-process.md`

## Evidence Handling

Use `references/review-process.md`.
Use `references/evidence-traceability.md`.

Required labels:

- Evidence: directly present in supplied material or verified source.
- Inference: reasoned conclusion from evidence.
- Assumption: useful but unverified.
- Gap: missing item that can change the decision.

## Output Contracts

Use `assets/templates/mournival-output-template.md` unless user asks for another
format.

Role reviews must follow `assets/schemas/role-review.schema.yaml`.

Consolidated decision must follow
`assets/schemas/mournival-decision.schema.yaml`.

Findings should follow `assets/schemas/finding.schema.yaml`.

## Quality Gates

Before final answer, verify:

- all four role reviews are present
- role collaboration order was followed
- veto rules are applied
- missing evidence is not treated as evidence
- findings and consolidated decision include traceability or explicit gaps
- blocked next steps are explicit
- allowed next steps are explicit
- human review requirement is explicit
- final status is one of the allowed statuses
- AI-generated content is not accepted as evidence by itself
- diagrams are governance or review diagrams and do not create primary
  enterprise, security, software, or DDD designs

## Boundaries

- Do not replace accountable human architecture approval.
- Do not provide legal, compliance, privacy, or security certainty without
  verified source basis.
- Do not approve high-risk productive use alone.
- Do not hide uncertainty to make an artifact look usable.
- Do not create primary architecture design diagrams; hand those to the relevant
  architecture skill.

## Output Style

- Use concise structured output.
- Prefer YAML for machine-readable review results.
- Keep rationale short and specific.
- Use role names exactly.
- Use Mermaid for quick governance diagrams and PlantUML when the review flow
  must be kept as architecture-as-code.
- Do not add fictional persona language.
