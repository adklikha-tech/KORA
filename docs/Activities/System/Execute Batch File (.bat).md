---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Execute Batch File (.bat)

**Activity group:** System

## Purpose

Runs a Windows `.bat` or `.cmd` file and captures its standard output, error output, and exit code.

## Properties

- `Batch File (.bat)`: Full path to an existing `.bat` or `.cmd` file. Environment variables in the path are expanded.
- `Arguments`: Optional command-line arguments passed to the batch file.
- `Working Directory`: Optional execution folder. When blank, the batch file folder is used.
- `Timeout (seconds)`: Maximum runtime before the process is stopped with a timeout error.
- `Standard Output`: Text variable that receives standard output.
- `Error Output`: Text variable that receives standard error.
- `Exit Code`: Number variable that receives the process exit code.

## Example

```txt
Batch File (.bat): C:\Scripts\daily-import.bat
Arguments: "C:\Input Files" production
Working Directory: C:\Scripts
Timeout (seconds): 120
Standard Output: BatchOutput
Error Output: BatchError
Exit Code: BatchExitCode
```

A non-zero exit code is treated as an activity failure and follows the configured On Error policy. Do not place passwords or secrets directly in Arguments.
