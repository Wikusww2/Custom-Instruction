# File Research Pipeline

## Purpose

Find, inspect, and synthesize source files accurately. Use this when the answer depends on local files, uploaded files, folders, document collections, logs, code, spreadsheets, slides, or PDFs.

## Workflow

1. Clarify the target
   - Identify the requested topic, date, module, file type, output format, and source boundary.
   - If the user says "all files" or "elsewhere," search broadly enough to include likely duplicates and outliers.

2. Build a candidate set
   - Use filenames, folder paths, extensions, metadata, and dates.
   - Prefer fast file search first.
   - Include likely synonyms and related terms.

3. Inspect content
   - Use text extraction for searchable PDFs, DOCX, TXT, Markdown, HTML, CSV, spreadsheets, and code.
   - Use OCR workflow for scanned/image-only sources.
   - For spreadsheets, inspect sheet names, headers, formulas, and relevant ranges.
   - For slides, inspect slide titles, speaker notes, and visual text where possible.

4. Track evidence
   - Keep file path, page, section, heading, line, row, or slide references.
   - Mark duplicates and near-duplicates.
   - Separate direct source claims from assistant inference.

5. Synthesize
   - Answer the question directly.
   - Group findings by topic, source, date, or priority as appropriate.
   - Note missing or conflicting evidence.

6. Verify output
   - Check that the answer is grounded in the inspected files.
   - Confirm that extracted dates, numbers, formulas, and names match the source.
   - State any extraction limitations.

## Useful extraction methods

- Text PDFs: `pdftotext`, built-in PDF parsing, or document readers.
- Scanned PDFs/images: OCR with Tesseract or other OCR.
- DOCX: structured document extraction.
- XLSX/CSV: spreadsheet parsers rather than ad hoc text search.
- Code: repository search plus entry-point, tests, and config inspection.

## Failure modes to avoid

- Relying on filename matches only.
- Missing scanned pages because text extraction returned nothing.
- Treating duplicates as separate sources.
- Summarizing without page/section evidence.
- Answering from general knowledge when source files were requested.
