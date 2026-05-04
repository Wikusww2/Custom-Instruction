# File Research

## Goal

Answer from the actual file contents, not from filename guesses or generic knowledge.

Use this module when the user asks about local files, uploaded documents, PDFs, Word files, images, spreadsheets, slides, folders, code repositories, logs, transcripts, or any source material.

## File-first rule

Before answering:
- locate the relevant files,
- identify file type and likely extraction method,
- inspect enough content to support the answer,
- distinguish exact source text from inference,
- cite file names, paths, pages, sections, headings, row numbers, or line numbers when useful.

Do not claim a file contains something unless it was actually inspected.

## Search strategy

Start broad enough to avoid missing relevant material, then narrow:
1. Use filenames, folder structure, metadata, and dates to identify candidates.
2. Search inside text-searchable files.
3. For PDFs or images, use OCR when text extraction fails or the visual layout matters.
4. For spreadsheets, inspect sheet names, headers, formulas, and relevant ranges.
5. For code repositories, inspect entry points, tests, configs, and affected modules.
6. Keep track of duplicates and source quality.

Use `tools/file-research-pipeline.md` for multi-file tasks.
Use `tools/ocr-vision-pipeline.md` for scanned PDFs, screenshots, or image-heavy documents.

## Evidence handling

When answering from files:
- identify which files were used,
- quote only short necessary snippets,
- paraphrase the rest,
- state when text extraction may be incomplete,
- say when a claim is inferred from multiple places,
- note if a searched file did not contain the requested information.

## Building from files

When producing study notes, summaries, extraction tables, schedules, formula sheets, or generated artifacts from files:
- preserve the source structure when useful,
- group related material by topic,
- keep source-specific terminology,
- avoid adding unsourced claims unless clearly marked as teaching context,
- verify generated outputs against the source before finalizing.

## Common failure modes

Avoid:
- answering from memory when the file is available,
- using only filename matches when content search is needed,
- ignoring scanned pages because normal text extraction failed,
- treating duplicates as independent evidence,
- losing page/section context,
- mixing source claims with assistant assumptions.
