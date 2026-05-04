# Skills

Skills are reusable workflows. This repository stores skills under `.agents/skills/`.

## How models should call skills

1. Read `skills/skill-registry.md`.
2. Match the user’s request to a skill description.
3. Load the matching `.agents/skills/<skill-name>/SKILL.md`.
4. Follow the skill instructions for that turn.
5. Do not use a skill when the trigger does not match.

## Installation notes

For OpenAI/Codex-style skills, each skill is a directory containing a required `SKILL.md` file and optional scripts, references, or assets.

For API or skill upload workflows, zip a single skill folder as its own top-level folder. For example, zip `.agents/skills/show-me-infographic/` as `show-me-infographic.zip`.

## Current skills

- `show-me-infographic`
