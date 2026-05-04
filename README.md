# Custom Instruction

A modular instruction repository for high-reliability ChatGPT/Codex/GitHub Copilot behavior.

This repo is designed to act as a canonical instruction source for Wikus van Wyk’s assistant behavior. It converts one long Custom Instructions prompt into maintainable Markdown modules, quality levels, domain rules, and skill packages.

## Core idea

The short Custom Instructions prompt pasted into ChatGPT acts only as an instruction router. When the model has web, repository, or file access, it should load this repo and follow `START_HERE.md`.

## Important limitation

A pasted ChatGPT Custom Instructions field cannot guarantee that every future model will automatically fetch this GitHub repo. If browsing or repository access is unavailable, the model must use the fallback rules in `custom-instructions/chatgpt-paste-prompt.txt`.

## Repository entry point

Models should start here:

1. `START_HERE.md`
2. `instruction-router.md`
3. `quality-levels/README.md`
4. Relevant files in `core/`, `domains/`, and `.agents/skills/`

## Main folders

| Folder | Purpose |
|---|---|
| `custom-instructions/` | Paste-ready ChatGPT instruction text and fallback prompt |
| `core/` | Global rules derived from the original custom prompt |
| `quality-levels/` | Response rigor levels from quick answers to high-stakes work |
| `domains/` | Task-specific rules for code, calculations, research, study, and clinical/optometry work |
| `skills/` | Skill registry and skill-calling policy |
| `.agents/skills/` | OpenAI/Codex-style skill packages containing `SKILL.md` |
| `templates/` | Reusable templates for new rules and skills |
| `governance/` | Update rules, source hierarchy, and instruction integrity |
| `.github/` | GitHub Copilot-compatible instruction files |

## Baseline philosophy

Be precise, evidence-seeking, concise, and useful. Answer the actual user request first. Verify before claiming. Do not fabricate. Distinguish known facts, inferences, uncertainty, and limits. Preserve the user’s requested format and intent.

## Source-informed design notes

This structure follows the current OpenAI guidance that:
- Skills are reusable workflows that can bundle instructions, examples, and code.
- A skill is a folder or bundle with a `SKILL.md` manifest containing front matter and instructions.
- Long global prompts should stay small; repeatable workflows belong in skills.
- GitHub/Copilot-style repositories commonly use root and path-specific instruction files for persistent project behavior.

See `docs/research-notes.md` for references and implementation notes.
