# Changelog

## ProjektZeit 1.0.5 — 2026-09-22

- Reconciled the Greenfield build against the agreed product requirements and restored missing workflows.
- Hardened billing and time-booking integrity against concurrent PostgreSQL operations, including approval/rejection races and duplicate starts.
- Protected finalized billing positions and already billed orders against unintended direct changes or new time bookings.
- Bound live SSE streams to their concrete login sessions so revoked sessions stop receiving events immediately.
- Completed MFA reset/re-enrollment, secure login-email changes, client-specific session lifetimes and privacy for personal security history.
- Completed individual pause-rule handling and explicit pause corrections for work time versus order time.
- Added server-side pagination/sorting for projects, orders and provider tables plus cursor/keyset pagination and indexes for deep audit/security history.
- Replaced native browser and Windows dialogs with ProjektZeit-owned dialogs and expanded regression coverage.
- Validated PostgreSQL 17 concurrency and a realistic multi-user mix up to 20 simultaneous users, with an additional 25-user reserve run without request errors or deadlocks.
- Known performance note: under the deliberately small 2-core load-test runner, calendar requests were the main latency outlier at high concurrency; this is accepted for 1.0.5 and remains a later optimization topic.


## ProjektZeit 1.0.4 — 2026-09-19

- Completed the Greenfield master-plan acceptance pass and added a persistent master-plan status checklist.
- Added Dienstreisen with travel periods, overnight stays and provided meals.
- Added real notification delivery for SMTP e-mail, browser Web Push and Pushover.
- Added personal and company Pushover configuration, browser push registration and channel preferences.
- Completed account security settings for passkeys, TOTP, recovery codes and session revocation.
- Completed editable company, work-time, SMTP, time-category and absence-type settings.
- Hardened production startup, trusted hosts, security headers and readiness diagnostics.
- Added automatic Alembic upgrades at container startup and upgrade grants for existing bookkeeping roles.
- Expanded the Windows client with order stop, notifications, tray alerts and update checks.
- Added server permission auditing and full Docker-based Chromium E2E coverage for desktop and mobile.


## ProjektZeit 1.0.3 — 2026-09-19

- Added full calendar event creation, editing, invitations, responses and company-wide events.
- Added flexible statistics workbench with scoped date-range analysis and saved views.
- Added external evidence synchronization and review for Zammad, STARFACE and TeamViewer.
- Added customer, project and order mapping for external evidence.
- Added structured audit/security logs and extended operational diagnostics.
- Added responsive web workbenches and regression tests for the new workflows.


## ProjektZeit 1.0.2 — 2026-09-19

- Completed employee master-data views with work models and contact visibility.
- Added full administrator user management including role assignment, activation and password reset.
- Added editable role and permission management in the web interface.
- Added customer detail editing, archiving and customer contacts including Zammad and TeamViewer mappings.
- Added project detail editing, lifecycle controls and project-member management.
- Added server-side permission checks and regression tests for the new master-data workflows.


## ProjektZeit 1.0.1 — 2026-09-19

- Completed absence workflows including approval, cancellation and hour-ledger synchronization.
- Added on-call rotations, slots and replacement workflows.
- Added notification management, attachment/receipt workflows and company branding.
- Completed billing approval, rejection, resubmission, finalization and correction states.
- Added real provider clients and settings for Zammad, STARFACE and TeamViewer.
- Hardened permissions, calendar visibility and release/version handling.
- Added source-free public release publication with installer checksums.


## ProjektZeit Server 1.0.0 — 2026-09-18

- First Greenfield release with a new relational data model and audit history.
- Customers, employees, projects, orders, work time, absences, expenses and billing domains.
- Role-based permissions with per-user exceptions.
- PWA, responsive web application, notifications, calendar/iCal, diagnostics and integration account model.
- New setup wizard and full demo-data workflow.

## ProjektZeit Windows 1.0.0 — 2026-09-18

- New tray client with browser authorization using Authorization Code + PKCE.
- New regular Windows installer with server and compatibility checks before installation.
- Server URL is preserved for upgrades.
