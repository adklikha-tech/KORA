---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# AI Click

**Activity group:** AI Screen Control

## Purpose

Clicks a visible target found through an `AIElement`, a natural-language description, or a captured image snippet.

## Properties

- `Target Window`: `Automatic` or part of the target window title.
- `AIElement`: Optional variable created by AI Find Element.
- `Target Description`: Used when no `AIElement` or image snippet is supplied.
- `OCR / Image Target Snippet`: Optional captured target region searched within the selected window.
- `Snippet Match Confidence`: Required image-match score from `0.1` to `1`.
- `Minimum Confidence`: Required element confidence from `0` to `1`.
- `Click Action`: Mouse action, such as `left click`.
- `Output`: Boolean variable set to `true` after a successful click.

## Example

```txt
Target Window: Rpa Challenge
AIElement: SubmitButton
Minimum Confidence: 0.7
Click Action: left click
Output: ClickSucceeded
```

If the visible layout may move, use AI Find Element immediately before this activity. Likha refuses targets inside its own application window.
