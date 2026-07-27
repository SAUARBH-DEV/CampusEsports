# Kurukshetra Feature Specifications

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

This document provides detailed specifications for every feature included in Kurukshetra.

It explains how each feature behaves, the user interactions, business rules, validation requirements, and expected outcomes.

This document serves as the implementation guide for developers.

---

# Feature 1 — Authentication

## Description

Authentication allows users to securely access Kurukshetra using their credentials.

---

## Users

- Student
- Organizer
- College Admin
- Super Admin

---

## Functional Requirements

- Register
- Login
- Logout
- Reset Password
- Email Verification

---

## Input

- Name
- Email
- Password
- College

---

## Output

Authenticated user session.

---

## Validation

- Email must be unique.
- Password minimum 8 characters.
- Strong password required.
- Email format validation.

---

## Success Message

Account created successfully.

---

## Error Cases

- Email already exists.
- Invalid password.
- Invalid email.

---

# Feature 2 — Tournament Creation

## Description

Organizers can create esports tournaments.

---

## Inputs

- Tournament Name
- Game
- Description
- Banner
- Registration Deadline
- Match Format
- Team Limit

---

## Outputs

Tournament is published.

---

## Validation

Tournament name required.

Deadline must be future date.

Team limit > 1.

---

## Business Rules

Only organizers can create tournaments.

Students cannot create tournaments.

---

## Success

Tournament published successfully.

---

# Feature 3 — Team Management

## Description

Students can create and manage gaming teams.

---

## Inputs

- Team Name
- Team Logo
- Members

---

## Features

- Create Team
- Edit Team
- Invite Members
- Remove Members
- Transfer Captain

---

## Business Rules

One student can own only one active team.

Maximum members depend on the game.

---

## Validation

Unique team name.

Maximum member limit.

---

## Success

Team created successfully.

---

# Feature 4 — Tournament Registration

## Description

Teams register for tournaments.

---

## Validation

Registration must be open.

Team must satisfy game rules.

No duplicate registrations.

---

## Output

Registration confirmed.

---

## Errors

Tournament closed.

Tournament full.

Already registered.

---

# Feature 5 — Live Brackets

## Description

Automatically generate tournament brackets.

---

## Types

- Single Elimination
- Double Elimination

---

## Features

Auto generation.

Live updates.

Winner progression.

Bracket sharing.

---

## Output

Updated bracket.

---

## Success

Bracket generated.

