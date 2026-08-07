# Bolt-to-Backend Demo
### Turning an AI-Generated Frontend Into a Real, Working Product

---

## The Problem This Solves

Tools like Bolt, Lovable, and v0 generate polished frontends fast — but they ship with mock data, placeholder logic, and no real backend. This project demonstrates exactly what it takes to close that gap: a production-ready Node.js backend with real authentication, real data handling, and real error management.

---

## What This Backend Does

- User registration with secure password hashing (bcryptjs)
- User login with JWT token generation
- Protected routes using JWT authentication
- Proper error handling on every endpoint
- Environment-based configuration (no hardcoded secrets)

---

## Tech Stack

- **Runtime:** Node.js
- **Framework:** Express.js
- **Authentication:** JSON Web Tokens (JWT)
- **Password Security:** bcryptjs
- **Environment Config:** dotenv
- **CORS:** enabled for frontend connection

---

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/register | Register a new user |
| POST | /api/login | Login and receive JWT token |
| GET | /api/profile | Access protected route with token |

---

## How to Run Locally

```bash
# Clone the repo
git clone https://github.com/racheal160/bolt-backend-demo

# Install dependencies
npm install

# Start the server
node src/server.js
```

Server runs on http://localhost:3000

---

## Example Usage

**Register a user:**
```bash
curl -X POST http://localhost:3000/api/register \
  -H "Content-Type: application/json" \
  -d '{"name":"John Doe","email":"john@example.com","password":"password123"}'
```

**Login:**
```bash
curl -X POST http://localhost:3000/api/login \
  -H "Content-Type: application/json" \
  -d '{"email":"john@example.com","password":"password123"}'
```

---

## Why This Matters for Real Projects

Most AI-generated frontends assume a backend exists. This project is the backend they assume — built to production standards, not just demo standards.