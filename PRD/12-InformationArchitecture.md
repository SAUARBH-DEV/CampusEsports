# Kurukshetra Information Architecture

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

This document defines the structure of the Kurukshetra platform, including pages, navigation, user roles, dashboards, and relationships between different parts of the application.

It serves as the blueprint for UI/UX design, frontend routing, backend APIs, and database architecture.

---

# Platform Structure

Kurukshetra consists of five major sections.

1. Public Website
2. Student Portal
3. Organizer Portal
4. College Portal
5. Super Admin Portal

---

# Public Website

Accessible without login.

Pages

- Home
- About
- Features
- Tournaments
- Leaderboards
- Colleges
- Blog
- Contact
- FAQ
- Privacy Policy
- Terms & Conditions
- Login
- Register

---

# Student Portal

Dashboard

Pages

- Dashboard
- My Profile
- My Teams
- My Tournaments
- Browse Tournaments
- Notifications
- Leaderboards
- Settings

---

# Organizer Portal

Dashboard

Pages

- Dashboard
- Create Tournament
- Tournament Management
- Registrations
- Matches
- Brackets
- Analytics
- Announcements
- Settings

---

# College Portal

Dashboard

Pages

- Dashboard
- Students
- Teams
- Tournaments
- Reports
- Rankings
- Analytics
- Settings

---

# Super Admin Portal

Dashboard

Pages

- Dashboard
- Users
- Colleges
- Organizers
- Reports
- Analytics
- Moderation
- Platform Settings

---

# Navigation Hierarchy

Home

├── Features

├── Tournaments

├── Leaderboards

├── Colleges

├── Blog

├── About

├── Contact

├── Login

└── Register

---

# Student Navigation

Dashboard

├── Home

├── My Profile

├── My Teams

├── Browse Tournaments

├── Registered Tournaments

├── Notifications

├── Leaderboards

└── Settings

---

# Organizer Navigation

Dashboard

├── Create Tournament

├── My Tournaments

├── Registrations

├── Matches

├── Brackets

├── Analytics

└── Settings

---

# Role Access Matrix

| Feature | Student | Organizer | College | Admin |
|----------|:-------:|:---------:|:--------:|:-----:|
| Register | ✅ | ✅ | ✅ | ❌ |
| Login | ✅ | ✅ | ✅ | ✅ |
| Create Tournament | ❌ | ✅ | ❌ | ✅ |
| Join Tournament | ✅ | ❌ | ❌ | ❌ |
| Manage Teams | ✅ | ✅ | ❌ | ✅ |
| Analytics | Limited | ✅ | ✅ | ✅ |
| User Management | ❌ | ❌ | ❌ | ✅ |

---

# Platform Hierarchy

Kurukshetra

│

├── Public Website

│

├── Authentication

│

├── Student Dashboard

│

├── Organizer Dashboard

│

├── College Dashboard

│

├── Super Admin Dashboard

│

└── Shared Services

     ├── Notifications

     ├── Search

     ├── Settings

     ├── Help Center

     └── Support

---

# Conclusion

The Information Architecture defines the structural blueprint of Kurukshetra.

It ensures that every user role has a clear navigation path, every feature belongs to the correct module, and the application remains scalable as new features are introduced.

