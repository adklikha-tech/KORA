---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# AI Verify Screen

**Activity group:** AI Screen Control

## Purpose

Checks whether the current screen matches an expected state and returns a decision, explanation, and confidence score.

## Properties

- `Expected Screen or State`: Natural-language condition to verify.
- `Minimum Confidence`: Required confidence from `0` to `1`; a lower score forces `Is Verified` to `false`.
- `Is Verified`: Boolean result variable.
- `Explanation`: Text variable explaining the decision.
- `Confidence`: Number variable containing the returned score.
- `Status Code`: Number variable that receives the AI request HTTP status code.
- `Timeout`: Maximum AI request time in seconds.

## Example

```txt
Expected Screen or State: Verify that the success message is visible and the form was submitted
Minimum Confidence: 0.7
Is Verified: IsVerified
Explanation: VerificationExplanation
Confidence: VerificationConfidence
```

Use the Boolean output in an IF Else activity to branch on the verification result.
