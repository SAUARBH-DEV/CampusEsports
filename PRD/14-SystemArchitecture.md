# Kurukshetra System Architecture

---

Version: 1.0

Last Updated: 28 July 2026

Prepared By: Saurabh Singh

---

# Purpose

This document describes the overall technical architecture of Kurukshetra.

It explains how the frontend, backend, database, authentication, storage, notifications, analytics, and third-party services interact to build a scalable and maintainable platform.

---

# High-Level Architecture

Kurukshetra follows a modern cloud-native architecture.

Frontend

↓

API Layer

↓

Business Logic

↓

Database

↓

Storage

↓

Real-Time Services

↓

Analytics

---

# Technology Stack

Frontend

- Next.js
- React
- TypeScript
- Tailwind CSS
- shadcn/ui

Backend

- Next.js Route Handlers
- Supabase

Authentication

- Clerk

Database

- PostgreSQL

Storage

- Supabase Storage

Deployment

- Vercel

Version Control

- GitHub

---

# System Diagram

Users

↓

Browser

↓

Next.js Frontend

↓

Clerk Authentication

↓

API Layer

↓

Supabase PostgreSQL

↓

Storage

↓

Realtime Engine

↓

Analytics

---

# Frontend Architecture

Pages

↓

Layouts

↓

Components

↓

Hooks

↓

API Services

↓

State Management

↓

UI Components

---

# Backend Architecture

Authentication Layer

↓

Authorization Layer

↓

Business Logic

↓

Database Layer

↓

Storage Layer

↓

Notification Layer

---

# Authentication Flow

User

↓

Login

↓

Clerk

↓

JWT Token

↓

Backend Validation

↓

Dashboard

---

# Tournament Flow

Organizer

↓

Create Tournament

↓

Database

↓

Tournament Published

↓

Students View Tournament

↓

Registration

↓

Bracket Generation

↓

Matches

↓

Leaderboard Update

---

# Team Flow

Student

↓

Create Team

↓

Invite Members

↓

Members Accept

↓

Register Tournament

↓

Play Matches

---

# File Upload Flow

User

↓

Upload Image

↓

Supabase Storage

↓

Image URL Generated

↓

Database Updated

↓

Displayed on Platform

---

# Notification Flow

Event

↓

Backend

↓

Notification Service

↓

Database

↓

Email

↓

In-App Notification

---

# Real-Time Services

Realtime updates include:

- Live Brackets
- Match Status
- Leaderboards
- Notifications
- Tournament Registrations

---

# Security Layers

HTTPS

↓

Authentication

↓

Authorization

↓

Input Validation

↓

Rate Limiting

↓

Database Security

↓

Audit Logging

---

# Third-Party Integrations

Clerk

Authentication

Supabase

Database

Storage

Realtime

Vercel

Deployment

GitHub

Source Control

Resend

Emails

Cloudflare (Future)

CDN & Security

---

# Scalability

Phase 1

Single College

↓

Phase 2

Multiple Colleges

↓

Phase 3

NIT Network

↓

Phase 4

National Platform

↓

Phase 5

International Expansion

---

# Monitoring

Application Logs

Performance Metrics

Error Tracking

Database Health

Storage Usage

API Monitoring

Authentication Logs

---

# Disaster Recovery

Daily Database Backup

Storage Backup

Version Control

Rollback Strategy

Recovery Documentation

---

# Conclusion

Kurukshetra is designed using a modular, cloud-native architecture with Next.js, Clerk, Supabase, PostgreSQL, and Vercel.

This architecture provides scalability, security, and maintainability while supporting future growth from a single college to a nationwide platform.
