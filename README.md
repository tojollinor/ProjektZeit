# ProjektZeit

ProjektZeit is a self-hosted work platform for employee time, customers, projects, orders, billing preparation, absences, expenses, calendar, notifications and integrations such as Zammad, STARFACE and TeamViewer.

Copyright © 2026 Tobias Friedrichsen. ProjectZeit is free of charge for private use and commercial internal use, but it is not open-source software. See [LICENSE.md](LICENSE.md).

## Requirements

- Docker Engine with Docker Compose
- PostgreSQL is included by the provided Compose stack
- A reverse proxy / HTTPS endpoint is recommended for production
- SMTP and external integrations are optional and can be configured after first login

## Installation with Docker Compose

1. Download `docker-compose.yml` and `.env.example` from this repository.
2. Copy `.env.example` to `.env`.
3. Replace every password/secret placeholder and set `APP_URL` to the public HTTPS address.
4. Start the stack with `docker compose up -d`.
5. Open the configured `APP_URL`.

The initial administrator is created only when the database is empty. Change the bootstrap password after the first login and remove `BOOTSTRAP_ADMIN_PASSWORD` from the environment afterwards.

## First start and demo mode

At the first login ProjectZeit offers **Start directly** or **Create demo data**. Demo mode creates realistic example employees, customers, projects, orders, times, absences, expenses, calendar events, billing data, notifications and integration examples. A visible `DEMO` badge remains active until an administrator resets the installation.

The demo reset deletes all business data created during demo mode and preserves only the initial administrator. The setup wizard can then be started again.

## PWA

The web application is installable as a Progressive Web App. Offline mode is read-only for data already cached on the device. Time tracking and other write operations always require server confirmation.

## Windows client

Official Windows releases contain a normal installer, not a portable application. The installer asks for the ProjectZeit server address before installation, verifies the public server version endpoint and checks this repository's [compatibility manifest](compatibility.json). Existing installations keep their configured server address.

## Integrations

Global Zammad, STARFACE and TeamViewer configuration is managed by administrators. Users connect their personal external accounts separately. Personal tokens are not exposed to administrators. Provider rate limits are only applied when the provider documents an actual limit; ProjectZeit has no artificial global API throttle.

## Updates

Server updates are performed through the normal container deployment process. The application does not self-update its server. The Windows client checks compatibility before installing an update.

## Backup

ProjektZeit does not provide an integrated backup system. Back up the PostgreSQL database and Docker volumes with the host or infrastructure backup solution.

## New database structure

This Greenfield release uses a completely new database structure.

## Support

Use GitHub Issues in this public repository for reproducible bugs and installation problems. Never include passwords, API tokens, client secrets or private customer data in an issue.
