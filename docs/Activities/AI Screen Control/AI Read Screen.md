---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# AI Read Screen

**Activity group:** AI Screen Control

## Purpose

Extracts visible text and layout from the current screen into a structured object.

## Properties

- `Output`: Object variable containing `full_text`, bounded text blocks, tables, fields, and a layout summary.
- `Status Code`: Number variable that receives the AI request HTTP status code.
- `Timeout`: Maximum AI request time in seconds.

## Example

```txt
Output: ScreenContent
Status Code: AIReadStatusCode
Timeout: 90
```

Use this activity when downstream steps need screen text. Use AI Understand Screen when the flow needs a broader explanation of controls and screen state.
