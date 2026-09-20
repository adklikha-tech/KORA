---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Installation Guide

## Development Or Local Desktop Install

1. Install Python dependencies:

```bat
install.bat
```

2. Start the desktop app:

```bat
run_desktop.bat
```

3. Build and run workflows from the desktop shell.

## Browser Dashboard

Start the FastAPI dashboard:

```bat
run.bat
```

Then open:

```text
http://127.0.0.1:8765
```

## Direct Server Startup

```bat
python -m uvicorn app.main:app --host 127.0.0.1 --port 8765
```

## Desktop Build

```bat
build_desktop.bat
```

Packaged output:

```text
dist\Likha\Likha.exe
```

## Installer Build

```bat
build_installer.bat
```

Installer output:

```text
installer-output\LikhaSetup.exe
```

## OCR Setup

OCR activities prefer the bundled Tesseract folder:

```text
tesseract/
  tesseract.exe
  tessdata/
    eng.traineddata
```

See:

[How to Setup OCR Tesseract](How%20to%20Setup%20OCR%20Tesseract.html)

## Robot Runtime

For unattended setup:

- `run_robot_service.bat`
- `install_robot_service.bat`
- `run_user_agent.bat`

See:

- [Robot Service and User Agent.md](Robot%20Service%20and%20User%20Agent.html)
- [Distributed Control Room and VM Robot Setup.md](Distributed%20Control%20Room%20and%20VM%20Robot%20Setup.html)

## Optional Shared Database Drivers

SQLite works automatically and needs no additional database setup. PostgreSQL support uses a PostgreSQL connection URL. Microsoft SQL Server requires **Microsoft ODBC Driver 18 for SQL Server** on every Windows machine that connects directly to the database.

After installation, configure and test the shared database under **Control Room > Database**, save the selection, and restart Likha.

See:

[Database Settings](Database%20Settings.html)


