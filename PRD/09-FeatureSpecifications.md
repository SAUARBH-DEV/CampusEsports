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

---

# Feature 6 — Player Profile

## Description

Every student has a personalized gaming profile that showcases their identity, tournament history, achievements, and statistics.

---

## Users

- Student
- Organizer

---

## Inputs

- Name
- Profile Photo
- Bio
- College
- Preferred Games
- Social Links

---

## Outputs

Professional player profile.

---

## Features

- Edit profile
- Upload avatar
- View achievements
- Tournament history
- Match history
- Win/Loss ratio
- Favorite games
- Current ranking

---

## Validation

Profile photo must be an image.

Bio maximum 300 characters.

---

## Business Rules

One profile per account.

Tournament history cannot be edited manually.

---

## Success

Profile updated successfully.

---

# Feature 7 — Notifications

## Description

Users receive important updates about tournaments and matches.

---

## Notification Types

- Tournament Registration
- Match Reminder
- Team Invitation
- Match Result
- Tournament Announcement
- Organizer Announcement

---

## Delivery

- In-App
- Email

---

## Features

- Mark as Read
- Delete Notification
- Notification History

---

## Success

Notification delivered.

---

# Feature 8 — Search

## Description

Users can search for tournaments, colleges, teams, and players.

---

## Search Categories

- Players
- Teams
- Colleges
- Tournaments

---

## Filters

- Game
- College
- Tournament Status
- Date
- Ranking

---

## Output

Relevant search results.

---

## Business Rules

Search should support partial matching.

Recent searches stored locally.

---

# Feature 9 — Leaderboards

## Description

Display rankings for players, teams, and colleges.

---

## Categories

- Overall
- Game-wise
- Monthly
- Annual

---

## Metrics

- Wins
- Losses
- Points
- Win Rate
- Tournament Titles

---

## Features

- Filter leaderboard
- Search leaderboard
- Top Players
- Top Teams
- Top Colleges

---

# Feature 10 — Admin Dashboard

## Description

Administrators manage the complete Kurukshetra platform.

---

## Features

- User Management
- Tournament Management
- College Management
- Reports
- Analytics
- Moderation

---

## Permissions

Create

Read

Update

Delete

Suspend

Verify

---

## Business Rules

Only Super Admins have full access.

---

# Feature 11 — Organizer Dashboard

## Description

Organizers manage tournaments from a centralized dashboard.

---

## Features

- Dashboard Overview
- Tournament Statistics
- Team Management
- Match Scheduling
- Registration Approval
- Announcement Center

---

## Outputs

Tournament analytics.

Participation statistics.

Upcoming matches.

---

# Feature 12 — College Dashboard

## Description

Each college has its own dashboard to monitor esports activities.

---

## Features

- Registered Students
- Active Teams
- Tournament Participation
- Rankings
- Analytics
- Event History

---

## Future Features

- Official College Page

- Campus Clubs

- Campus Events

