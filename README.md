# Business Operations Planning System

A public-safe case study of a database-backed internal planning and workflow system built for structured academic and operational scheduling. This repository does not include production source code, database dumps, configuration files, credentials, uploads, backups, or client-specific data.

## Business Problem

Organizations that coordinate programs, courses, instructors, rooms, sessions, and schedules often rely on spreadsheets or manual communication. That creates duplicated records, unclear access control, schedule conflicts, delayed approvals, and limited visibility into planning activity.

## Solution Overview

The verified source project implements a PHP and MySQL/MariaDB web application for managing planning data, user access, timetable workflows, conflict checks, exports, and administrative monitoring. The system is positioned here generically as a business operations planning platform that demonstrates experience building internal workflow software.

## Core Capabilities

- Program, session, semester, and course management
- Instructor, room, lab, and resource allocation
- Timetable generation, validation, conflict review, and approval workflows
- Role-based administration and scoped access
- User activation, login, OTP verification, and trusted-browser controls
- Device/IP binding controls for administrative access monitoring
- Activity logging, dashboard views, live presence, and operational reports
- CSV/PDF-style export workflows and data import support
- Email workflows through PHPMailer

## System Workflow

1. Administrators configure organizational structures, sessions, programs, courses, instructors, rooms, and access scopes.
2. Planning users create or update course offerings and scheduling resources.
3. Scheduling logic checks availability, resource constraints, and timetable conflicts.
4. Managers review generated or edited schedules through dashboard and timetable views.
5. The system records activity, exposes reports, and supports exports for operational use.

## Technology Stack

- PHP
- MySQL/MariaDB
- PDO
- HTML/CSS
- PHPMailer
- Composer

## Security Approach

The verified project includes authentication, role checks, scoped permissions, CSRF protection, password hashing paths, OTP verification for elevated access, trusted-browser handling, login logging, rate-limit style checks, secure-session helpers, and device/IP binding workflows.

This public case study describes those mechanisms conceptually only. It does not include implementation details, secrets, hashes, user records, network data, or production configuration.

## Commercial Applications

This type of system is suitable for organizations that need custom internal tools for planning, scheduling, resource allocation, approval workflows, reporting, and administrative control across multiple teams or departments.

## Project Status

Public-safe case-study documentation. Production source code and operational data are intentionally excluded.

Additional detail is available in:

- [Architecture](docs/architecture.md)
- [Features](docs/features.md)
- [Security](docs/security.md)
