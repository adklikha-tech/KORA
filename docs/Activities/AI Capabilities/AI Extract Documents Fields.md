---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# AI Extract Documents Fields

![Likha Control Room - AI Settings](../../images/control-room-ai-settings.png)

**Activity group:** AI Capabilities

## Purpose

Extracts specific named fields from document text or readable document files and saves the result as structured JSON plus readable text.

Use this when a flow needs invoice numbers, totals, dates, customer names, reference numbers, or other document values for later automation steps.

## Properties

- `document_files`: One or more readable file paths. Use one path per line or semicolon-separated paths.
- `document_text`: Pasted document text or a variable such as `{{ocr_text}}` or `{{DocumentText}}`.
- `fields`: Field definitions to extract. Each field has a `name` and optional `sample_pattern`.
- `json_response`: Output variable for the extracted object.
- `text_response`: Output variable for a formatted text version of the extracted object.
- `status_code`: Output variable for the HTTP status code.

## Field Definitions

Define fields in the activity property panel. A field should describe the value you want back:

```txt
name: invoice_number
sample_pattern: INV-1001

name: total_amount
sample_pattern: 1234.56
```

The sample pattern is a hint for the AI. It does not require an exact match.

## Example

```txt
document_text: {{InvoiceText}}
fields:
  invoice_number: INV-1001
  total_amount: 1234.56
json_response: ExtractedFieldsJson
text_response: ExtractedFieldsText
status_code: AIExtractStatusCode
```

The `ExtractedFieldsJson` variable can be used later with expressions such as:

```txt
ExtractedFieldsJson["invoice_number"]
```

## Notes

This activity reads text-like files directly. For scanned PDFs or images, use OCR or AI Vision first, then pass the extracted text into `document_text`.

