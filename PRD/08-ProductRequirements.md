# Kurukshetra Product Requirements Document (PRD)

---

# Version

1.0

---

# Last Updated

28 July 2026

---

# Prepared By

Saurabh Singh

---

# Purpose

This document defines the functional and non-functional requirements of Kurukshetra. It serves as the primary blueprint for designers, developers, testers, and future contributors while building the platform.

---

# Product Vision

Kurukshetra aims to become India's leading college esports platform by providing students and organizers with a unified system for tournament management, team collaboration, player profiles, rankings, analytics, and community engagement.

The platform focuses on simplicity, scalability, and transparency while reducing manual effort and improving the tournament experience for every participant.

---

# Product Goals

The primary goals of Kurukshetra are:

- Simplify tournament management.
- Digitize college esports.
- Build gaming communities.
- Improve communication.
- Reduce organizer workload.
- Enable player recognition.
- Support college esports growth.

---

# Product Scope

### Included in MVP

- Student registration
- Login system
- Tournament creation
- Tournament registration
- Team creation
- Team invitations
- Match scheduling
- Live brackets
- Notifications
- Leaderboards
- Player profiles
- Organizer dashboard

---

### Not Included in MVP

- Live streaming
- Merchandise store
- Sponsor marketplace
- AI matchmaking
- Mobile applications
- Scholarship portal

These features are planned for future releases.

---

# User Roles

### Student

- Register
- Join tournaments
- Create teams
- View rankings
- Receive notifications

---

### Organizer

- Create tournaments
- Manage teams
- Publish results
- Schedule matches

---

### College Administrator

- Verify tournaments
- View analytics
- Manage college profile

---

### Super Admin

- Manage users
- Manage colleges
- Moderate content
- Platform analytics

---

# Functional Requirements

Functional Requirements (FR) describe the specific capabilities the system must provide.

Each requirement has a unique ID.

Priority Levels:

- Must Have
- Should Have
- Could Have

---

# Epic 1 — Authentication

## Description

This module manages user registration, login, security, and account access.

### FR-001

User can create an account.

Priority: Must Have

---

### FR-002

User can log in using email and password.

Priority: Must Have

---

### FR-003

User can log out.

Priority: Must Have

---

### FR-004

User can reset forgotten password.

Priority: Must Have

---

### FR-005

User verifies email address.

Priority: Should Have

---

### FR-006

Support Google Sign-In.

Priority: Should Have

---

### FR-007

Support role-based authentication.

Roles:

- Student
- Organizer
- College Admin
- Super Admin

Priority: Must Have

---

# Epic 2 — User Profile

## Description

Each user has a gaming profile.

### FR-008

View profile.

Priority: Must Have

---

### FR-009

Edit profile.

Priority: Must Have

---

### FR-010

Upload profile picture.

Priority: Should Have

---

### FR-011

Display gaming statistics.

Priority: Must Have

---

### FR-012

Display tournament history.

Priority: Must Have

---

### FR-013

Display earned badges.

Priority: Could Have

---

### FR-014

Display rankings.

Priority: Must Have

---

# Epic 3 — College Management

## Description

Manage colleges registered on Kurukshetra.

### FR-015

Create college profile.

Priority: Must Have

---

### FR-016

Students join college.

Priority: Must Have

---

### FR-017

College verification.

Priority: Should Have

---

### FR-018

Display college rankings.

Priority: Could Have

---

### FR-019

Display college statistics.

Priority: Should Have

---

### FR-020

Manage official college page.

Priority: Could Have

---

# Acceptance Criteria

Authentication Module

A feature is complete when:

- User can register.
- User can log in.
- Invalid credentials show proper error.
- Session remains secure.
- Password reset works correctly.

User Profile Module

A feature is complete when:

- Profile loads successfully.
- User can edit profile.
- Statistics display correctly.

College Module

A feature is complete when:

- Students join colleges.
- College data displays correctly.

---

# Epic 4 — Tournament Management

## Description

The Tournament Management module allows organizers to create, manage, and monitor esports tournaments from a centralized dashboard.

### FR-021

Organizer creates tournament.

Priority: Must Have

---

### FR-022

Organizer edits tournament.

Priority: Must Have

---

### FR-023

Organizer deletes tournament.

Priority: Must Have

---

### FR-024

Tournament has registration deadline.

Priority: Must Have

---

### FR-025

Tournament supports multiple games.

Examples:

- BGMI
- Valorant
- Free Fire MAX
- Chess
- FIFA
- CS2

Priority: Must Have

---

### FR-026

Organizer defines rules.

Priority: Must Have

---

### FR-027

Tournament banner upload.

Priority: Should Have

---

### FR-028

Maximum team limit.

Priority: Must Have

---

### FR-029

Tournament visibility.

Options

- Public
- Private
- College Only

Priority: Must Have

---

# Epic 5 — Team Management

## Description

Students create and manage esports teams.

### FR-030

Create team.

Priority: Must Have

---

### FR-031

Invite teammates.

Priority: Must Have

---

### FR-032

Accept invitation.

Priority: Must Have

---

### FR-033

Leave team.

Priority: Must Have

---

### FR-034

Transfer captain.

Priority: Should Have

---

### FR-035

Team logo upload.

Priority: Could Have

---

### FR-036

Team statistics.

Priority: Should Have

---

### FR-037

Team achievements.

Priority: Could Have

---

# Epic 6 — Match Management

## Description

Manage tournament matches.

### FR-038

Automatic match scheduling.

Priority: Must Have

---

### FR-039

Manual schedule editing.

Priority: Should Have

---

### FR-040

Match reminders.

Priority: Must Have

---

### FR-041

Result submission.

Priority: Must Have

---

### FR-042

Dispute reporting.

Priority: Should Have

---

### FR-043

Winner declaration.

Priority: Must Have

---

# Epic 7 — Bracket System

## Description

Generate tournament brackets automatically.

### FR-044

Single Elimination.

Priority: Must Have

---

### FR-045

Double Elimination.

Priority: Should Have

---

### FR-046

Round Robin.

Priority: Future

---

### FR-047

Automatic bracket generation.

Priority: Must Have

---

### FR-048

Live bracket updates.

Priority: Must Have

---

### FR-049

Bracket sharing.

Priority: Should Have

---

# Acceptance Criteria

Tournament Module

A tournament is complete when:

- Organizer creates it.
- Registration opens.
- Registration closes automatically.
- Teams join successfully.
- Bracket generates correctly.

Team Module

A team is complete when:

- Captain creates team.
- Players join.
- Team enters tournament.

Bracket Module

Complete when:

- Winners automatically advance.
- Bracket updates correctly.
- Final winner is displayed.


