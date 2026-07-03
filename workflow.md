# Project Structure

## Repository Structure

```text
project/
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── config/
│   └── server.js
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── assets/
│   │   ├── services/
│   │   └── App.js
│   └── public/
│
├── database/
│   └── schema.sql
│
├── docs/
├── README.md
└── STRUCTURE.md
```

---

# Git Workflow

## Branch Structure

```text
main
├── <developer_name>_<feature_name>
├── <developer_name>_<feature_name>
└── ...
```

### 1. Update the Repository

```bash
git switch main
git pull origin main
```

### 2. Create a Feature Branch

```bash
git switch -c <developer_name>_<feature_name>
```

Example:

```bash
git switch -c rahul_login
```

### 3. Develop Your Feature

```bash
git add .
git commit -m "Add login functionality"
git push -u origin <developer_name>_<feature_name>
```

### 4. Merge into Main

```bash
git switch main
git pull origin main
git merge <developer_name>_<feature_name>
git push origin main
```

---

# Project Guidelines

* Create a separate branch for every new feature.
* Use meaningful commit messages.
* Test your changes before merging.
* Keep the `main` branch stable.
* Delete feature branches after they are merged if they are no longer needed.

---

# Database Schema

## Tables

### Users

| Column     | Type      | Description           |
| ---------- | --------- | --------------------- |
| id         | INT (PK)  | User ID               |
| name       | VARCHAR   | User name             |
| email      | VARCHAR   | Email address         |
| password   | VARCHAR   | Encrypted password    |
| created_at | TIMESTAMP | Account creation time |

### Example Relationships

```text
Users
  │
  ├── id (PK)
  ├── name
  ├── email
  └── password
```

> Add new tables and relationships here as the project grows.

---

# API Structure

```text
/api
├── /auth
├── /users
└── /health
```

---

# Naming Conventions

| Item       | Convention                        |
| ---------- | --------------------------------- |
| Branch     | `<developer_name>_<feature_name>` |
| Files      | camelCase or lowercase            |
| Components | PascalCase                        |
| Variables  | camelCase                         |
| Constants  | UPPER_SNAKE_CASE                  |

---

# Future Documentation

* Database ER Diagram
* API Endpoints
* Environment Variables
* Deployment Steps
* Testing Guide
* Coding Standards
