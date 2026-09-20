---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# AI Understand Screen

**Activity group:** AI Screen Control

## Purpose

Analyzes the current screen and returns structured information about its summary, controls, forms, tables, visible text, and screen state.

## Properties

- `Instruction`: Describes what the AI should inspect or explain.
- `Output`: Object variable that receives the structured screen analysis.
- `Status Code`: Number variable that receives the AI request HTTP status code.
- `Timeout`: Maximum AI request time in seconds.

## Example

```txt
Instruction: Identify the active application, visible form fields, and available actions
Output: ScreenUnderstanding
Status Code: AIUnderstandStatusCode
Timeout: 90
```

Use [AI Find Element](AI%20Find%20Element.html) when the next step must interact with one specific control.
