# Instruction Router

Use this router to decide what to load.

## Default route

For ordinary prompts:

1. Apply `quality-levels/L1-reliable-default.md`.
2. Apply all required core modules.
3. Apply only the relevant domain module.
4. If a tool workflow would improve evidence, verification, file analysis, OCR, calculation, simulation, or algorithm design, read the relevant file in `tools/`.
5. If a skill trigger matches, load the skill.

## Escalation route

Use `L2-verified.md` when:
- web research is needed,
- citations are required,
- the user asks whether something is true,
- the answer depends on recent information,
- the answer contains specific numbers, dates, standards, or classifications.

Use `L3-high-stakes.md` when:
- the content is medical, legal, financial, safety-related, or ethical,
- incorrect advice could cause material harm,
- the user asks for clinical or academic support.

Use `L4-production-artifact.md` when:
- generating code, documents, ZIPs, PDFs, slides, spreadsheets, or other deliverables,
- the output needs file paths, links, reproducibility, or validation.

## Tool route

Use `tools/README.md` to choose a tool workflow.

Common tool routes:
- File or document investigation: `domains/file-research.md` and `tools/file-research-pipeline.md`.
- Images, scans, screenshots, or PDFs with visual text: `tools/ocr-vision-pipeline.md`.
- Numeric, symbolic, or multi-step calculations: `domains/calculations-and-units.md` and `tools/calculation-verification.md`.
- Simulations or computational models: `domains/simulations-and-modeling.md` and `tools/simulation-design.md`.
- Algorithm design, optimization, or implementation planning: `tools/algorithmic-design.md`.

## Skill route

If the request starts with or clearly means:
- “Show me...”
- “Visualize...”
- “Explain visually...”
- “Make an interactive infographic about...”

then load:
- `.agents/skills/show-me-infographic/SKILL.md`

## Fallback route

If the repo cannot be read, use the compact fallback in `custom-instructions/chatgpt-paste-prompt.txt`.
