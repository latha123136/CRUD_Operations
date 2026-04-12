# User Management CRUD Application

A full-stack web application for managing users with Create, Read, Update, and Delete (CRUD) operations. Built with Node.js, Express, MongoDB, and vanilla JavaScript.

## 🚀 Features

- **User Registration** - Create new user accounts with name, email, password, and role
- **User Authentication** - Secure login system with JWT tokens
- **User Management** - View all users in a responsive table
- **Edit Users** - Update user information (name, email, role) with modal interface
- **Delete Users** - Remove users with confirmation dialog
- **Role-based System** - Support for Student, Trainer, and Admin roles
- **Responsive Design** - Modern UI with orange and white color scheme
- **Real-time Updates** - Instant UI updates after CRUD operations

## 🛠️ Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **bcryptjs** - Password hashing
- **jsonwebtoken** - JWT authentication
- **cors** - Cross-origin resource sharing
- **dotenv** - Environment variables

### Frontend
- **HTML5** - Markup structure
- **CSS3** - Styling and responsive design
- **Vanilla JavaScript** - Client-side functionality
- **Fetch API** - HTTP requests to backend

## 📁 Project Structure


Copy

Insert at cursor
CRUD operations/
├── crudOperations/
│ ├── backend/
│ │ ├── config/
│ │ │ └── db.js # Database connection
│ │ ├── controllers/
│ │ │ └── authController.js # CRUD operations logic
│ │ ├── models/
│ │ │ └── User.js # User schema
│ │ ├── routes/
│ │ │ └── authRoutes.js # API routes
│ │ ├── .env # Environment variables
│ │ ├── package.json # Dependencies
│ │ └── server.js # Main server file
│ └── frontend/
│ └── index.html # Complete frontend application


## ⚙️ Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local installation or MongoDB Atlas)
- Git

### 1. Clone Repository
```bash
git clone <your-repo-url>
cd "CRUD operations/crudOperations"

Copy

Insert at cursor
2. Backend Setup
cd backend
npm install

Copy

Insert at cursor
bash
3. Environment Configuration
Create .env file in the backend directory:

PORT=5000
MONGO_URI=mongodb://localhost:27017/crud_db
JWT_SECRET=your-secret-key-here

Copy

Insert at cursor
env
For MongoDB Atlas (Cloud):

MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/crud_db?retryWrites=true&w=majority

Copy

Insert at cursor
env
4. Start Backend Server
npm run dev

Copy

Insert at cursor
bash
You should see:

Server running on port 5000
MongoDB connected successfully!

Copy

Insert at cursor
5. Start Frontend
Open frontend/index.html with Live Server extension in VS Code

Or serve it using any local server (not by double-clicking the file)

🔧 API Endpoints
Method	Endpoint	Description	Request Body
POST	/api/auth/register	Create new user	{name, email, password, role}
POST	/api/auth/login	Authenticate user	{email, password}
GET	/api/auth/users	Get all users	None
PUT	/api/auth/users/:id	Update user	{name, email, role}
DELETE	/api/auth/users/:id	Delete user	None
Example API Usage
Register User:

POST http://localhost:5000/api/auth/register
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "password123",
  "role": "student"
}

Copy

Insert at cursor
javascript
Login:

POST http://localhost:5000/api/auth/login
Content-Type: application/json

{
  "email": "john@example.com",
  "password": "password123"
}

Copy

Insert at cursor
javascript
🎯 Usage Guide
1. Registration
Click "Register" tab

Fill in name, email, password

Select role (Student/Trainer/Admin)

Click "Register" button

2. Login
Click "Login" tab

Enter registered email and password

Click "Login" button

Upon success, user table will appear

3. View Users
After login, all users are displayed in a table

Shows name, email, role, and action buttons

4. Edit User
Click "Edit" button next to any user

Modal opens with current user data

Modify fields and click "Save"

5. Delete User
Click "Delete" button next to any user

Confirm deletion in the dialog

User is removed from database and table

6. Logout
Click "Logout" button in header

Returns to login/register screen

Clears authentication token

🔒 Security Features
Password Hashing - bcrypt with salt rounds

JWT Authentication - Secure token-based auth

Input Validation - Required fields and email format

CORS Protection - Controlled cross-origin access

Error Handling - Proper HTTP status codes

🎨 UI Features
Modern Design - Clean orange and white theme

Responsive Layout - Works on desktop and mobile

Interactive Elements - Hover effects and smooth transitions

Modal Interface - User-friendly edit dialogs

Real-time Feedback - Success/error messages

Tab Navigation - Easy switching between login/register

🚨 Troubleshooting
Backend Issues
MongoDB Connection Failed:

# Check if MongoDB service is running
sc query MongoDB

# Start MongoDB service (Windows)
net start MongoDB

Copy

Insert at cursor
bash
Port Already in Use:

# Kill process on port 5000
npx kill-port 5000

Copy

Insert at cursor
bash
Frontend Issues
CORS Errors:

Ensure cors() middleware is enabled in server.js

Use Live Server, don't open HTML file directly

API Connection Refused:

Verify backend is running on port 5000

Check console for error messages

📦 Dependencies
Backend Dependencies
{
  "express": "^4.18.2",
  "mongoose": "^7.5.0",
  "bcryptjs": "^2.4.3",
  "jsonwebtoken": "^9.0.2",
  "cors": "^2.8.5",
  "dotenv": "^16.3.1"
}

Copy

Insert at cursor
json
Development Dependencies
{
  "nodemon": "^3.0.1"
}

Copy

Insert at cursor
json
🤝 Contributing
Fork the repository

Create feature branch (git checkout -b feature/AmazingFeature)

Commit changes (git commit -m 'Add AmazingFeature')

Push to branch (git push origin feature/AmazingFeature)

Open Pull Request

📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

👨💻 Author
Your Name

GitHub: @yourusername

Email:

🙏 Acknowledgments
Express.js team for the excellent web framework

MongoDB team for the robust database solution

bcrypt.js for secure password hashing

JWT for authentication standards

⭐ If you found this project helpful, please give it a star!


