# Research Notes

These notes summarize the public guidance used to design this repo.

## OpenAI Skills

OpenAI describes ChatGPT Skills as reusable, shareable workflows that can bundle instructions, examples, and code. OpenAI API documentation describes a skill as a versioned bundle of files plus a `SKILL.md` manifest with front matter and instructions.

OpenAI Cookbook guidance separates:
- system prompts for global behavior and stable policies,
- tools for external actions or live state,
- skills for repeatable workflows, scripts, templates, and procedures.

Codex documentation states that a skill is a directory with a required `SKILL.md` file and optional scripts, references, assets, and agents metadata. It also emphasizes that skill descriptions are important for implicit matching.

## Custom Instructions

OpenAI Help documentation describes Custom Instructions as user-provided guidance applied to chats. It also documents a 1500-character limit for the longer text field.

Because of that limit, this repo uses a compact Custom Instructions prompt as a router, while the full rules live in this repository.

## Other user approaches

Public GitHub and community examples commonly treat custom instructions as:
- persistent project or user behavior guidance,
- a repository-level rulebook,
- modular instruction files,
- reusable prompt/skill packages.

A common limitation discussed by users is that plain Custom Instructions do not always automatically dereference external URLs in every environment. This repo therefore includes a self-contained fallback prompt.
