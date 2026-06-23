# Risk Rubric

Use this rubric to classify consequence and misuse risk.

## Checkpoints

- Are assumptions unproven?
- Is data classification missing or unclear?
- Is compliance or privacy impact possible?
- Is security impact possible?
- Could the claim be misused later?
- Does it create lock-in or semantic drift?
- Is wording stronger than evidence supports?

## Risk Levels

- `low`: limited effect, reversible, clear evidence and classification.
- `medium`: meaningful impact or ambiguity, manageable with conditions.
- `high`: harmful consequence possible; human review required.
- `critical`: severe harm, compliance breach, security exposure, or production
  contamination likely.

## Hard Veto

Block when:

- data classification is unclear and productive use is requested
- high or critical risk lacks Human Architect review
- Dirty Information can be mistaken for validated knowledge
- compliance or security risk is plausible and unresolved
