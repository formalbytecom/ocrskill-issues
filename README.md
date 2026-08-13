# OCRskill.com public issue tracker

Public issue tracker for [ocrskill.com](https://ocrskill.com) and the OCR API at `https://api.ocrskill.com`.

**There is no source code in this repo.** It exists only so users can report bugs, ask
questions, and request features in one searchable place.

## Open an issue

- **Bug** — something returns the wrong result, errors out, or behaves inconsistently.
- **Question / help** — you are not sure how to call the API or integrate it.
- **Feature request** — a format, field, endpoint, or integration you need.
- **Docs** — anything wrong, missing, or confusing on the site or in the API reference.

Please search existing issues first; a comment on an open issue is more useful than a duplicate.

## What to include in a bug report

The more of this you provide, the faster it gets diagnosed:

- Endpoint and method (e.g. `POST /ocr.json?fields=invoice_date,total`)
- HTTP status code and the full response body
- Approximate timestamp **in UTC**, so the request can be found in logs
- Input file type, size, and page count — plus how it was produced (scan, phone photo, export)
- A minimal `curl` command that reproduces it
- What you expected versus what you got

## Do not post secrets or sensitive documents

- **Never paste a full API key.** If one leaks, regenerate it from the
  [dashboard](https://ocrskill.com/dashboard) immediately.
- **Never attach documents containing personal or confidential data.** Redact them, or
  reproduce the problem with a synthetic sample. Issues here are public and permanent.
- Suspected vulnerabilities: do **not** open a public issue. Email legal@formalbyte.eu instead.

## Before filing: known constraints

These are by design, not bugs:

- Maximum file size is **20 MB**.
- Supported inputs: images (PNG, JPEG, WebP, GIF, BMP, TIFF), PDF, Word, Excel, PowerPoint,
  OpenDocument, RTF, CSV, HTML, Markdown, and plain text.
- Multi-page documents are read page by page, so large PDFs can take several minutes.
- OCR content is not stored server-side, so a result cannot be recovered after the fact —
  include the input needed to reproduce it.

## Links

- Website: https://ocrskill.com
- API base URL: https://api.ocrskill.com
- Structured JSON API reference: https://ocrskill.com/ocr-json-api, for AI Agents: http://ocrskill.com/ocr-json-api.md
- Free API key: `curl https://api.ocrskill.com/get-key.json`
- Usage and billing: https://ocrskill.com/dashboard
- Machine-readable docs for agents: https://ocrskill.com/llms.txt
- Blog: https://ocrskill.com/blog
- [Privacy](https://ocrskill.com/privacy) · [Terms](https://ocrskill.com/terms)
