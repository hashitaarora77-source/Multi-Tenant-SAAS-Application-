# Multi Tenant SAAS Application 
A full-stack multi-tenant SaaS application with authentication and authorization.
# Multi-Tenant SAAS Application

## 🚀 Features
- **Multi-tenant Architecture:** Support for multiple tenants with isolated data  
- **Authentication:** JWT-based authentication with secure password hashing  
- **Authorization:** Protected routes requiring authentication  
- **Beautiful UI:** Dark-themed login page matching modern design standards  
- **Tenant Isolation:** Each tenant has their own data, theme, and branding  

---

## ⚙️ Setup

### 🔧 Backend
Navigate to the backend directory:
```bash
cd backend
Install dependencies:

npm install


Seed the database with sample data:

npm run seed


Start the backend server:

npm run dev


The API will be available at:
👉 http://localhost:4000
Tenant isolation ensures users can only access their tenant's data
Development
Backend uses Express 5 with ES modules
Frontend uses React 19 with Vite
Database: MongoDB with Mongoose
Authentication: JWT with jsonwebtoken
