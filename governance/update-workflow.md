# Update Workflow

Use this when editing the repo.

## Versioning

- Update `VERSION.md` when behavior changes.
- Add a short entry to `CHANGELOG.md`.
- Keep `START_HERE.md` stable and short.

## Adding a core rule

1. Create or update a file in `core/`.
2. Link it from `core/README.md`.
3. Link it from `START_HERE.md` if it is required.

## Adding a domain rule

1. Create a file in `domains/`.
2. Add it to `domains/README.md`.
3. Add routing guidance to `instruction-router.md` if needed.

## Adding a skill

1. Create `.agents/skills/<skill-name>/SKILL.md`.
2. Include valid front matter with `name` and `description`.
3. Add it to `skills/skill-registry.md`.
4. Add installation notes if scripts/assets are included.
