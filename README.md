# mournival-architecture-skill

Single-skill repository for architecture governance reviews using four steward
perspectives:

- Architecture Decision Steward
- Architecture Risk Steward
- Architecture Value Steward
- Architecture Assurance Steward

The skill reviews knowledge claims, dirty information, contradictions,
architecture artifacts, optimization candidates, and release or pipeline gates.
It always separates role reviews from the consolidated decision.

## Install For Codex

```powershell
npx -y skills add MartinEgli/mournival-architecture-skill --skill * -a codex --yes
```

## Local Checks

```powershell
npm run validate
npm run test
npm run package
```

## Skill

```text
skills/mournival-architecture/SKILL.md
```

## Output Shape

The expected review shape is:

1. Decision Steward Review
2. Risk Steward Review
3. Value Steward Review
4. Assurance Steward Review
5. Consolidated Mournival Decision
6. Required Actions
7. Blocked Next Steps
8. Allowed Next Steps
