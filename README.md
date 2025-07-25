# 🔒 GoAuth: Lightweight JWT Auth API (Golang)

**GoAuth** is a production-ready, secure, and minimal authentication API written in **Go (Golang)**. It handles user sign-up, login, logout, and token refresh using **JWT** for stateless authentication, **bcrypt** for secure password hashing, and **Redis** for token blacklisting. The project uses **PostgreSQL** as the primary user data store and **Gorilla Mux** for routing.

This API is designed to be clean, easy to extend, and ready to plug into any web or mobile backend. It follows best practices for building modern and secure authentication systems.


## ✨ Features

- ✅ Secure user registration and login
- 🔑 JWT token-based stateless authentication
- 🔄 Token refresh mechanism with expiry checks
- 🚪 Logout using Redis-based token blacklist
- 👤 Role-based access control (Admin/User)
- 🔐 Password hashing using bcrypt
- 🧩 Modular code structure with middleware
- 🌐 Swagger/OpenAPI documentation
- 🐳 Dockerized for easy deployment


## 🚀 Tech Stack

- Language: **Go (Golang)**
- Router: **Gorilla Mux**
- Database: **PostgreSQL**
- Auth: **JWT** & **bcrypt**
- Cache: **Redis** (for blacklisting tokens)
- Docs: **Swagger (OpenAPI 3.0)**
- Container: **Docker**


## 📂 Project Structure

```
goauth-jwt-auth-api-golang/
├── main.go
├── Dockerfile
├── go.mod / go.sum
├── config/
├── controllers/
├── middleware/
├── models/
├── routes/
├── utils/
├── frontend/
│   └── index.html
├── swagger.yaml
└── README.md
```


## ⚙️ Setup Instructions

### 1️⃣ Prerequisites

- Go 1.20+ installed
- PostgreSQL and Redis running locally or via Docker
- Git

### 2️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/goauth-jwt-auth-api-golang.git
cd goauth-jwt-auth-api-golang
```

### 3️⃣ Update Config

Edit the `config/config.go` file to match your DB/Redis credentials.

### 4️⃣ Run the Server

```bash
go run main.go
```

The server will start on `http://localhost:8000`


## 🧪 API Endpoints

| Method | Endpoint           | Description              | Auth |
|--------|--------------------|--------------------------|------|
| POST   | `/signup`          | Register new user        | ❌   |
| POST   | `/login`           | Login & get tokens       | ❌   |
| POST   | `/refresh`         | Refresh access token     | ✅   |
| POST   | `/logout`          | Logout & blacklist token | ✅   |
| GET    | `/protected/user`  | User-only route          | ✅   |
| GET    | `/protected/admin` | Admin-only route         | ✅   |


## 🔐 Authentication Flow

1. User registers via `/signup`
2. Logs in via `/login` and gets `access_token` and `refresh_token`
3. Access protected routes with `Authorization: Bearer <token>`
4. Use `/refresh` to obtain a new access token
5. Use `/logout` to invalidate current token


## 🐳 Docker Support

Build and run using Docker:

```bash
docker build -t goauth-api .
docker run -p 8000:8000 goauth-api
```


## 📖 API Docs (Swagger)

Serve the `swagger.yaml` with [Swagger UI](https://swagger.io/tools/swagger-ui/) or import into [Postman](https://www.postman.com/).
