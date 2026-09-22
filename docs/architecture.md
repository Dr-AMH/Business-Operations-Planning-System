# Architecture

This document describes the verified system at a high level without production source code, database dumps, configuration files, credentials, or client-specific details.

## Application Style

The source project is a PHP web application organized around public entry points, administrative screens, API/AJAX endpoints, shared library modules, configuration files, and Composer-managed dependencies.

The architecture follows a conventional server-rendered business application pattern:

- Browser-based administrative and planning screens
- PHP request handlers for page views, AJAX actions, and API responses
- Shared PHP libraries for authentication, validation, scheduling, access control, logging, mail, and database access
- MySQL/MariaDB persistence accessed through PDO
- Composer dependency management, including PHPMailer for email workflows

## High-Level Request Flow

1. A user accesses a public or administrative page.
2. The PHP layer validates the session and access permissions.
3. Request-specific handlers call shared business modules.
4. Business modules read or update MySQL/MariaDB tables through PDO.
5. Responses are rendered as HTML pages, API/AJAX payloads, exports, or operational reports.
6. Activity and security-related events are recorded for later review.

## Major Architectural Areas

### Public Interface

The public layer contains login, dashboard, planner, profile, report, search, upload, and live-view screens. It also contains administrative screens for managing users, courses, programs, sessions, resources, timetables, activity logs, and access controls.

### API and AJAX Layer

The project includes endpoint groups for adding, updating, deleting, searching, exporting, and validating planning data. These endpoints support interactive course planning, program management, semester handling, timetable operations, and conflict checks.

### Shared Business Libraries

The shared library layer contains modules for:

- Authentication and authorization
- Access control and scoped permissions
- CSRF and request security
- Scheduling and timetable generation
- Schedule validation and conflict detection
- Academic/session planning data
- Instructor and room/resource management
- Activity logging
- Email delivery
- Device/IP binding
- Data validation and response helpers

### Database Layer

The verified schema includes tables for users, roles/permissions, sessions, programs, courses, instructors, rooms, timetable data, schedule conflicts, activity logs, login logs, trusted-browser data, device bindings, chat messages, and planning relationships.

This case-study repository does not include schema dumps or production records.

## Integration Points

Verified integration points include:

- MySQL/MariaDB through PDO
- SMTP email through PHPMailer
- CSV/PDF-style export workflows
- File upload areas in the production system, excluded here for safety

## Data Safety Boundary

The production project contains operational records and sensitive security-related data. For public presentation, only sanitized documentation is included. Production source, data, backups, uploads, configuration, and secrets are intentionally omitted.
