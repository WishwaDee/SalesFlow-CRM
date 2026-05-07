# 🚀 SalesFlow CRM - Lead Management System

A professional, high-performance Customer Relationship Management (CRM) system designed for small sales teams. This application streamlines lead tracking, pipeline management, and data visualization using the modern MERN stack.

---

## 📑 Table of Contents
- [Project Overview](#-project-overview)
- [Tech Stack](#%EF%B8%8F-tech-stack)
- [Key Features](#-key-features)
- [Getting Started](#-getting-started)
- [Environment Variables](#-environment-variables)
- [Test Credentials](#-test-credentials)
- [Project Structure](#-project-structure)
- [Reflection & Architecture](#-reflection--architecture)
- [Known Limitations](#-known-limitations)

---

## 🎯 Project Overview
SalesFlow CRM is built to help sales teams move prospects through a structured pipeline. It provides a centralized hub to manage contact information, track deal values, and collaborate via internal notes. The goal of this project was to demonstrate full-stack proficiency, secure authentication, and product-focused engineering.

## 🛠️ Tech Stack
- **Frontend:** React 18 (Vite), Tailwind CSS, Lucide Icons, React Router 7.
- **Backend:** Node.js, Express.js.
- **Database:** MongoDB (Mongoose ODM).
- **Authentication:** JSON Web Tokens (JWT) & Bcrypt.js hashing.
- **Communication:** Axios with interceptors for automatic token handling.

## ✨ Key Features
- **Secure Authentication:** Complete login flow with protected routes and persistent sessions.
- **Lead CRUD:** Full lifecycle management (Create, Read, Update, Delete) for sales leads.
- **Interactive Dashboard:** Real-time KPIs including Total Leads, Conversion rates, and Deal Values.
- **Visual Sales Pipeline:** Track leads through stages: *New, Contacted, Qualified, Proposal Sent, Won, Lost*.
- **Collaboration Tools:** A timestamped internal notes system for every lead.
- **Advanced Search & Filtering:** Instant multi-field search (Name/Email/Company) and status filtering.
- **Responsive Design:** A mobile-friendly, professional interface.

## 🏁 Getting Started

### Prerequisites
- **Node.js:** v16 or higher.
- **MongoDB:** A local instance running on `mongodb://localhost:27017/crm_db`.

### Installation
1. **Clone the Repo:**
   ```bash
   git clone <your-repo-url>
   cd CRM_Wishwa_Dilshan
   ```

2. **Install Dependencies:**
   I have included a root-level script to install all frontend and backend dependencies at once:
   ```bash
   npm run install-all
   ```

3. **Seed the Database:**
   Initialize the database with the required admin user and sample lead data:
   ```bash
   npm run seed
   ```

4. **Launch the App:**
   Run both the frontend and backend concurrently:
   ```bash
   npm run dev
   ```
   - **Frontend:** `http://localhost:5173`
   - **Backend:** `http://localhost:5000`

## 🔑 Environment Variables
The application uses a `.env` file in the `server/` directory:
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/crm_db
JWT_SECRET=your_secure_secret_here
NODE_ENV=development
```

## 🔐 Test Credentials
Use these to log in and test all features:
- **Email:** `admin@example.com`
- **Password:** `password123`

## 📁 Project Structure
```text
├── client/                 # React Frontend
│   ├── src/
│   │   ├── components/     # Reusable UI (Modals, Cards)
│   │   ├── context/        # Auth State Management
│   │   ├── pages/          # Main Views (Dashboard, Leads)
│   │   └── services/       # API configuration (Axios)
├── server/                 # Node/Express Backend
│   ├── src/
│   │   ├── config/         # DB & Token config
│   │   ├── controllers/    # Business Logic
│   │   ├── models/         # MongoDB Schemas
│   │   ├── routes/         # API Endpoints
│   │   └── middleware/     # Auth & Protection
└── package.json            # Orchestration scripts
```

## 🧠 Reflection & Architecture
This project implements a **Modular Monolith** architecture. 
- **Backend:** By separating logic into controllers and routes, we ensure the API is easy to test and extend. We use Mongoose middlewares (pre-save) to handle security concerns like password hashing automatically.
- **Frontend:** We leverage React Context for global authentication state, ensuring a seamless user experience. Tailwind CSS was chosen for its utility-first approach, allowing for a highly customized and professional design without bloated CSS files.

**Challenges Overcome:**
- Designing a robust filtering system that maintains performance as the lead count grows.
- Ensuring a smooth "Edit Mode" experience that provides immediate visual feedback.

## ⚠️ Known Limitations
- **File Uploads:** Currently supports text-based notes only (no document attachments).
- **Multi-user Roles:** Designed for a single "Admin" salesperson role for this assessment.

---
**Developed by Wishwa Dilshan**  
*Intern Developer - Full-Stack CRM Assessment*
