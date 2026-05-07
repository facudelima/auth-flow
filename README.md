# 🔐 Auth Flow

> A modern authentication system implementation showcasing secure user authentication and authorization flows.

**Repository:** [https://github.com/facudelima/auth-flow](https://github.com/facudelima/auth-flow)
 
---
 
## 🚀 Features

- 🔐 **Secure user authentication** — Sign up and sign in with validated credentials
- 📧 **Email verification** — Verify user email before full access
- 🔄 **Password reset** — Forgot password and reset via email link
- 🎫 **JWT token-based auth** — Stateless, scalable session handling
- 🛡️ **Protected routes** — Middleware-guarded endpoints
- 🔒 **Role-based access control (RBAC)** — Permissions by user role

---

## 🛠️ Tech Stack

### Backend
- **Node.js**
- **Express.js**
- **MongoDB**
- **JWT** (JSON Web Tokens)
- **bcrypt** (password hashing)
- **Nodemailer** (email sending)

### Frontend
- 🚧 **Coming soon!** — React or similar stack planned

---

## ⚙️ Prerequisites

- **Node.js** v18 or higher
- **MongoDB** (local or Atlas)
- **npm** or yarn

---

## 📦 Installation

1. **Clone the repository:**

```bash
git clone https://github.com/facudelima/auth-flow.git
cd auth-flow
```

2. **Install dependencies:**

```bash
npm install
```

3. **Set up environment variables**

Create a `.env` file in the project root:

```env
# Server
PORT=5000
NODE_ENV=development

# Database
MONGODB_URI=mongodb://localhost:27017/auth-flow

# JWT
JWT_SECRET=your_jwt_secret_here
JWT_EXPIRES_IN=7d

# Email (for verification & password reset)
EMAIL_SERVICE=gmail
EMAIL_USER=your_email@gmail.com
EMAIL_PASSWORD=your_app_password
```

---

## ▶️ Running the Application

Start the development server:

```bash
npm run dev
```

The API will be available at **http://localhost:5000**

| Service   | URL                     |
| --------- | ----------------------- |
| API       | http://localhost:5000   |
| Health    | http://localhost:5000/api/health *(if available)* |

---

## 📡 API Endpoints

### Authentication

| Method | Endpoint                      | Description                    | Auth required |
| ------ | ----------------------------- | ------------------------------ | ------------- |
| POST   | `/api/auth/register`          | User registration              | No            |
| POST   | `/api/auth/login`             | User login                     | No            |
| POST   | `/api/auth/verify-email`       | Email verification             | No            |
| POST   | `/api/auth/forgot-password`   | Request password reset         | No            |
| POST   | `/api/auth/reset-password`     | Reset password (with token)    | No            |
| GET    | `/api/auth/profile`           | Get current user profile       | Yes (JWT)     |

---

## 🛡️ Security Features

- **Password hashing** — bcrypt with salt rounds
- **JWT authentication** — Access + refresh token strategy (if implemented)
- **Email verification** — Reduce fake signups and secure account recovery
- **Rate limiting** — Protect against brute force and abuse
- **CORS** — Configured allowed origins
- **XSS protection** — Sanitized inputs and secure headers
- **Input validation** — Request body validation (e.g. express-validator)
- **Helmet** — Secure HTTP headers *(recommended)*

---

## 📁 Suggested Project Structure

```
auth-flow/
├── src/
│   ├── config/
│   │   └── db.js
│   ├── controllers/
│   │   └── authController.js
│   ├── middleware/
│   │   ├── auth.js
│   │   └── validate.js
│   ├── models/
│   │   └── User.js
│   ├── routes/
│   │   └── auth.js
│   ├── utils/
│   │   └── email.js
│   └── server.js
├── .env
├── .env.example
└── package.json
```

---

## 📄 License

This project is licensed under the MIT License.

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a Pull Request
