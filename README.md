🔐 Login System with User Details & File Access

Developer: Kuldeep Patel
Project: FOSSEE Osdag – Autumn 2026 Semester Internship Screening Task
Area: Software Development

📌 Project Overview

This project is a full-stack web application built with Django REST Framework and React.

The application focuses on secure user authentication, user details management, and file access. It provides a foundation for managing authenticated users and protecting application resources through JWT-based authentication.

✨ Features

1. User Registration

User signup with username, email, password, and password confirmation.

Validation for duplicate usernames and email addresses.

Password validation requiring a letter, number, and special character.

Passwords are stored using Django's password hashing.

2. User Login

Login using email and password.

Authentication handled through Django.

JWT access and refresh tokens are generated after successful authentication.

Invalid credentials return an appropriate error response.

3. Authenticated User Dashboard

Protected dashboard API endpoints.

User information can be retrieved by authenticated users.

User details include:

User ID

Username

Email

Active status

4. User Details Management

Authenticated API endpoints for retrieving, updating, and deleting user records.

Password updates use Django's secure password hashing mechanism.

5. File Upload

Supports file uploads through the Django backend.

Uploaded files are stored using Django's media storage.

File metadata is exposed through REST API endpoints.

Pagination is provided for file listings.

6. Image Upload

Supports image uploads.

Images are stored in the application's media directory.

Image records can be accessed through REST API endpoints.

7. REST API

The backend is implemented using Django REST Framework and provides API endpoints for authentication, users, files, and images.

🏗️ Project Structure

project/
├── backend/
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
├── taskapp/
│   ├── models.py
│   ├── serializers.py
│   ├── views.py
│   ├── urls.py
│   ├── admin.py
│   └── migrations/
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── vite.config.js
│
├── media/
├── manage.py
├── requirements.txt
└── README.md

🧰 Technology Stack

Layer

Technology

Backend

Python, Django

API

Django REST Framework

Authentication

JWT / Simple JWT

Frontend

React, Vite

UI

Tailwind CSS

Database

SQLite

File Storage

Django Media Storage

Version Control

Git & GitHub

⚙️ Backend Setup

1. Create a virtual environment

Windows:

python -m venv venv
venv\Scripts\activate

2. Install dependencies

pip install -r requirements.txt

3. Apply database migrations

python manage.py migrate

4. Start the Django development server

python manage.py runserver

The backend will be available at:

http://127.0.0.1:8000/

🔑 Main Authentication Flow

User
  │
  ├── Sign Up
  │      ↓
  │   Django User
  │
  └── Login
         ↓
    Authentication
         ↓
    JWT Access Token
         ↓
  Protected API
         ↓
 User / File Resources

🔒 Security

The application uses Django's built-in authentication system and JWT authentication for protected API resources.

Passwords are not stored as plain text. Authentication-protected endpoints require a valid access token.

For production deployment, additional security configuration such as HTTPS, environment-based secrets, secure cookie settings, and production database configuration should be applied.

👨‍💻 Developer

Kuldeep Patel
B.Tech Computer Science
VIT Bhopal University

📄 Internship Context

This repository is prepared as a screening-task project for the FOSSEE Osdag Autumn 2026 Semester Internship, with the selected area of interest being:

Login System with User Details & File Access

The implementation focuses on authentication, user management, REST APIs, and controlled access to uploaded resources.