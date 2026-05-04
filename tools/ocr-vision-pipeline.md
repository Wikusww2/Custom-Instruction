# OCR and Vision Pipeline

## Purpose

Improve extraction from images, scanned PDFs, screenshots, diagrams, handwritten notes, and documents where normal text extraction is incomplete.

## Preferred stack

Use available local tools when possible:
- Tesseract OCR for image text extraction,
- PDF rendering to images for scanned PDFs,
- image preprocessing before OCR,
- visual inspection for diagrams, tables, and layout,
- structured parsers when files are already machine-readable.

## Workflow

1. Detect whether OCR is needed
   - Text extraction returns empty or garbled output.
   - The page is scanned or image-heavy.
   - Important content is in screenshots, diagrams, tables, labels, or handwritten notes.

2. Prepare images
   - Render PDF pages at sufficient resolution.
   - Deskew or crop if needed.
   - Improve contrast and remove noise when useful.
   - Split complex pages into regions if OCR confuses columns or tables.

3. OCR
   - Run OCR on the page or region.
   - Preserve page numbers and region context.
   - Keep uncertain text marked rather than silently correcting it.

4. Validate
   - Compare OCR output against the image visually for key terms, numbers, formulas, and headings.
   - Re-run with better preprocessing when accuracy is poor.
   - Use multiple passes for tables or formulas.

5. Use in answer
   - Cite page/image context.
   - State when OCR uncertainty remains.
   - Do not over-trust OCR for small text, formulas, handwriting, or low-resolution images.

## Tesseract design notes

Useful modes:
- single block of text for paragraphs,
- sparse text for screenshots and diagrams,
- table/column regions cropped separately,
- language packs when non-English text appears.

Preprocessing options:
- grayscale,
- threshold,
- denoise,
- deskew,
- crop margins,
- upscale low-resolution images.

## Failure modes to avoid

- Treating OCR as perfect.
- Losing page numbers.
- Reading columns in the wrong order.
- Misreading similar characters such as 0/O, 1/l/I, µ/u, minus/en dash, decimal commas/points.
- Using OCR for formulas without manual verification.
