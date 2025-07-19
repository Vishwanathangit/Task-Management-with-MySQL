
# 📝 Full-Stack Task Manager App (MySQL + Express + React)

A full-stack task management web application where users can create, view, edit, soft-delete, restore, and permanently delete tasks. It features a modern UI built with React and Tailwind CSS, and a backend API built using Express.js, Sequelize ORM, and MySQL.

---

## 🧰 Tech Stack

### Frontend
- React (with Vite)
- Tailwind CSS
- Axios
- Lucide-react icons

### Backend
- Node.js + Express.js
- Sequelize ORM
- MySQL Database
- dotenv

---

## 📂 Project Structure

```
project-root/
├── backend/
│   ├── config/
│   │   ├── config.js
│   │   └── database.js
│   ├── migrations/
│   │   ├── 20250626051833-create-task.js
│   │   └── 20250626130344-init-tasks-table.js
│   ├── models/
│   │   ├── Task.js
│   │   └── index.js
│   ├── routes/
│   │   └── taskRoutes.js
│   ├── index.js (Entry point)
│   └── .sequelizerc.cjs
│
├── frontend/
│   ├── public/
│   │   └── index.html
│   ├── src/
│   │   ├── api.js
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   ├── index.css
│   │   ├── pages/
│   │   │   ├── TaskPage.jsx
│   │   │   └── TaskListPage.jsx
│   │   └── components/
│   │       ├── TaskForm.jsx
│   │       └── TaskItem.jsx
│   ├── vite.config.js
│   └── eslint.config.js
│
├── .env (You must create this)
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
```

---

### 2. Set Up Environment Variables

Create a `.env` file in the `backend/` folder:

```env
PORT=3000
DB_USER=your_mysql_user
DB_PASSWORD=your_mysql_password
DB_NAME=task_db
DB_HOST=localhost
```

---

### 3. Database Setup

Make sure MySQL is running, then run:

```bash
cd backend
npx sequelize-cli db:create
npx sequelize-cli db:migrate
```

---

### 4. Run Backend Server

```bash
cd backend
npm install
node index.js
```

Your backend will run on: [http://localhost:3000](http://localhost:3000)

---

### 5. Run Frontend

```bash
cd frontend
npm install
npm run dev
```

Your frontend will run on: [http://localhost:5173](http://localhost:5173)

---

## ⚙️ Features

- ✅ Create a new task with title and optional description
- ✏️ Edit existing tasks
- ✅ Mark tasks as complete/incomplete
- 🗑️ Soft delete (hide) tasks
- ♻️ Restore soft-deleted tasks
- ❌ Permanently delete tasks
- 💡 LocalStorage-based soft delete logic for frontend experience
- 📋 Filter tasks by status (In Progress / Completed)
- 📱 Fully responsive and modern UI

---

## 📦 API Endpoints (Backend)

| Method | Endpoint                      | Description                      |
|--------|-------------------------------|----------------------------------|
| GET    | `/api/tasks`                 | Get all active tasks             |
| GET    | `/api/tasks?includeInactive=true` | Get all tasks including inactive |
| GET    | `/api/tasks/:id`             | Get a task by ID                 |
| POST   | `/api/tasks`                 | Create a new task                |
| PUT    | `/api/tasks/:id`             | Update a task                    |
| DELETE | `/api/tasks/:id`             | Soft delete a task               |
| POST   | `/api/tasks/:id/restore`     | Restore a soft-deleted task      |
| DELETE | `/api/tasks/:id/permanent`   | Permanently delete a task        |

---

## 🛠️ Future Improvements

- ✅ Add user authentication
- 🗃️ Pagination & search for large task lists
- ⏰ Task due dates and reminders
- 📊 Analytics dashboard

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).
