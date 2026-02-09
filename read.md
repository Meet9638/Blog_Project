# 📝 Laravel Blog Management System

A role-based Blog Management System built with **Laravel 12**, featuring **Readers, Authors, and Admins**, with full CRUD functionality, authentication, authorization, and an admin dashboard.

---

## 🚀 Features

### 🔐 Authentication & Roles
- User authentication (Login / Register)
- Role-based access:
  - **Reader** – View blog posts
  - **Author** – Create, edit, and manage own posts
  - **Admin** – Manage all posts, authors, readers, and categories

---

### 📖 Blog Module
- View all blog posts
- View single blog details
- Posts organized by **categories** and **tags**
- Pagination for blog listing

---

### ✍️ Author Features
- Create new blog posts
- Edit and delete own posts
- Auto role upgrade: **Reader → Author** on first post creation
- Tag management (comma-separated tags)

---

### 🛠️ Admin Dashboard
- Dashboard overview
- Manage all blog posts
- Manage authors and readers
- Block / unblock users
- Category management (CRUD)
- View total posts per author/category

---

### 🔐 Security
- Laravel Policies for authorization
- Middleware for admin and blocked users
- Role-based UI visibility
- Protection against unauthorized actions

---

## 🧱 Tech Stack

- **Framework**: Laravel 12
- **Language**: PHP 8+
- **Database**: MySQL
- **Frontend**: Blade + Bootstrap 5
- **Authentication**: Laravel Auth
- **Authorization**: Laravel Policies & Middleware

---

## 📂 Project Structure (Simplified)

app/
├── Http/Controllers/
│ ├── BlogController.php
│ ├── PostController.php
│ └── Admin/
│ ├── DashboardController.php
│ ├── UserController.php
│ └── CategoryController.php
├── Models/
│ ├── Post.php
│ ├── Category.php
│ ├── Tag.php
│ └── User.php
├── Policies/
│ └── PostPolicy.php

resources/views/
├── blog/
├── posts/
├── admin/
│ ├── posts/
│ ├── authors/
│ └── categories/
└── layouts/


---

---

## 🗄️ Database Tables

- users
- posts
- categories
- tags
- post_tag (pivot table)
- comments (optional)

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository
```bash
git clone https://github.com/your-username/laravel-blog-project.git
cd laravel-blog-project


2️⃣ Install dependencies
composer install

3️⃣ Environment setup
cp .env.example .env
php artisan key:generate


Update .env with your database credentials.


4️⃣ Run migrations
php artisan migrate

5️⃣ Run the application
php artisan serve

Visit:

http://127.0.0.1:8000



👥 User Roles & Access
Role |Permissions
Reader |	View all blog posts
Author |	Create & manage own posts
Admin	|Full system control

👥 admin
email : admin1@gmail.com
password:12345678

📌 Future Enhancements

Post approval workflow

Comment moderation

Search & filters

Post analytics

Email notifications



