# Kurukshetra Database Design

---

Version: 1.0

Last Updated: 28 July 2026

Prepared By: Saurabh Singh

---

# Purpose

This document defines the logical and physical database architecture for Kurukshetra.

It includes entities, relationships, constraints, indexing strategy, storage, security policies, and scalability considerations.

The goal is to create a robust, scalable, and maintainable database suitable for a nationwide college gaming platform.

---

# Database Technology

Primary Database

PostgreSQL

Backend Platform

Supabase

Authentication

Clerk

File Storage

Supabase Storage

Caching (Future)

Redis

Search (Future)

Meilisearch

---

# Database Modules

The database is divided into the following domains:

- Authentication
- Users
- Colleges
- Teams
- Tournaments
- Registrations
- Matches
- Brackets
- Leaderboards
- Notifications
- Reports
- Analytics

---

# Core Entities

- User
- College
- Team
- Team Member
- Tournament
- Tournament Registration
- Match
- Match Result
- Bracket
- Leaderboard
- Badge
- Achievement
- Notification
- Report
- Organizer

---

# Entity Relationships

One College

↓

Many Students

One Student

↓

Many Teams

One Team

↓

Many Players

One Tournament

↓

Many Registrations

One Tournament

↓

Many Matches

One Match

↓

One Winner

One Player

↓

Many Achievements

One College

↓

Many Tournaments

---

# Naming Convention

Tables

snake_case

Examples

users

teams

matches

Columns

snake_case

Primary Key

id

Foreign Keys

user_id

team_id

college_id

created_at

updated_at

---

# Common Fields

id

created_at

updated_at

created_by

status

deleted_at (Soft Delete)

is_active

---

# users

Fields

id

clerk_id

name

email

phone

avatar_url

college_id

bio

role

xp

level

current_rank

created_at

updated_at

---

# colleges

id

name

city

state

country

logo

website

verified

ranking

created_at

---

# team_members

id

team_id

user_id

joined_at

role

---

# tournaments

## Purpose

Stores tournament information created by organizers.

## Owner Module

Tournament Management

## Fields

id

organizer_id

title

description

game

banner_url

format

status

registration_start

registration_end

start_date

end_date

max_teams

entry_fee

prize_pool

visibility

rules

created_at

updated_at

## Relationships

One Organizer → Many Tournaments

One Tournament → Many Registrations

One Tournament → Many Matches

---

# tournament_registrations

## Purpose

Stores all team registrations.

## Fields

id

tournament_id

team_id

status

registered_at

approved_by

notes

## Relationships

One Tournament

↓

Many Registrations

One Team

↓

Many Registrations

---

# matches

## Purpose

Stores every match.

## Fields

id

tournament_id

round

team_a

team_b

winner_team

score

scheduled_at

completed_at

status

created_at

## Status

Upcoming

Live

Completed

Cancelled

---

# match_results

## Purpose

Detailed result of each match.

## Fields

id

match_id

winner_team

loser_team

score

submitted_by

verified

remarks

---

# brackets

## Purpose

Tournament bracket structure.

## Fields

id

tournament_id

round

match_id

position

parent_match

status

---

# leaderboards

## Purpose

Stores rankings.

## Fields

id

user_id

team_id

college_id

game

points

wins

losses

rank

season

---

# notifications

## Purpose

Stores notifications.

## Fields

id

user_id

title

message

type

is_read

created_at

---

# achievements

## Purpose

Achievement badges.

## Fields

id

title

description

icon

xp_reward

badge_color

---

# user_achievements

## Purpose

Tracks earned achievements.

## Fields

id

user_id

achievement_id

earned_at

---

# reports

## Purpose

User reports and disputes.

## Fields

id

reporter_id

reported_user

type

description

status

resolved_by

resolved_at

---

# Storage Buckets

Supabase Storage Buckets

avatars

team-logos

college-logos

tournament-banners

match-screenshots

certificates

---

# Indexing Strategy

Indexes

email

college_id

team_id

tournament_id

match_id

game

status

created_at

---

# Foreign Key Relationships

users.college_id

→ colleges.id

teams.captain_id

→ users.id

team_members.team_id

→ teams.id

team_members.user_id

→ users.id

tournaments.organizer_id

→ users.id

registrations.team_id

→ teams.id

matches.tournament_id

→ tournaments.id

---

# Soft Delete

Instead of permanently deleting records:

deleted_at

is_active

This preserves historical tournament data.

---

# Audit Logs

Track:

User Login

Tournament Creation

Tournament Update

Registration Approval

Match Result Update

Admin Actions

Security Events

---

# Backup Strategy

Daily Backup

Weekly Snapshot

Monthly Archive

Disaster Recovery Testing

Point-in-Time Recovery (Future)

---

# Future Tables

sponsors

internships

gaming_clubs

shop

orders

payments

scholarships

messages

friendships

activity_feed

---

# Conclusion

The Kurukshetra database is designed using a modular PostgreSQL architecture on Supabase. It separates responsibilities into clear domains, supports future growth, and provides a secure foundation for a nationwide college gaming platform.
