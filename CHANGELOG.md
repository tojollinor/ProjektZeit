# Changelog

## ProjektZeit 1.0.13 — 2026-10-09

- Linked dashboard time-series aggregation to the selected day, ISO-week, month or year period, removing the redundant monthly aggregation checkbox.
- Moved hours-development chart boundary values to the right side while keeping pinch zoom.
- Replaced general dashboard data-widget tables, including employee hours in Buchhaltung, with compact responsive cards and full record detail dialogs. Added a consistent inline search with reset and readable, rounded hour values.
- Updated the dashboard period regression expectation for the controlled selector.
- Integrated the approved original logo into Web/PWA, Windows and installer builds through checksum-verified branding assets, refreshing the PWA cache.


## ProjektZeit 1.0.12 — 2026-10-08

- Refined the compact work-status panel with the active order-time clock and concise order, project and customer context.
- Improved pause and order-time controls: the chooser disappears during breaks and mutually exclusive start/stop actions are no longer displayed together.
- Added touch pinch zoom from 1× to 8× to the timeline and hours-development chart while preserving horizontal scrolling.
- Recovered valid PWA install icons (192/512 px), updated the service worker cache and expanded installability checks.
- Added read-only customer details until explicitly entering edit mode, quick details for selected entities and modal creation workflows with persistent actions.
- Made quick creation of customers, projects, orders and time categories context-aware, with list refresh and direct selection after saving.
- Modernized the mobile projects overview with responsive, tappable cards, a consistent status layout and customer-style search.
- Expanded automated frontend, server and desktop/mobile regression coverage.
- Deferred replacement of the header master logo until an approved original asset is available; existing logo usage remains unchanged.

## ProjektZeit 1.0.11 — 2026-10-08

- Unified input/search field feedback and made the compact work-status strip fully interactive, including keyboard support and a visible expand control.
- Moved ProjektZeit Web branding and the DEMO marker to the header while improving the compact sidebar, version badge and expand control.
- Separated Dashboard widget editing (pencil) from dashboard management (gear), retaining personal layouts, sharing and existing permission rules.
- Replaced multiple period controls with one picker for days, ISO calendar weeks, months and years, including bounded date ranges across years.
- Improved the Arbeitszeit Soll/Ist summary with actual/target values, progress and deviations while retaining the existing balance, order and comparison statistics.
- Added a subtle line marking the current day in the daily trend chart.
- Separated the Compose image tag (PROJEKTZEIT_IMAGE_TAG) from the server product version so package metadata remains authoritative.
- Extended frontend, backend and desktop/mobile regression coverage.


## ProjektZeit 1.0.10 — 2026-10-07

- Removed the misleading hardcoded server-version fallback; runtime version is now read from the installed package or an explicit non-empty override and fails visibly when neither is available.
- Unified ProjektZeit branding across the Windows window, sidebar, tray and installer while keeping the approved web branding unchanged.
- Compacted the live work-status strip so status and running time share one clear line.
- Reworked dashboard navigation and management: real dashboard names remain in the main tabs, creation/copy/share/delete actions live in management, and Dashboard categories distinguish Mein Dashboard, Buchhaltung, System and Admin.
- Added reusable page-information actions and persistent dialog footers with explicit Schließen actions.
- Modernized Zeiten & Korrekturen with compact adjacent filters, rounded controls and clearer session, order-time and history panels.
- Modernized customer search and replaced the mobile customer table with fixed-width customer cards to prevent horizontal page scrolling.
- Expanded frontend, server and E2E regression coverage for the 1.0.10 UX and versioning changes.

## ProjektZeit 1.0.9 — 2026-10-06

- Stabilized product-logo rendering on login and product surfaces without replacing the approved branding asset.
- Reworked the workday panel into a collapsible live status surface with second-by-second work, pause and order timers and no manual refresh action.
- Added permission-aware <Neuer …> choices for customers, projects, orders and time categories while reusing the existing creation workflows.
- Modernized order search and added a dedicated mobile order-card view with project, customer, status, responsibility and contextual actions.
- Removed sticky status behavior on mobile and kept entity details in full-height mobile dialogs with a persistent bottom close action.
- Normalized common action-button sizing, spacing and responsive grouping across desktop and mobile.
- Extended frontend and desktop/mobile E2E regression coverage for the new workday, quick-create, mobile order and dialog-footer behavior.

## ProjektZeit 1.0.8 — 2026-10-05

- Completed the second UI/UX live-review round across desktop and mobile.
- Applied system dark mode before login and separated product branding from PWA/app icons.
- Reworked navigation, persistent desktop sidebar, Admin-Optionen, settings and notification navigation.
- Made master-data tables use the available width and moved entity details into accessible dialogs.
- Improved work-time selection layout, dashboard period controls, chart date axes and timeline detail dialogs.
- Added calendar day and event detail views including descriptions and series information.
- Made personal expenses directly reachable without exposing bookkeeping navigation to normal users.
- Hardened attachment uploads, previews, downloads, deletion, MIME/signature validation and repeated uploads for supported business objects.
- Expanded release-gate E2E coverage for security headers, PWA manifest, dynamic version reporting, table width, sidebar scrolling and responsive overflow.
- Made the closed-posting-period regression test independent of the current calendar month.

## ProjektZeit 1.0.7 — 2026-09-23

- Replaced remaining PZ placeholders with the ProjektZeit product logo and completed PWA/browser icon branding.
- Reorganized settings into personal, data/tooling and permission-aware Admin-Optionen sections.
- Added optional project/order assignment for expenses with server-side visibility and consistency validation.
- Made customer, project, order and employee rows directly keyboard- and mouse-accessible and added direct entity navigation from global search.
- Added a real order detail view while preserving permission checks and existing row actions.
- Unified card, panel, control and dialog surface radii across light, dark and mobile layouts without changing Dashboard editor behavior.
- Expanded frontend regression coverage and CI to run Vitest before the production web build.

## ProjektZeit 1.0.6 — 2026-09-23

- Fixed failed-login handling on PostgreSQL so the first invalid login returns HTTP 401 instead of HTTP 500.
- Hardened login-lock counters against legacy NULL values and added database-level defaults plus a migration.
- Added regression coverage for fresh and legacy login-lock rows.

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
