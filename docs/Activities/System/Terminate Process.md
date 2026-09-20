---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Terminate Process

**Activity group:** System

## Purpose

Terminates every running Windows process whose executable name matches the supplied process name.

## Properties

- `Process Name`: Windows process name with or without the `.exe` extension.

## Example

```txt
Process Name: notepad.exe
```

Save work before using this activity. It does not ask the target application to close gracefully, and more than one matching process may be terminated.
