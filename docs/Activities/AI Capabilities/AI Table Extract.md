---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# AI Table Extract

![Likha Control Room - AI Settings](../../images/control-room-ai-settings.png)

**Activity group:** AI Capabilities

## Purpose

Extracts tabular data from a PDF or image and saves the rows into a DataTable variable.

Use this when a document or screenshot contains a table that needs to be looped through, written to Excel, added to a queue, or filtered.

## Properties

- `input_file`: Path to a PDF or image file.
- `output`: Output DataTable variable.
- `status_code`: Output variable for the HTTP status code.

## Example

```txt
input_file: C:\Docs\invoice-table.pdf
output: ExtractedTable
status_code: AITableExtractStatusCode
```

Then use:

```txt
For Each source: ExtractedTable
```

or write the result with Excel > Write Range.

## Notes

For PDFs, the activity reads text from the PDF before sending table extraction instructions to the AI model. For scanned PDFs, convert the page to an image or use OCR first if the PDF has no embedded text.

