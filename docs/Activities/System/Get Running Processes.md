---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Get Running Processes

**Activity group:** System

## Purpose

Returns the processes currently running on the robot machine as a DataTable.

## Properties

- `Output DataTable`: DataTable variable that receives the process rows.

## Output

Each row describes a running process and can be used by For Each, Filter Data Table, or other DataTable activities.

## Example

```txt
Output DataTable: RunningProcesses
```

Process visibility depends on the permissions of the Windows account running Likha.
