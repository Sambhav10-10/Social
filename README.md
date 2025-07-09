# 📱 KapotaConnect – Mini Social Media App

A lightweight social networking platform built as part of a CodeAlpha full-stack development internship.  
KapotaConnect enables users to create profiles, share posts, comment, and follow others—mimicking the core features of a modern social media platform.

---

## 📌 Project Overview

**Tech Stack:** Node.js, Express.js, EJS, SQLite/MySQL  
**Developer:** Honoured OneByte  
**Internship Duration:** Task 2 – CodeAlpha Internship

This project is designed to simulate real-world social media functionality, including:

- User authentication and session management  
- Post creation, viewing, and commenting  
- Following/unfollowing other users  
- Responsive UI and clean page navigation

---

## ✨ Features

### 👤 User Authentication
- Register and login with username & password
- Session-based authentication using `express-session`
- Logout functionality

### 📝 Posts & Comments
- Create text/image posts
- View all posts in a feed
- Comment on individual posts

### 🔗 Follow System
- Follow and unfollow other users
- View follower/following counts on profile

---

## 🚦 Application Routes

| Method | Route                    | Description                      |
|--------|--------------------------|----------------------------------|
| GET    | `/`                      | Homepage feed                    |
| GET    | `/register`              | Show user registration form      |
| POST   | `/register`              | Handle user signup               |
| GET    | `/login`                 | Show login form                  |
| POST   | `/login`                 | Handle user login                |
| GET    | `/logout`                | Log the user out                 |
| GET    | `/profile/:username`     | View user profile                |
| GET    | `/post/new`              | Show form to create post         |
| POST   | `/post/new`              | Submit new post                  |
| GET    | `/post/:id`              | View single post with comments   |
| POST   | `/post/:id/comment`      | Add comment to a post            |
| POST   | `/follow/:userId`        | Follow a user                    |
| POST   | `/unfollow/:userId`      | Unfollow a user                  |

---

## 🛠️ Installation & Setup

### Prerequisites
- Node.js
- SQLite (or MySQL configured)
- Git

### Steps

```bash
# 1. Clone the repo
git clone https://github.com/Honoured-1-byte/CodeAlpha_KapotaConnect.git
cd CodeAlpha_KapotaConnect

# 2. Install dependencies
npm install

# 3. Configure environment
cp .env.example .env
# Edit .env to set: DATABASE_URL, SESSION_SECRET, PORT

# 4. (Optional) Seed dummy users/posts
# node seedUsers.js

# 5. Run the app
npm start
