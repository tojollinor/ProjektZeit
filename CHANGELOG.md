# Changelog

## ProjektZeit 1.0.5 — 2026-09-19

- Reconciled the Greenfield build against pre-reset product requirements and restored missing workflows.
- Replaced native browser prompts and Windows MessageBox flows with consistent ProjektZeit-owned dialogs and added regression guards.
- Restored direct work-time corrections with pauses, audit history and billed-time protection.
- Added linked payroll reversal entries and explicit project billing handoff/reopen workflows.
- Restored profile editing, avatar, theme selection, holiday-region defaults, API tokens and CSV import/export.
- Restored admin MFA reset UI, individual permission overrides, optional first-password change and policy-controlled remember-me login.
- Restored customer/project history, evidence-to-customer suggestions, Zammad owner filters, provider column settings and TeamViewer token help.
- Restored grouped STARFACE missed calls with persistent callback status and compact notification indicators.
- Restored a responsive month calendar and expanded regression coverage for the reconciled workflows.


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


## ProjektZeit 1.0.2 — 2026-09-19

- Completed employee master-data views with work models and contact visibility.
- Added full administrator user management including role assignment, activation and password reset.
- Added editable role and permission management in the web interface.
- Added customer detail editing, archiving and customer contacts including Zammad and TeamViewer mappings.
- Added project detail editing, lifecycle controls and project-member management.


## ProjektZeit 1.0.1 — 2026-09-19

- Completed absence, on-call, notification, attachment and branding workflows.
- Completed billing approval, rejection, resubmission, finalization and correction states.
- Added Zammad, STARFACE and TeamViewer provider clients and settings.
- Hardened permissions, calendar visibility and version/release handling.


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
