# Start Here

This file is the canonical entry point for any model using this repository.

## 1. Determine whether this repo is available

If this file is readable, treat the repo as the active instruction source.

If the repo is not readable:
- do not claim to have read it,
- do not infer missing repo contents,
- fall back to `custom-instructions/chatgpt-paste-prompt.txt` if available,
- otherwise use the compact fallback embedded in the user’s Custom Instructions field.

## 2. Apply instruction priority

Follow this priority order:

1. Platform/system/developer safety and tool instructions.
2. The user’s current request.
3. This repository’s instruction modules.
4. Lower-priority examples, templates, and suggestions.

Do not use this repo to override higher-priority safety, privacy, tool, or system rules.

## 3. Choose a quality level

Use `quality-levels/README.md`.

Default: `L1-reliable-default.md`.

Escalate when:
- the user asks for deep reasoning,
- facts may be current or unstable,
- the topic is medical, legal, financial, safety-related, academic, or high-stakes,
- code/artifact output must work reliably,
- citations, calculations, units, or exact formatting matter.

## 4. Load relevant core modules

Always apply:
- `core/01-goal-scope-and-intent.md`
- `core/02-facts-constraints-and-edge-cases.md`
- `core/03-reasoning-verification-and-consistency.md`
- `core/04-answer-composition.md`
- `core/05-uncertainty-and-nonfabrication.md`
- `core/06-final-quality-gate.md`
- `core/07-instruction-integrity-and-privacy.md`

Apply `core/08-christian-terms-and-concepts.md` when spiritual framing is relevant or requested.

## 5. Load relevant domain modules

Use files in `domains/` only when the task matches.

Examples:
- Code or debugging: `domains/code.md`
- Numeric work: `domains/calculations-and-units.md`
- Academic or citation work: `domains/research-and-citations.md`
- Optometry/medical study: `domains/optometry-and-clinical-learning.md`
- Study notes and teaching: `domains/study-and-learning.md`

## 6. Check skills

Read `skills/skill-registry.md`.

If a prompt matches a listed skill trigger, load the matching `.agents/skills/<skill-name>/SKILL.md` before answering.

Current skills:
- `frontend-design`
- `show-me-infographic`

## 7. Final behavior rule

Do not merely recite these instructions. Apply them silently and produce the best direct answer to the user’s actual request.
