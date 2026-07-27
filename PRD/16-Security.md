# Kurukshetra Security Architecture

---

Version: 1.0

Last Updated: 28 July 2026

Prepared By: Saurabh Singh

---

# Purpose

This document defines the security architecture of Kurukshetra.

It covers authentication, authorization, API protection, database security, infrastructure security, monitoring, incident response, and best practices required to protect user data and platform integrity.

---

# Security Principles

Kurukshetra follows a "Security by Design" approach.

Core Principles

- Least Privilege
- Zero Trust
- Defense in Depth
- Secure by Default
- Privacy First
- Audit Everything
- Fail Securely

---

# Authentication

Provider

Clerk Authentication

Supported Methods

- Email & Password
- Google Login
- OTP Verification (Future)

Security Features

- Secure Sessions
- JWT Tokens
- Email Verification
- Password Reset
- Session Expiration

---

# Authorization

Role-Based Access Control (RBAC)

Roles

Student

Organizer

College Admin

Super Admin

Permissions

Each role can only access the features assigned to it.

---

# Password Policy

Minimum Length

8 Characters

Recommended

12+ Characters

Requirements

- Uppercase Letter
- Lowercase Letter
- Number
- Special Character

Passwords are never stored in plain text.

---

# Session Security

- Secure Cookies
- Automatic Session Expiration
- Session Revocation
- Logout from All Devices (Future)
- Device Tracking (Future)

---

# API Security

All APIs require authentication except public endpoints.

Security Measures

- JWT Verification
- Request Validation
- Input Sanitization
- Rate Limiting
- Request Logging
- Role Validation

---

# Database Security

Platform

Supabase PostgreSQL

Security Features

- Row Level Security (RLS)
- Foreign Key Constraints
- Indexes
- Encrypted Connections
- Automatic Backups

---

# Row Level Security Policies

Students

Can only view and edit their own profile.

Organizers

Can manage only their own tournaments.

College Admins

Can view only their own college data.

Super Admins

Have full administrative access.

---

# File Upload Security

Allowed Types

- JPG
- PNG
- WEBP
- PDF

Maximum Size

10 MB

Validation

- MIME Type Check
- File Size Validation
- Virus Scan (Future)
- Unique File Names

---

# Input Validation

Validate

- Email
- Phone Number
- Tournament Name
- Team Name
- URLs

Sanitize

- HTML
- SQL Inputs
- JavaScript

---

# Web Security

Protect Against

- SQL Injection
- Cross-Site Scripting (XSS)
- Cross-Site Request Forgery (CSRF)
- Clickjacking
- Broken Authentication
- Session Hijacking

---

# Rate Limiting

Protect APIs from abuse.

Examples

Login

5 attempts / minute

Registration

3 requests / minute

Search

100 requests / minute

General API

300 requests / minute

---

# Audit Logging

Record

- Login
- Logout
- Tournament Creation
- Registration Approval
- Match Result Update
- User Suspension
- Admin Actions

---

# Security Monitoring

Monitor

- Failed Logins
- Suspicious Activity
- API Errors
- Database Errors
- Storage Usage
- Server Health

---

# Backup Strategy

Daily Database Backup

Weekly Full Snapshot

Monthly Archive

Storage Backup

Recovery Testing Every Quarter

---

# Incident Response Plan

Detect

↓

Investigate

↓

Contain

↓

Recover

↓

Review

↓

Improve

---

# User Privacy

Collect only necessary data.

Users can

- View their data
- Edit profile information
- Delete account (subject to platform policies)
- Export personal data (Future)

The platform should clearly explain how user data is used and protected.

---

# Security Checklist

| Item | Status |
|--------|--------|
| HTTPS | ✅ |
| Authentication | ✅ |
| Authorization | ✅ |
| JWT Validation | ✅ |
| Row Level Security | ✅ |
| Rate Limiting | ✅ |
| Input Validation | ✅ |
| Audit Logs | ✅ |
| Backups | ✅ |
| Monitoring | ✅ |

---

# Conclusion

Kurukshetra follows modern security best practices with secure authentication, role-based authorization, database protections, API validation, monitoring, and backup strategies.

Security is treated as a core design principle rather than an afterthought, ensuring that the platform can safely support students, organizers, colleges, and future nationwide growth.

