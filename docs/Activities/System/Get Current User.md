---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Get Current User

**Activity group:** System

## Purpose

Returns the Windows account running the workflow as text.

## Properties

- `Output Text`: Text variable that receives the current user.

## Output

When a Windows domain is available, the result uses `DOMAIN\username`. Otherwise, it returns the username.

## Example

```txt
Output Text: CurrentUser
```

In unattended execution, this is the robot service or user-agent account, which may differ from the person who scheduled the flow.
