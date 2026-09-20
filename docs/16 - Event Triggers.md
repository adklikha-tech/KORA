---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Event Triggers

Event triggers start workflows from external or system events.

This overview reuses the detailed trigger guide:

[Event Triggers.md](Activities/Event%20Triggers/Event%20Triggers.html)

## Trigger Types

- HTTP request received
- Scheduled
- Email received
- File
- Folder
- Queue
- Webhook
- Windows Event

## Runtime Behavior

Triggers are managed from:

```text
Control Room > Robots > Event triggers
```

Triggered runs are unattended jobs. They should be handled by the robot runtime rather than designer Run.

## Required Runtime

- `LikhaRobotService` supervises trigger definitions.
- `LikhaUserAgent` is required for interactive desktop/browser/UI work.
- VM robot setup requires Control Room URL and robot token configuration.

