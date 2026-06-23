# Role Collaboration Guide

Use this guide for every Mournival review.

## Four-Role Model

The four stewards review the same artifact from different concerns. They are
not personas and they do not debate theatrically. Treat them as four review
lenses that protect decision quality.

| Role | Primary Question | Main Power |
| --- | --- | --- |
| Architecture Assurance Steward | Is it evidenced, traceable, and not overstated? | Blocks unsupported productive knowledge |
| Architecture Risk Steward | What can go wrong if this is accepted or used? | Blocks high-risk or unclear-risk use |
| Architecture Value Steward | Is it understandable, useful, and actionable? | Requires rework for poor utility |
| Architecture Decision Steward | What decision or next action is allowed now? | Consolidates progress, stop, rework, or escalation |

## Internal Review Order

Evaluate internally in this order:

1. Assurance
2. Risk
3. Value
4. Decision

This order matters:

- Assurance first decides what can be treated as evidence.
- Risk then evaluates only what is evidenced or explicitly marked as an
  assumption, inference, or gap.
- Value improves usability without weakening evidence or hiding risk.
- Decision last converts the combined review into allowed next steps, blocked
  next steps, required actions, and escalation.

## Output Order

Output role sections in this order:

1. Decision Steward Review
2. Risk Steward Review
3. Value Steward Review
4. Assurance Steward Review
5. Consolidated Mournival Decision

The output starts with Decision so the user sees the actionable result first,
while the underlying reasoning still respects Assurance before Risk before Value
before Decision.

## Interaction Rules

- Assurance may downgrade or block any claim that lacks source, traceability, or
  correct evidence class.
- Risk may block or require human review when harm, misuse, compliance, security,
  data classification, or semantic drift is material.
- Value may require rework when an artifact is not understandable or actionable,
  but it must not soften evidence gaps or risk findings.
- Decision must not override Assurance or Risk vetoes. It may only convert them
  into blocked next steps, required actions, rework, or escalation.
- A soft Value concern can become blocking only when poor clarity would cause
  misuse, wrong decisions, or failed handoff.
- If roles disagree, preserve the disagreement as a finding and let the
  stricter evidence or risk position determine productive-use status.

## Veto Strength

Use this precedence when consolidating:

1. Assurance veto: unsupported, untraceable, contaminated, or overstated
   knowledge cannot become productive knowledge.
2. Risk veto: high or unclear material risk requires blocking, rework, or Human
   Architect review.
3. Decision veto: process, ownership, or approval path is missing.
4. Value veto: artifact is too unclear or unusable for the intended audience or
   next step.

## Consolidation Steps

1. Identify the artifact or claim under review.
2. Classify supplied material as evidence, inference, assumption, or gap.
3. Run Assurance review and record evidence blockers.
4. Run Risk review and record risk blockers or human-review triggers.
5. Run Value review and record usefulness or clarity rework.
6. Run Decision review and derive allowed next steps, blocked next steps, and
   required actions.
7. Produce the consolidated decision using the strictest unresolved blocker.

## Final Status Selection

- `accepted`: evidence is sufficient, risk is acceptable, value is clear, and
  no blocking decision issue remains.
- `accepted_with_conditions`: productive use is allowed only after listed
  conditions or limited to a stated scope.
- `needs_rework`: useful direction exists, but evidence, risk, clarity, or
  decision gaps must be fixed before acceptance.
- `blocked`: productive use must stop because a blocker remains unresolved.
- `human_review_required`: accountable human architecture review is required
  before productive use.

## Common Failure Modes

- Decision jumps to approval before Assurance checks evidence.
- Value makes unsupported content look more credible through polished wording.
- Risk treats every uncertainty as a blocker instead of separating material and
  non-material risk.
- Assurance blocks low-risk useful work because formatting is incomplete while
  source meaning is clear.
- The consolidated decision hides role disagreement instead of preserving it.

## Minimal Review Pattern

For small reviews, keep each role short but still present:

- Decision: final action, blocked/allowed next steps.
- Risk: material risks and human-review need.
- Value: usability and audience fit.
- Assurance: evidence basis, traceability, gaps.

Never omit a role section in a Mournival result.
