# Dignity Net Public Export Workflow

This repo contains the public-facing copies of Dignity Net materials. The canonical full-stack markdown source currently lives outside this repo at:

- `/Users/genevieveprentice/Documents/Dignity Core/01_DignityNet/DN-FullStack_v1.4_2026-07-16.md`

The public repo currently publishes a Markdown reading copy:

- `DN-FullStack_v1.4_2026-07-16.md`

Older public artifacts should not remain in this repo because they can create install confusion.

## Prerequisites

- `pandoc` installed locally
- Google Chrome installed at:
  - `/Applications/Google Chrome.app/Contents/MacOS/Google Chrome`
- `pdftotext` available for verification

## Rebuild The Public DN Markdown

1. Copy the canonical source into the public repo.

2. Update the public header:

- set `Version` to the promoted version,
- set `Status` to `CANONICAL`,
- remove candidate-only change notes,
- include the public copyright / license pointer.

3. Verify there are no stale references to older public DN versions:

```bash
rg 'DN-FullStack_v1\.[123]|Dignity Net Full Stack v1\.[123]|latest Full Stack document \(v1\.[123]\)' README.md index.md BUILD.md
```

4. Confirm README and index point to the current public full stack:

```bash
rg 'DN-FullStack_v1.4_2026-07-16.md|Current Version' README.md index.md
```

## Optional PDF Export

If a PDF is needed later, export from the current public Markdown file and name it with the same version:

```bash
pandoc 'DN-FullStack_v1.4_2026-07-16.md' \
  -s \
  -o /private/tmp/DN-FullStack_v1.4_2026-07-16.html \
  --metadata title='DN-FullStack_v1.4_2026-07-16'
```

## Notes

- The rights line should live in the public markdown itself so every downstream export inherits it.
- If the public markdown paper changes rights language, keep it aligned with the full-stack source and `LICENSE.md`.
- If Chrome or Pandoc locations change, update this file rather than relying on memory.
