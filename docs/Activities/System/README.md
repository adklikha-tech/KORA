---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# System Activities

System activities manage Windows processes, run batch files, and retrieve information about the robot machine and signed-in user.

## Activities

- [Terminate Process](Terminate%20Process.html)
- [Get Running Processes](Get%20Running%20Processes.html)
- [Execute Batch File (.bat)](Execute%20Batch%20File%20(.bat).html)
- [Get Machine Information](Get%20Machine%20Information.html)
- [Get Current User](Get%20Current%20User.html)

All System activities support Retry, Retry Count, Retry Interval, and On Error behavior.

## Execution Notes

- System activities run on the machine executing the workflow, not necessarily the Control Room server.
- In an unattended setup, confirm the robot account has permission to access the requested process, file, and working directory.
- Use caution with Terminate Process and batch files because they can affect applications and data outside the flow.
