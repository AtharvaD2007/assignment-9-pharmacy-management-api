# Pharmacy Management API

This is the solution for Assignment 09: Pharmacy & Healthcare Store API with RBAC & JWT.

## Setup Instructions

1. **Install Dependencies:**
   ```bash
   npm install
   ```

2. **Environment Variables:**
   Copy `.env.example` to `.env` and configure your `MONGO_URI` (either a local instance or MongoDB Atlas) and `JWT_SECRET`.
   ```bash
   cp .env.example .env
   ```

3. **Start the Application:**
   ```bash
   npm run dev
   ```

## Roles and Access
- **Customer**: Can browse medicines and place orders.
- **Pharmacist**: Can manage inventory (add, update), view expiring medicines, and approve orders (which deducts stock).
- **Admin**: Can do everything a Pharmacist can, plus delete medicines from the catalog.

## Registering Staff
Use the `/api/auth/register-staff` endpoint with the correct `secretKey` (default is `supersecret` from `.env.example`) to create Pharmacist and Admin users.
