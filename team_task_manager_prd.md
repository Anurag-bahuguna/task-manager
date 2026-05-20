# Team Task Manager - Project Specification

## Overview
A task management platform with role-based access control (Admin/Member) built for efficiency and team collaboration.

## Data Models

### Users
- id, name, email, password, role (Admin/Member), profileImage, createdAt

### Projects
- id, projectName, description, createdBy (Admin ID), teamMembers (User IDs), deadline, status (Active/Archived), createdAt

### Tasks
- id, taskTitle, description, assignedTo (User ID), projectId, priority (Low/Medium/High), status (Pending/In Progress/Completed), dueDate, createdAt

## Screen Requirements

### 1. Authentication
- Login & Signup pages with form validation.

### 2. Admin Dashboard
- Stats: Total projects, total tasks, completed/pending/overdue tasks.
- Visuals: Progress charts (radial/bar).
- List: Recent activity or upcoming deadlines.

### 3. Project Management
- List view of all projects with search/filter.
- Create/Edit Project modals/pages.
- Detail view showing team members and task breakdown.

### 4. Task Management
- Global task list and project-specific task lists.
- Task Creation: Assignee, priority, due date, project association.
- Status updates: Drag-and-drop or dropdown status changes.

### 5. User Profile
- Personal info, role display, and "My Tasks" summary.

## Tech Stack (Reference)
- Frontend: React + Tailwind CSS
- Backend: Node.js + Express.js
- Database: MongoDB
- Auth: JWT + Bcrypt
