# Assurance Rubric

Use this rubric to protect evidence, origin, traceability, and auditability.

## Checkpoints

- Is origin present?
- Is source ID present?
- Is fragment ID or conversation excerpt ID present when needed?
- Is evidence class present and plausible?
- Is execution context present?
- Is review status present?
- Is version present?
- Is wording limited to what evidence supports?
- Is backward and forward traceability complete?

## Evidence Classes

Use project-specific evidence classes if supplied. When none are supplied, use:

- `E0`: unsupported or unknown
- `E1`: source-backed artifact
- `E2`: multi-source or independently checked artifact
- `E3`: confirmed conversation or human confirmation
- `E4`: approved architecture decision or controlled record

## Hard Veto

Block productive use when:

- origin is missing
- evidence class is missing
- traceability is missing
- claim is overstated beyond source
- Dirty Information is being promoted without review state
