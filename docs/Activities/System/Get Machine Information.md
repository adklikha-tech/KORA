---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Get Machine Information

**Activity group:** System

## Purpose

Returns identifying and operating-system information for the machine executing the workflow.

## Properties

- `Output Object`: Object variable that receives the machine information.

## Output Fields

- `MachineName`
- `OperatingSystem`
- `OSVersion`
- `OSRelease`
- `Architecture`
- `Processor`
- `CpuCount`

## Example

```txt
Output Object: MachineInformation
```

Access a field in an operation with bracket notation, for example `MachineInformation["MachineName"]`.
