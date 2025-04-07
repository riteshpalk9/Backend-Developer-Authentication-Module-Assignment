# Backend Auth API (Node.js + JWT)

A simple backend authentication system using Node.js, Express, MongoDB, and JWT.

## Features

- User Signup  
- User Login with JWT  
- Protected Routes  
- Logout (stateless)  
- CRUD operations for users  

## Tech Stack

- Node.js  
- Express.js  
- MongoDB (via Mongoose)  
- JWT for authentication  
- bcrypt for password hashing  

## Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/your-username/backend-auth-api.git
cd backend-auth-api
```

### 2. Install dependencies
```bash
npm install
```

### 3. Create `.env` file
Create a `.env` file in the root directory and add the following:
```
PORT=5000
MONGO_URI=mongodb://localhost:27017/backend-auth
JWT_SECRET=your_jwt_secret
```

### 4. Start the server
```bash
node app.js
```

## API Endpoints

| Method | Route              | Description         | Auth Required |
|--------|--------------------|---------------------|---------------|
| POST   | /api/users/signup  | Create a new user   | ❌            |
| POST   | /api/users/login   | Login and get token | ❌            |
| POST   | /api/users/logout  | Logout              | ❌            |
| GET    | /api/users/        | Get all users       | ✅            |
| PUT    | /api/users/:id     | Update a user       | ✅            |
| DELETE | /api/users/:id     | Delete a user       | ✅            |

## Notes

- Use Postman to test the APIs.
- For protected routes, add this header:  
  `Authorization: Bearer <your_token_here>`

## License

MIT License
