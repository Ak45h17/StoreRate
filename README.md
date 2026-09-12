# StoreRate

A full-stack store rating platform built as a coding challenge for Roxiler Systems.

StoreRate allows users to discover stores, submit and update ratings, while administrators manage users, stores, and platform statistics. Store owners can monitor ratings and customer feedback for their assigned stores.

---

## Overview

StoreRate is a role-based web application built with:

- React + Vite frontend
- NestJS + TypeScript backend
- PostgreSQL database
- Prisma ORM
- JWT authentication

The application supports three roles:

- **ADMIN** — manages users, stores, roles, and platform statistics.
- **USER** — searches stores and submits or updates ratings.
- **STORE_OWNER** — monitors assigned stores, ratings, and customer feedback.

Authentication and authorization are implemented using JWT and role-based route protection.

---

## Key Features

### Admin

- Secure administrator login
- Dashboard statistics
- Total users
- Total stores
- Total ratings
- User role statistics
- Create users
- Create administrators
- Create store owners
- Create stores
- Assign stores to store owners
- Search users
- Filter users by name, email, address, and role
- Sort users ascending/descending
- Search stores
- Filter stores
- Sort stores ascending/descending
- View user details
- View store and store-owner rating information
- Logout

### Normal User

- User registration
- Secure login
- Store listing
- Search stores by name and address
- View overall store rating
- View personal submitted rating
- Submit ratings from 1–5
- Modify existing ratings
- Sort stores by name, address, and rating
- Filter stores by:
  - All Stores
  - Rated by Me
  - Not Rated
- Rating descriptions from Poor to Excellent
- Change password
- Logout

### Store Owner

- Secure owner login
- Owner dashboard
- View owner information
- View assigned stores
- View store details
- View average rating
- View total ratings
- View customer ratings
- Sort customer ratings
- Rating distribution from 1–5 stars
- Change password
- Logout

---

## UI Improvements

The final implementation includes several UI and usability improvements:

- Modern StoreRate branding and logo
- Improved dashboard statistics
- User rating filters
- Rating summary cards
- Rating descriptions such as "Very Good" and "Excellent"
- Store owner rating distribution
- Consistent branding across login, registration, admin, user, and owner pages
- Responsive dashboard layouts
- Improved visual organization of store and rating information

---

## Screenshots

Screenshots of the final implementation are available in the `ScreenShot` directory.

### Login / Registration

The authentication pages provide a clean interface for user login and registration with the updated StoreRate branding.

### User Dashboard

Users can search stores, view ratings, filter stores based on whether they have rated them, and submit or update ratings.

### Admin Dashboard

Administrators can view platform statistics and manage users and stores.

### Store Owner Dashboard

Store owners can view their stores, average ratings, customer ratings, and rating distribution.

### Change Password

Users and store owners can securely change their account passwords.

---

## Technology Stack

### Frontend

- React
- Vite
- React Router
- Axios
- Lucide React

### Backend

- NestJS
- TypeScript
- Prisma ORM
- PostgreSQL
- JWT Authentication
- Passport
- class-validator
- bcrypt

### Development Tools

- Node.js
- npm
- Git
- GitHub
- Docker
- Docker Compose

---

## Architecture

```text
                    ┌─────────────────────┐
                    │       Browser       │
                    │    React + Vite     │
                    └──────────┬──────────┘
                               │
                               │ HTTP / JSON
                               ▼
                    ┌─────────────────────┐
                    │      NestJS API     │
                    │                     │
                    │ Authentication      │
                    │ Authorization       │
                    │ Admin Module        │
                    │ User Module         │
                    │ Owner Module        │
                    │ Rating APIs         │
                    └──────────┬──────────┘
                               │
                               │ Prisma ORM
                               ▼
                    ┌─────────────────────┐
                    │     PostgreSQL      │
                    │                     │
                    │ Users               │
                    │ Stores              │
                    │ Ratings             │
                    └─────────────────────┘
