---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Distributed Control Room and VM Robot Setup

This MVP lets Kora run with a central Control Room server and one or more VM robot resources.

## Architecture

```text
Server machine
  Kora Control Room
  SQLite database
  Scheduler, queues, logs, robot jobs
  HTTP API

Robot VM
  KoraRobotService
  KoraUserAgent
  Browser / desktop / mouse / keyboard automation
```

The Control Room owns flows, schedules, queues, robot jobs, and run logs. The VM robot polls the Control Room over HTTP, claims jobs, executes them in the VM user session, then posts status, logs, and output back.

## 1. Configure the Control Room server

Start Kora Control Room on a server reachable by robot VMs.

Example URL:

```text
http://KORA-SERVER:8000
```

Recommended: set a shared robot token in Control Room:

```text
Control Room > Robots > Setup Helper > Robot API token
```

Save the token there, then copy the same value into each robot VM `robot.env`.

Alternative: set a token before starting the server:

```powershell
$env:KORA_ROBOT_TOKEN="change-this-shared-token"
```

If both are present, the Control Room saved setting is used first. Every robot VM must use the same token.

Open the firewall for the Control Room port, for example TCP `8000`.

From the VM, test:

```powershell
Invoke-WebRequest http://KORA-SERVER:8000/api/health
```

## 2. Configure each robot VM

Copy `robot.env.example` to `robot.env` in the Kora application folder.

Example:

```text
KORA_CONTROL_ROOM_URL=http://KORA-SERVER:8000
KORA_ROBOT_TOKEN=change-this-shared-token
KORA_ROBOT_NAME=VM-Robot-01
```

If `KORA_CONTROL_ROOM_URL` is present, `KoraRobotService` and `KoraUserAgent` run in remote robot mode.

## 3. Start the VM robot components

On the VM, start:

```text
run_robot_service.bat
run_user_agent.bat
```

`KoraRobotService` sends service heartbeat to Control Room.

`KoraUserAgent` must run inside the logged-in Windows user session. It handles browser, desktop, mouse, keyboard, screen, Excel, and other UI automation.

## 4. Confirm in Control Room

Go to:

```text
Control Room > Robots
```

You should see:

- Robot Service: Online
- User Agent: Online
- VM robot resource listed by name
- Heartbeat updated within 45 seconds

## 5. Run a flow on the VM

Create or select a flow that uses browser, desktop, mouse, keyboard, screen, monitor, or message box activities.

When you click Run or a schedule fires:

1. Control Room creates a queued robot job.
2. VM `KoraUserAgent` claims the job.
3. The flow runs inside the VM desktop session.
4. Logs and output return to Control Room.
5. The Robots page shows job status.

## Notes and MVP limitations

- UI automation requires an active Windows user session on the VM.
- The service can run in the background, but desktop/browser actions must be performed by `KoraUserAgent`.
- This MVP sends logs and output variables back to Control Room. File artifact upload, screenshots, package deployment, and advanced robot assignment rules are future improvements.
- For production, use HTTPS, unique robot tokens, locked-down firewall rules, and a dedicated robot Windows account.
