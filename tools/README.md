# Tools

This folder defines reusable tool workflows and helper designs. These are not mandatory dependencies; they are operating procedures for using available tools well.

Use these files when a task benefits from extra evidence extraction, verification, or structured design:

| Tool workflow | Use for |
|---|---|
| `file-research-pipeline.md` | Searching, reading, and synthesizing local or uploaded files |
| `ocr-vision-pipeline.md` | OCR for scanned PDFs, screenshots, photos, diagrams, and image-heavy documents |
| `calculation-verification.md` | Complex calculations, formulas, unit checks, symbolic/numeric validation |
| `simulation-design.md` | Designing simulations, models, and interactive demonstrations |
| `algorithmic-design.md` | Algorithm choice, data structures, complexity, edge cases, and implementation plans |

## General rule

Use a tool workflow when it would make the answer more accurate, verifiable, or useful. Do not mention tool internals unless the user asks or it helps explain the result.

## Output discipline

When a tool workflow is used:
- state the useful result, not every internal step,
- cite files, paths, pages, lines, or sources where relevant,
- say what could not be verified,
- avoid pretending a tool was run when it was only recommended.
