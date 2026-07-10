# Team Task Manager


A complete, production-ready full-stack Team Task Management platform built with React, Node.js (Express), MongoDB (Mongoose), and Tailwind CSS. It supports advanced user management, role-based permissions (Admins & Members), interactive Kanban boards, activity audit timelines, and customizable analytics dashboards.


---


## 🛠️ Technology Stack

- **Frontend:** React.js, Vite, Tailwind CSS v4, React Router v6, custom Fetch/Axios API client, Context API, Lucide Icons.
- **Backend:** Node.js, Express.js, Mongoose.
- **Database:** MongoDB.
- **Security:** JWT (JSON Web Tokens), Bcrypt.js (password hashing), Helmet (HTTP security headers), Express Rate Limit (API and auth endpoint throttling).

---

## 🚀 Getting Started

Follow these instructions to run the application locally on your machine.

### Prerequisites

- [Node.js](https://nodejs.org/) (v16.0 or higher recommended)
- [MongoDB](https://www.mongodb.com/) (running locally or a MongoDB Atlas connection string)

### 1. Project Setup
Configure your environment variables in the root directory. A `.env` file has been pre-configured for local MongoDB access:
- File location: `.env`
- Pre-filled MongoDB URI: `mongodb://127.0.0.1:27017/team_task_manager`

### 2. Install Dependencies
Run the following command at the root directory to install all packages for both frontend and backend concurrently:
```bash
npm run install-all
```

### 3. Seed the Database
Populate the database with default projects, tasks, user roles, and activity logs:
```bash
npm run seed --prefix backend
```

### 4. Launch the Development Environment
Run the unified command at the root workspace to launch the Express API and the Vite React server concurrently:
```bash
npm run dev
```
- Frontend will open at: `http://localhost:5173`
- Backend API will run at: `http://localhost:5000`

---

## 🔑 Demo Access Credentials

The database seeding script creates sample Administrator and Team Member accounts for testing:

| Account Type | Email | Password | Allowed Permissions |
| :--- | :--- | :--- | :--- |
| **Workspace Administrator** | `admin@example.com` | `password123` | Create, Edit, Delete projects and tasks; Invite team members; Full reports. |
| **Team Member** | `member@example.com` | `password123` | View assigned projects and tasks; Update task status via Kanban board; View progress. |

---

## 📁 Repository Structure

```
├── backend/
│   ├── config/         # Database configuration (db.js)
│   ├── controllers/    # Route controllers (auth, user, project, task, activity)
│   ├── models/         # Mongoose models (User, Project, Task, ActivityLog)
│   ├── middlewares/    # Custom middlewares (auth, validation, rateLimiter, error)
│   ├── routes/         # Express API routers
│   ├── utils/          # Seeder and project calculation helpers
│   └── server.js       # Express main entrypoint
├── frontend/
│   ├── src/
│   │   ├── components/ # Sidebar, Navbar, Kanban board
│   │   ├── context/    # AuthContext and NotificationContext (toasts)
│   │   ├── pages/      # Login, Signup, Dashboard, Projects, Tasks, Profile, 404
│   │   ├── services/   # Fetch API wrapper
│   │   ├── App.jsx     # Main routes and layouts
│   │   ├── main.jsx    # Client mounting entrypoint
│   │   └── index.css   # Tailwind CSS imports & animations
│   ├── index.html      # Document skeleton
│   └── vite.config.js  # Vite React & Tailwind configurations
├── package.json        # Main project concurrent launch script
└── .env                # Global environment variables
```
