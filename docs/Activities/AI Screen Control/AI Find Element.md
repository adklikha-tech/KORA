---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# AI Find Element

**Activity group:** AI Screen Control

## Purpose

Finds one visible UI element from a natural-language description and saves its location and metadata as an `AIElement` variable.

## Properties

- `Target Window`: `Automatic` or part of the target window title.
- `Target Description`: Natural-language description such as `Submit button`.
- `Minimum Confidence`: Required match confidence from `0` to `1`.
- `Output`: `AIElement` variable containing the description, text, control type, confidence, bounds, and center coordinates.
- `Status Code`: Number variable that receives the AI request HTTP status code.
- `Timeout`: Maximum AI request time in seconds.

## Example

```txt
Target Window: Rpa Challenge
Target Description: Submit button below the form
Minimum Confidence: 0.7
Output: SubmitButton
```

Pass `SubmitButton` to AI Click. The activity fails when the returned confidence is lower than Minimum Confidence.
