# Maintainer Instructions

## Source Of Truth

- `skills/mournival-architecture/SKILL.md` defines agent behavior.
- `references/roles/` defines the four steward perspectives.
- `references/rubrics/` defines review scoring and veto rules.
- `assets/schemas/` defines reusable output schemas.
- `assets/templates/` defines output templates.
- `examples/` proves expected behavior.

## Before Commit

Run:

```powershell
npm run validate
npm run test
npm run package
```

## Skill Rules

- Keep core workflow in `SKILL.md`.
- Keep detailed role behavior in `references/roles/`.
- Do not make the role files independent skills.
- Keep the skill a single deployable unit until roles need separate lifecycle,
  installation, or release cadence.
- Never weaken evidence requirements to improve usability.
- Never let dirty information enter productive use without review state,
  evidence class, and traceability.

## Release

- Update `CHANGELOG.md`.
- Run all checks.
- Package with `npm run package`.
