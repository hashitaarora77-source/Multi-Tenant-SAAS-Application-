# Multi-Tenant SAAS Application

A full-stack multi-tenant SaaS application featuring authentication, authorization, tenant isolation, modern UI, and complete backend–frontend integration using Express, React, and MongoDB.

## 🚀 Features
- Multi-tenant Architecture: Support for multiple tenants with isolated data
- Authentication: JWT-based authentication with secure password hashing
- Authorization: Protected routes requiring authentication
- Beautiful UI: Dark-themed login page matching modern design standards
- Tenant Isolation: Each tenant has their own data, theme, and branding

## ⚙️ Setup

### Backend
Navigate to backend directory:
```bash
cd backend
```

Install dependencies:
```bash
npm install
```

Seed the database:
```bash
npm run seed
```

Start backend server:
```bash
npm run dev
```

Backend runs at: **http://localhost:4000**

### Frontend
Navigate to frontend directory:
```bash
cd frontend
```

Install dependencies:
```bash
npm install
```

Start development server:
```bash
npm run dev
```

Frontend runs at: **http://localhost:5173**

## 📘 Usage
- Enter a tenant slug (e.g., `acme` or `globex`) in the tenant switcher
- Login to access the tenant-specific dashboard and resources

## 🔗 API Endpoints

### Authentication
- POST `/api/auth/register` – Register user
- POST `/api/auth/login` – Login
- GET `/api/auth/me` – Get current user
- POST `/api/auth/logout` – Logout

### Resources (Protected)
- GET `/api/resources` – Get all resources
- POST `/api/resources` – Create resource
- GET `/api/resources/:id` – Get resource by ID

### Tenants
- GET `/api/tenants` – List tenants
- GET `/api/tenants/me` – Get current tenant

### Themes
- GET `/api/themes/current.css` – Load tenant theme CSS

### Auth Header
```
Authorization: Bearer <token>
```

Or token sent automatically via HTTP-only cookies.

## 🗂️ Project Structure
```
ProjectApp/
├── backend/
│   ├── src/
│   │   ├── middleware/
│   │   │   ├── auth.js          # JWT middleware
│   │   │   └── tenantContext.js # Tenant context middleware
│   │   ├── models/
│   │   │   ├── User.js          # User model
│   │   │   ├── Tenant.js        # Tenant model
│   │   │   └── Resource.js      # Resource model
│   │   ├── routes/
│   │   │   ├── auth.js          # Auth routes
│   │   │   ├── resources.js     # Resource routes
│   │   │   ├── tenants.js       # Tenant routes
│   │   │   └── themes.js        # Theme routes
│   │   └── server.js            # Express server
│   └── seed/
│       └── seed.js              # DB seeder
└── frontend/
    ├── src/
    │   ├── components/
    │   │   ├── Login.jsx        # Login UI
    │   │   └── Login.css        # Login styles
    │   ├── App.jsx              # Main App
    │   └── styles.css           # Global styles
    └── vite.config.js
```

## 🔐 Security Notes
- Passwords hashed using bcrypt
- JWT tokens expire after 7 days
- HTTP-only cookies used when supported
- CORS configured safely
- Tenant isolation enforced strictly

## 🧰 Development Info
- Backend: Express 5 (ES Modules)
- Frontend: React 19 (Vite)
- Database: MongoDB with Mongoose
- Authentication: JWT with jsonwebtoken
