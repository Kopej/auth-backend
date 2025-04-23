User Authentication API

A secure and scalable user authentication system built with Node.js, Express, MongoDB (Atlas), and JWT. This API provides endpoints for user registration and login, and is ready for integration with web or mobile applications.

---

Features

- User registration with hashed passwords (bcrypt)
- User login with JWT token generation
- Protected route example (`/dashboard`)
- MongoDB Atlas for cloud database
- CORS-enabled for frontend integration
- Ready for deployment on Render

---

Base URL (Local)

http://localhost:5000/api/auth


> For deployed version, use: 'https://auth-backend-j0sy.onrender.com'

---

API Endpoints

Register a New User

URL:`POST /register`  
Headers:
Content-Type: application/json

Request Body:
json
{
  "username": "john",
  "email": "john@example.com",
  "password": "password123"
}
Response:

{
  "token": "jwt_token_here"
}

Login User
URL: POST /login

Headers:

Content-Type: application/json
Request Body:

{
  "username": "john",
  "password": "password123"
}
Response:

{
  "token": "jwt_token_here"
}

Protected Dashboard
URL: GET /dashboard
Requires JWT token in the Authorization header.

Response:

{
  "message": "Welcome to your dashboard"
}

Tech Stack
Backend: Node.js, Express

Database: MongoDB Atlas, Mongoose

Auth: bcryptjs, JSON Web Tokens (JWT)

Tools: Postman, Render, GitHub

How to Test Locally
Clone the repo:

git clone https://github.com/your-username/auth-backend.git
cd auth-backend
Install dependencies:

npm install
Create a .env file in the root and add:

MONGO_URI=your_mongo_atlas_connection_string
JWT_SECRET=your_jwt_secret_key

Start the server:

node server.js
Test the endpoints via Postman at http://localhost:5000/api/auth.

Folder Structure

auth-backend/
│
├── models/
│   └── User.js
├── routes/
│   └── auth.js
├── .env.example
├── server.js
├── package.json
└── README.md

Screenshots
See /screenshots folder or attached documentation for sample Postman tests.

Mobile App Integration
These endpoints are RESTful and can be used directly by a mobile app frontend (e.g., React Native or Flutter). Simply point mobile HTTP requests to:

https://auth-backend-j0sy.onrender.com

Author
Peter Sankale Kopejo
Backend Developer | GIS Analyst | Python Automation Enthusiast


This project is open-source and free to use under the MIT License.
