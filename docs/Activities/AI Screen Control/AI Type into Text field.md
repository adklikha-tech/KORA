---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# AI Type into Text field

**Activity group:** AI Screen Control

## Purpose

Finds or reuses a visible text field, focuses it, and types text into it.

## Properties

- `Target Window`: `Automatic` or part of the target window title.
- `AIElement`: Optional variable created by AI Find Element.
- `Target Description`: Used to find the field when no `AIElement` is selected.
- `Text to Type`: Literal text or text containing `{{variable}}` tokens.
- `Clear Existing Text`: Selects and replaces existing text before typing.
- `Minimum Confidence`: Required element confidence from `0` to `1`.
- `Interval`: Delay in seconds between keystrokes.
- `Output`: Boolean variable set to `true` after successful typing.

## Example

```txt
Target Window: Customer Portal
Target Description: Email address field
Text to Type: {{customer_email}}
Clear Existing Text: true
Minimum Confidence: 0.7
Interval: 0.02
Output: TypeSucceeded
```

Likha first attempts Windows UI Automation and falls back to hardware coordinates when necessary.
