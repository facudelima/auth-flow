# Auth Flow

A modern authentication system implementation showcasing secure user authentication and authorization flows.

## Features

- 🔐 Secure user authentication
- 📧 Email verification
- 🔄 Password reset functionality
- 🎫 JWT token-based authentication
- 🛡️ Protected routes
- 🔒 Role-based access control

## Tech Stack

- Node.js
- Express.js
- MongoDB
- JWT

## Prerequisites

- Node.js (v18 or higher)
- MongoDB
- npm or yarn

## Installation

1. Clone the repository:
```bash
git clone https://github.com/facudelima/auth-flow.git
cd auth-flow
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
# .env
PORT=5000
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
EMAIL_SERVICE=your_email_service
EMAIL_USER=your_email
EMAIL_PASSWORD=your_email_password
```

## Running the Application

Start the server:
```bash
npm run dev
```

The API will be available at `http://localhost:5000`

## API Endpoints

- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/verify-email` - Email verification
- `POST /api/auth/forgot-password` - Password reset request
- `POST /api/auth/reset-password` - Password reset
- `GET /api/auth/profile` - Get user profile (protected)

## Security Features

- Password hashing using bcrypt
- JWT token authentication
- Email verification
- Rate limiting
- CORS protection
- XSS protection
- Input validation

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

Facu de Lima - [GitHub Profile](https://github.com/facudelima)

## Acknowledgments

- Thanks to all contributors who have helped with this project
- Special thanks to the open-source community for their invaluable tools and libraries 