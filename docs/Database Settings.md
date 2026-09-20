---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Database Settings

Likha uses SQLite automatically on a fresh installation. No database configuration is required for a local desktop or small single-machine deployment.

Open **Control Room > Database** to select SQLite, PostgreSQL, or Microsoft SQL Server for flows, agents, knowledge, conversations, schedules, queues, robot records, settings, and run history.

## SQLite

Select **SQLite (default)** and leave the file path unchanged to use Likha's normal local database. In development this is `data/rpa.db`. In the installed desktop application it is `%LOCALAPPDATA%\Likha\data\rpa.db`.

A different SQLite file may be selected when a separate local data store is required. Do not place a SQLite file on an unreliable network share or allow multiple machines to write to the same file.

## PostgreSQL or Supabase

Select **PostgreSQL / Supabase** and enter a PostgreSQL connection URL:

```text
postgresql://user:password@host:5432/database?sslmode=require
```

The database user must be allowed to connect and create or update Likha tables. Use the direct or session-pooler URL supplied by the provider. Likha encrypts the saved connection URL with a key local to the installation.

## Microsoft SQL Server

Select **Microsoft SQL Server**, then configure:

- Server or instance, such as `localhost\SQLEXPRESS`, `SQLSERVER01`, or `sql.company.com,1433`.
- Database name.
- Windows Authentication or SQL Login.
- SQL Login username and password when applicable.
- Installed ODBC driver name.
- Connection encryption and certificate trust behavior.

Microsoft ODBC Driver 18 for SQL Server must be installed on every Windows machine that connects directly to SQL Server. The configured account must be able to connect to the selected database and create or update Likha tables. SQL Login passwords are encrypted with a key local to the Likha installation.

Keep **Encrypt connection** enabled for remote and Azure SQL connections. Enable **Trust server certificate** only when using a certificate that the Windows machine cannot validate, such as an approved internal development certificate.

## Activate a Selection

1. Select the database type.
2. Enter its file path, connection URL, or SQL Server settings.
3. Select **Test connection**.
4. Select **Save database settings**.
5. Close and restart Likha.

Likha creates missing tables in the selected SQLite, PostgreSQL, or SQL Server database during startup.

## Switching Does Not Migrate Data

Selecting another database does not copy existing records. The previous database retains its flows, agents, knowledge, conversations, settings, queues, schedules, and run history. Export or migrate the required records before switching a production installation.

The database selection itself is stored outside the active database under Likha's local data folder. This allows Likha to determine which database to open during startup.

