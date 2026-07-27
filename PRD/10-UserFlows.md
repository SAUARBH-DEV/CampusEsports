# Kurukshetra User Flows

---

Version: 1.0

Last Updated: 27 July 2026

Founder: Saurabh Singh

---

# Introduction

This document defines how different users interact with Kurukshetra from login to completing their goals.

The objective is to ensure every feature has a clear navigation path before UI development begins.

---

# User Types

1. Student Player
2. Team Captain
3. Organizer
4. College Admin
5. Super Admin

---

# Flow 1 — Student Registration

Goal:
Create a player account.

Flow

Home Page
    ↓
Click Register
    ↓
Choose Student
    ↓
Enter Details
    ↓
Verify Email / OTP
    ↓
Create Profile
    ↓
Dashboard

---

# Flow 2 — Student Login

Goal:
Access personal dashboard.

Flow

Home Page
    ↓
Login
    ↓
Enter Email & Password
    ↓
Authentication
    ↓
Dashboard

---

# Flow 3 — Browse Tournament

Dashboard
    ↓
Browse Tournaments
    ↓
Filter Games
    ↓
View Tournament
    ↓
Read Rules
    ↓
Join Team OR Register

---

# Flow 4 — Create Team

Dashboard
    ↓
My Teams
    ↓
Create Team
    ↓
Enter Team Name
    ↓
Upload Logo
    ↓
Invite Members
    ↓
Team Created

---

# Flow 5 — Join Existing Team

Invitation Link
    ↓
Accept Invite
    ↓
Join Team
    ↓
Appear in Team Dashboard

---

# Flow 6 — Register Tournament

Browse Tournament
    ↓
Open Tournament
    ↓
Click Register
    ↓
Select Team
    ↓
Eligibility Check
    ↓
Registration Success

---

# Flow 7 — Match Day

Dashboard
    ↓
Upcoming Match
    ↓
Receive Notification
    ↓
Join Match
    ↓
Play Match
    ↓
Organizer Submits Result
    ↓
Leaderboard Updated

---

# Flow 8 — Player Profile

Dashboard
    ↓
Profile
    ↓
View Statistics
    ↓
Achievements
    ↓
Edit Profile
    ↓
Save Changes

---

# Flow 9 — Notifications

Dashboard
    ↓
Notification Bell
    ↓
Read Notification
    ↓
Open Related Page

---

# Flow 10 — Logout

Dashboard
    ↓
Profile
    ↓
Logout
    ↓
Home Page

---

# Organizer Flows

The following flows describe how tournament organizers manage competitions from creation to completion.

---

## Flow 11 — Organizer Registration

Goal:
Create an organizer account.

Flow

Home
    ↓
Register
    ↓
Choose Organizer
    ↓
Enter Organization Details
    ↓
Verify Email / OTP
    ↓
Organizer Dashboard

## Flow 12 — Create Tournament

Organizer Dashboard
    ↓
Create Tournament
    ↓
Enter Tournament Details
    ↓
Select Game
    ↓
Set Rules
    ↓
Set Registration Dates
    ↓
Upload Banner
    ↓
Publish Tournament

## Flow 13 — Manage Registrations

Organizer Dashboard
    ↓
Tournament
    ↓
View Registered Teams
    ↓
Approve / Reject Teams
    ↓
Registration Complete

## Flow 14 — Generate Brackets

Tournament Dashboard
    ↓
Registration Closed
    ↓
Generate Brackets
    ↓
Automatic Seeding
    ↓
Bracket Published

## Flow 15 — Schedule Matches

Tournament Dashboard
    ↓
Create Match
    ↓
Assign Date & Time
    ↓
Assign Venue
    ↓
Notify Teams

## Flow 16 — Update Results

Organizer Dashboard
    ↓
Select Match
    ↓
Enter Winner
    ↓
Update Score
    ↓
Leaderboard Updated

## Flow 17 — Declare Winners

Tournament Completed
    ↓
Verify Results
    ↓
Declare Champions
    ↓
Publish Rankings
    ↓
Issue Certificates

## Flow 18 — Organizer Analytics

Organizer Dashboard
    ↓
Analytics
    ↓
View Registrations
    ↓
View Revenue
    ↓
View Participation
    ↓
Download Reports

---

# Organizer Features Summary

| Feature | Status |
|----------|--------|
| Create Tournament | ✅ |
| Edit Tournament | ✅ |
| Manage Teams | ✅ |
| Schedule Matches | ✅ |
| Generate Brackets | ✅ |
| Update Results | ✅ |
| View Analytics | ✅ |
| Download Reports | ✅ |

---

# College Admin Flows

College administrators monitor and support esports activities within their institution.

---

## Flow 19 — Register College

Goal:
Register the college on Kurukshetra.

Flow

Register College
    ↓
Enter College Information
    ↓
Upload Verification Documents
    ↓
Admin Review
    ↓
College Approved
    ↓
College Dashboard

## Flow 20 — Verify Students

College Dashboard
    ↓
Pending Student Requests
    ↓
Verify Student
    ↓
Student Added to College

## Flow 21 — Monitor Tournaments

College Dashboard
    ↓
View Active Tournaments
    ↓
Track Student Participation
    ↓
View Results

## Flow 22 — College Analytics

College Dashboard
    ↓
Analytics
    ↓
Player Statistics
    ↓
Tournament Statistics
    ↓
Download Report

## Flow 23 — College Rankings

College Dashboard
    ↓
College Rankings
    ↓
Compare Performance
    ↓
View Achievements

---

# Super Admin Flows

Super Admins manage the complete Kurukshetra platform.

---
## Flow 24 — Admin Login

Admin Login
    ↓
Authentication
    ↓
Admin Dashboard

## Flow 25 — User Management

Dashboard
    ↓
Users
    ↓
Search User
    ↓
Edit
    ↓
Suspend
    ↓
Save

## Flow 26 — College Management

Dashboard
    ↓
Colleges
    ↓
Approve College
    ↓
Update Information

## Flow 27 — Report Moderation

Dashboard
    ↓
Reports
    ↓
Review
    ↓
Take Action
    ↓
Close Report

## Flow 28 — Platform Analytics

Dashboard
    ↓
Analytics
    ↓
View Users
    ↓
View Revenue
    ↓
View Growth

---

# Error Flows

## Login Failure

Login
    ↓
Wrong Password
    ↓
Show Error
    ↓
Retry

---

## Tournament Full

Register
    ↓
Tournament Full
    ↓
Show Message
    ↓
Join Waitlist

---

## Team Already Registered

Register
    ↓
Duplicate Registration
    ↓
Display Error

---

## Internet Connection Lost

Action
    ↓
Network Error
    ↓
Retry


---

# Notification Flow

System Event
    ↓
Generate Notification
    ↓
Store Notification
    ↓
Deliver to User
    ↓
User Opens Notification

---

# Global Navigation

Landing Page

↓

Login / Register

↓

Role Detection

↓

Student Dashboard
OR
Organizer Dashboard
OR
College Dashboard
OR
Admin Dashboard

---

# User Journey Summary

Student

Discover
↓

Register
↓

Create Profile
↓

Create / Join Team
↓

Register Tournament
↓

Play Match
↓

Win Tournament
↓

Gain XP
↓

Increase Ranking

-------------------

Organizer

Register
↓

Create Tournament
↓

Approve Teams
↓

Generate Brackets
↓

Manage Matches
↓

Declare Winners

-------------------

College

Register College
↓

Verify Students
↓

Monitor Events
↓

Download Reports

-------------------

Super Admin

Manage Platform
↓

Review Reports
↓

Approve Colleges
↓

Platform Analytics

---

# User Flow Checklist

| Flow | Status |
|--------|--------|
| Student | ✅ |
| Organizer | ✅ |
| College | ✅ |
| Super Admin | ✅ |
| Notifications | ✅ |
| Errors | ✅ |
| Navigation | ✅ |

