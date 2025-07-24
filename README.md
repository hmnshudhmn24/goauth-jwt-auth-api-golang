# 🔒 GoAuth: Lightweight JWT Auth API

A secure and production-ready user authentication API built in **Go (Golang)** that provides a complete solution for managing users, roles, and sessions using modern best practices. This project uses **JWT tokens** for stateless authentication, **bcrypt** for secure password hashing, and **Redis** to implement token blacklisting for logout functionality.

It is designed to be minimal, extensible, and easy to deploy in any backend system. Perfect for developers who need a ready-made authentication system with secure login, token refresh, logout, and route protection — all out of the box.

Whether you're building a web app, mobile backend, or microservice, **GoAuth** offers a solid foundation for handling authentication securely and efficiently.

---

## 🚀 Features

- 🔐 **Signup/Login** with hashed password storage  
- 🔄 **Token refresh** with automatic expiration handling  
- 🚫 **Logout + Token blacklist** using Redis  
- 🛡️ **Protected Routes** with middleware  
- 👤 **User roles** embedded in JWT claims  
- 🧪 Fully structured for easy testing and expansion  

---

## 🛠️ Tech Stack

| Layer             | Tech Used          |
|------------------|--------------------|
| Language          | Go (Golang)        |
| Routing           | Gorilla Mux        |
| Database          | PostgreSQL         |
| Token Management  | JWT (HS256)        |
| Caching/Blacklist | Redis              |
| Password Hashing  | bcrypt             |

---

## 📁 Project Structure

goauth-jwt-auth-api-golang/
├── main.go
├── go.mod
├── Dockerfile
├── swagger.yaml
├── README.md
└── frontend/
└── index.html
