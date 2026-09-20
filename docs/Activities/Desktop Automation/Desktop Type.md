---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Desktop Type

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Desktop

## Purpose

Types text into a desktop UI element.

## Properties

- `selector`: Captured desktop selector.
- `text`: Text to type. Supports variables.
- `interval`: Delay between characters.
- `fallback_coordinates`: Use x/y if selector fails.
- `fallback_ocr`: Use image/OCR fallback.

## Variable syntax

Use variables in normal text fields with double braces:

```txt
{{variable_name}}
{{object_name.property}}
{{current_row["Column Name"]}}
```

Use direct variable names inside operation fields unless the activity help says otherwise:

```txt
count > 1
status == "Done"
current_row["Last Name"]
```

## Example

```txt
text: {{current_row["Name"]}}
interval: 0.02
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
