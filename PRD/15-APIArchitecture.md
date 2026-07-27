# Kurukshetra API Architecture

---

Version: 1.0

Last Updated: 28 July 2026

Prepared By: Saurabh Singh

---

# Purpose

This document defines the API architecture for Kurukshetra.

It specifies API design principles, endpoint organization, request and response formats, authentication, authorization, validation, error handling, and versioning.

The goal is to create a secure, scalable, and developer-friendly API that supports the current MVP and future expansion.

---

# API Design Principles

The Kurukshetra API follows REST principles.

Design Goals

- Simple
- Consistent
- Secure
- Versioned
- Predictable
- Scalable
- Easy to document

---

# API Structure

/api/v1

Modules

/auth

/users

/colleges

/teams

/tournaments

/registrations

/matches

/brackets

/leaderboards

/notifications

/admin

---

# Authentication APIs

POST /auth/register

Create account

--------------------

POST /auth/login

Login

--------------------

POST /auth/logout

Logout

--------------------

POST /auth/reset-password

Reset password

--------------------

GET /auth/me

Current user

---

# User APIs

GET /users/me

GET /users/{id}

PATCH /users/me

DELETE /users/me

GET /users/{id}/achievements

GET /users/{id}/tournaments

---

# Team APIs

POST /teams

GET /teams

GET /teams/{id}

PATCH /teams/{id}

DELETE /teams/{id}

POST /teams/{id}/invite

POST /teams/{id}/join

POST /teams/{id}/leave

---

# Tournament APIs

GET /tournaments

POST /tournaments

GET /tournaments/{id}

PATCH /tournaments/{id}

DELETE /tournaments/{id}

POST /tournaments/{id}/publish

POST /tournaments/{id}/close

---

# Registration APIs

POST /registrations

GET /registrations

PATCH /registrations/{id}

DELETE /registrations/{id}

---

# Match APIs

GET /matches

GET /matches/{id}

POST /matches

PATCH /matches/{id}

POST /matches/{id}/result

POST /matches/{id}/dispute

---

# Bracket APIs

GET /brackets/{tournamentId}

POST /brackets/generate

PATCH /brackets/update

---

# Leaderboard APIs

GET /leaderboards

GET /leaderboards/players

GET /leaderboards/teams

GET /leaderboards/colleges

---

# Notification APIs

GET /notifications

PATCH /notifications/{id}/read

DELETE /notifications/{id}

---

# Admin APIs

GET /admin/users

GET /admin/reports

PATCH /admin/users/{id}

DELETE /admin/users/{id}

GET /admin/analytics

---

# Response Format

Success

```json
{
  "success": true,
  "data": {},
  "message": "Operation completed successfully"
}
```

Failure

```json
{
  "success": false,
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Tournament name is required."
  }
}
```

---

# HTTP Status Codes

200 OK

201 Created

400 Bad Request

401 Unauthorized

403 Forbidden

404 Not Found

409 Conflict

422 Validation Error

500 Internal Server Error

---

# API Security

JWT Authentication

Role Based Access

Rate Limiting

Input Validation

HTTPS Only

Request Logging

Audit Logs

---

# API Versioning

Current Version

v1

Future

v2

Older versions remain supported for a defined migration period.

---

# Conclusion

The Kurukshetra API architecture provides a consistent, secure, and scalable interface between the frontend and backend.

By organizing endpoints into logical modules and applying standardized responses, authentication, and versioning, the API will remain maintainable as the platform evolves.
