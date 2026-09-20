---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

![Likha Control Room - Queue Management](../../images/control-room-queues.png)

## Scripting activities

Scripting activities run external scripts or shell commands and save their outputs into variables.

### Scripting > Run PowerShell

Runs a PowerShell command using `powershell.exe`.

Properties:

```txt
Command            PowerShell command text
Timeout            timeout in seconds
PowershellOutput   stdout output variable
Script Error       stderr or timeout output variable
```

### Scripting > Run VBScript

Runs VBScript text using `cscript.exe`.

Properties:

```txt
Command            VBScript command/script text
Timeout            timeout in seconds
VBScript output    stdout output variable
Script Error       stderr or timeout output variable
```

### Scripting > Run DOS command

Runs a DOS command using `cmd.exe /c`.

Properties:

```txt
Command              DOS command text
Timeout              timeout in seconds
CommandOutput        stdout output variable
CommandErrorOutput   stderr or timeout output variable
CommandExitCode      numeric exit code output variable
```

Notes:

- A timeout stores an error message and uses exit code `-1` for DOS commands.
- Non-zero exits are captured in output variables, then handled by the activity Error handling settings.
- Error handling supports Retry on error, Stop with error, Resume next, and Go To label.
- Use the output variables in `Conditional`, `If Else`, `Case`, or `Set Variable` activities.
