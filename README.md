# Role-Based Job Management System

This project is a backend-first job management platform built to demonstrate
how I design, execute, and own real-world systems involving authentication,
authorization, APIs, and databases.

The focus of this project is correctness, clarity, and execution — not UI polish.

---

## Overview

The system supports multiple roles:
- Admin
- Company / Recruiter
- Job Seeker

The backend is the source of truth.  
All permissions, validations, and state transitions are enforced server-side.

The frontend is only responsible for consuming APIs and rendering data.

---

## Backend Design

The backend is built using Node.js, Express, and MongoDB.

Key design decisions:
- Clear separation of routes, controllers, and models
- JWT-based authentication
- Role-based authorization using middleware
- Centralized error handling
- Environment-based configuration

APIs are structured as:
- `/api/v1/user`
- `/api/v1/company`
- `/api/v1/job`
- `/api/v1/application`

Each route has a single responsibility and explicit access control.

---

## Authentication & Authorization

- Users authenticate using JWT tokens
- Roles determine access to protected routes
- Authorization logic is enforced at the middleware level
- The frontend cannot bypass backend permissions

This ensures that business rules are protected regardless of the client.

---

## Database Modeling

MongoDB is used with Mongoose for schema definition.

Core entities:
- Users
- Companies
- Jobs
- Applications

Schemas were designed before API implementation to avoid tight coupling
and inconsistent data flow.

---

## Execution & Ownership

This project involved full ownership from setup to deployment:
- Environment configuration and debugging
- MongoDB connection and schema setup
- API design and validation
- Authentication and authorization logic
- Local development setup and GitHub deployment

Issues such as database connection errors and environment mismatches
were resolved independently during development.

---

## Local Setup

### Backend
```bash
cd backend
npm install
npm run dev
```
Backend runs on `http://localhost:3000`

### frontend
```bash

cd frontend
npm install
npm run dev
```
Frontend runs on `http://localhost:5173`






