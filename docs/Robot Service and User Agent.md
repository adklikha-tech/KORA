---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

## KoraRobotService and KoraUserAgent

Kora unattended runtime has two MVP components.

### KoraRobotService

`KoraRobotService` is the background supervisor. It is designed to run without the Control Room UI open.

Responsibilities:

- Creates robot runtime tables when needed.
- Sends heartbeats to `robot_resources`.
- Watches due schedules.
- Stores and supervises event trigger definitions.
- Picks up queued background-safe runs.
- Dispatches desktop/browser/UI jobs to a user-session agent.

Run in console mode:

```bat
run_robot_service.bat
```

Install as a Windows service:

```bat
install_robot_service.bat
```

Remove the Windows service:

```bat
uninstall_robot_service.bat
```

### KoraUserAgent

`KoraUserAgent` must run inside a logged-in Windows user session. It executes jobs that need an interactive desktop, browser, mouse, keyboard, monitor, or message box session.

Run it from the robot user account:

```bat
run_user_agent.bat
```

### Recommended VM setup

1. Install Kora on the VM.
2. Install and start `KoraRobotService`.
3. Configure `KoraUserAgent` to start when the robot Windows account logs in.
4. Keep the VM awake and logged in for desktop/browser automation.
5. Use schedules or queued runs to trigger work.

The service is the supervisor. The user agent is the interactive robot.

### Event triggers

Event triggers are managed in:

```txt
Control Room > Robots > Event triggers
```

For parameter details and examples, see:

```txt
Documentation/Event Triggers.md
```
