---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Desktop Automation

Desktop automation targets Windows desktop applications through UI Automation selectors, OCR/image fallback, and hardware input where needed.

## Desktop Activities

- [Desktop Start.md](Activities/Desktop%20Automation/Desktop%20Start.html)
- [Desktop Activate.md](Activities/Desktop%20Automation/Desktop%20Activate.html)
- [Desktop Click.md](Activities/Desktop%20Automation/Desktop%20Click.html)
- [Desktop Type.md](Activities/Desktop%20Automation/Desktop%20Type.html)
- [Desktop Hotkey.md](Activities/Desktop%20Automation/Desktop%20Hotkey.html)
- [Desktop Screenshot.md](Activities/Desktop%20Automation/Desktop%20Screenshot.html)
- [Desktop Extract Text.md](Activities/Desktop%20Automation/Desktop%20Extract%20Text.html)
- [Desktop Extract Table.md](Activities/Desktop%20Automation/Desktop%20Extract%20Table.html)
- [Desktop Wait Element.md](Activities/Desktop%20Automation/Desktop%20Wait%20Element.html)
- [Desktop Close.md](Activities/Desktop%20Automation/Desktop%20Close.html)

## Selector And Fallback Notes

Use Pick to capture a desktop selector. For unreliable controls, configure fallback behavior:

- OCR/image fallback
- Optional OCR target text
- X/Y fallback only when explicitly enabled

Desktop Click documentation:

[Desktop Click.md](Activities/Desktop%20Automation/Desktop%20Click.html)

## Recommended Pattern

1. Start or activate the application.
2. Use selectors when controls expose stable Windows properties.
3. Use OCR/image fallback for visual controls.
4. Use x/y fallback only as a last resort.

