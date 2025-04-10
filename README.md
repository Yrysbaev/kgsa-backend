# KGSA Backend

This is the backend API for the **Kyrgyz Student Association (KGSA)** website at [kgsa.us](https://kgsa.us). It handles protected admin routes for posting updates, news, and events. Built with **Node.js**, **Express**, **MySQL**, and **Firebase Authentication**.

---

## 🚀 Tech Stack

- **Backend Framework**: Node.js + Express
- **Authentication**: Firebase Authentication (with Admin SDK)
- **Database**: MySQL
- **Hosting**: [Render](https://render.com), Railway, or your own VPS
- **Frontend**: Deployed separately at [kgsa.us](https://kgsa.us)

---

## 📦 Features

- ✅ User authentication via Firebase
- 🔐 Protected admin routes
- 📝 CRUD operations for posts (create, read, update, delete)
- 🧩 RESTful API structure
- 📄 MySQL integration

---

## 📁 Project Structure

```
kgsa-backend/
├── controllers/
│   └── postController.js
├── routes/
│   └── postRoutes.js
├── middlewares/
│   └── authMiddleware.js
├── models/
│   └── db.js
├── .env
├── server.js
└── package.json
```

---

## 🔐 Firebase Setup

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Create a project (or use an existing one)
3. Enable **Authentication** (email/password or Google)
4. Go to **Project Settings > Service Accounts**, click “Generate new private key”
5. Download and save it as `firebase-adminsdk.json` in your backend folder
6. Add Firebase Admin setup in your project

---

## 🔧 Environment Variables

Create a `.env` file in the root:

```
PORT=5000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=kgsa_db
FIREBASE_DB_URL=https://your-firebase-app.firebaseio.com
FIREBASE_PROJECT_ID=your-firebase-project-id
```

---

## ▶️ Getting Started

```bash
# Clone the repository
git clone https://github.com/kgsa-team/kgsa-backend.git

# Navigate into the folder
cd kgsa-backend

# Install dependencies
npm install

# Start the server
npm run dev
```

---

## 🛠 Sample Routes

| Method | Endpoint         | Description            |
|--------|------------------|------------------------|
| GET    | /posts           | List all posts         |
| GET    | /posts/:id       | Get a single post      |
| POST   | /posts           | Create a post (admin)  |
| PUT    | /posts/:id       | Update a post (admin)  |
| DELETE | /posts/:id       | Delete a post (admin)  |

---

## 👥 Contributors

- **Yrysbaev Maksatbek** – Project Lead, Developer

---

## 🌐 License

MIT License
