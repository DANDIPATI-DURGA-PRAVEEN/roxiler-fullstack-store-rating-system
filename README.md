# Roxiler FullStack Store Rating System

A complete full-stack web application for store rating management with role-based access control.

## 🚀 Tech Stack

- **Backend**: Express.js with Node.js
- **Database**: PostgreSQL
- **Frontend**: React.js with Tailwind CSS
- **Authentication**: JWT (JSON Web Tokens)
- **Validation**: Express-validator & React Hook Form

## 📋 Features

### System Administrator
- ✅ Dashboard with system statistics
- ✅ Add/Edit/Delete users and stores
- ✅ Role management (System Admin, Normal User, Store Owner)
- ✅ Advanced filtering and sorting
- ✅ Multi-word search functionality

### Normal User
- ✅ User registration and login
- ✅ View all stores with ratings
- ✅ Submit and modify ratings (1-5 stars)
- ✅ Search stores by name and address
- ✅ Password update functionality

### Store Owner
- ✅ Dashboard with store statistics
- ✅ View users who rated their store
- ✅ See average store rating
- ✅ Password update functionality

## 🏗️ Project Structure

```
Roxiler_FullStack/
├── backend/                 # Express.js Backend
│   ├── config/
│   │   └── database.js      # PostgreSQL connection
│   ├── database/
│   │   └── schema.sql       # Database schema
│   ├── middleware/
│   │   ├── auth.js          # JWT authentication
│   │   └── validation.js    # Input validation
│   ├── routes/
│   │   ├── admin.js         # Admin routes
│   │   ├── auth.js          # Authentication routes
│   │   ├── ratings.js       # Rating routes
│   │   ├── stores.js        # Store routes
│   │   └── users.js         # User routes
│   ├── .env                 # Environment variables
│   ├── index.js             # Main server file
│   ├── init-db.js           # Database initialization
│   ├── update-admin.js      # Admin password update
│   └── package.json         # Backend dependencies
├── frontend/                # React.js Frontend
│   ├── public/
│   │   └── index.html       # HTML template
│   ├── src/
│   │   ├── components/
│   │   │   ├── Layout.js    # Main layout component
│   │   │   ├── LoadingSpinner.js
│   │   │   └── RatingStars.js
│   │   ├── contexts/
│   │   │   └── AuthContext.js
│   │   ├── pages/
│   │   │   ├── admin/
│   │   │   │   ├── Dashboard.js
│   │   │   │   ├── Stores.js
│   │   │   │   └── Users.js
│   │   │   ├── store-owner/
│   │   │   │   └── Dashboard.js
│   │   │   ├── Login.js
│   │   │   ├── Profile.js
│   │   │   ├── Register.js
│   │   │   ├── StoreDetail.js
│   │   │   └── Stores.js
│   │   ├── services/
│   │   │   └── api.js       # API service
│   │   ├── App.js           # Main app component
│   │   ├── index.js         # React entry point
│   │   └── index.css        # Global styles
│   ├── package.json         # Frontend dependencies
│   ├── tailwind.config.js   # Tailwind configuration
│   └── postcss.config.js    # PostCSS configuration
├── package.json             # Root package.json
└── README.md               # This file
```

## 🛠️ Setup Instructions

### Prerequisites
- Node.js (v14 or higher)
- PostgreSQL (v12 or higher)
- npm or yarn

### 1. Clone the Repository
```bash
git clone <your-repo-url>
cd Roxiler_FullStack
```

### 2. Install Dependencies
```bash
# Install root dependencies
npm install

# Install backend dependencies
cd backend
npm install

# Install frontend dependencies
cd ../frontend
npm install
```

### 3. Database Setup
1. **Create PostgreSQL Database**
   ```sql
   CREATE DATABASE roxiler_ratings;
   ```

2. **Configure Environment Variables**
   ```bash
   cd backend
   cp env.example .env
   ```
   
   Edit `.env` file:
   ```env
   DB_HOST=localhost
   DB_PORT=5432
   DB_NAME=roxiler_ratings
   DB_USER=postgres
   DB_PASSWORD=your_password
   JWT_SECRET=your_jwt_secret_key_here
   JWT_EXPIRES_IN=24h
   PORT=5000
   NODE_ENV=development
   CORS_ORIGIN=http://localhost:3000
   ```

3. **Initialize Database**
   ```bash
   cd backend
   npm run init-db
   ```

### 4. Start the Application
```bash
# From root directory
npm run dev
```

This will start:
- Backend server on http://localhost:5000
- Frontend React app on http://localhost:3000

## 🔑 Default Admin Account

- **Email**: `admin@roxiler.com`
- **Password**: `admin123`

## 📝 Form Validations

- **Name**: 20-60 characters
- **Address**: Maximum 400 characters
- **Password**: 8-16 characters, must include uppercase letter and special character
- **Email**: Standard email validation

## 🔧 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `PUT /api/auth/password` - Update password
- `GET /api/auth/profile` - Get user profile

### Stores
- `GET /api/stores` - Get all stores
- `GET /api/stores/:id` - Get store by ID
- `POST /api/stores` - Create store (Admin only)
- `PUT /api/stores/:id` - Update store (Admin only)
- `DELETE /api/stores/:id` - Delete store (Admin only)

### Ratings
- `POST /api/ratings/:storeId` - Submit rating
- `PUT /api/ratings/:storeId` - Update rating

### Admin
- `GET /api/admin/dashboard` - Admin dashboard stats
- `GET /api/admin/users` - Get all users
- `POST /api/admin/users` - Create user
- `PUT /api/admin/users/:id` - Update user
- `DELETE /api/admin/users/:id` - Delete user
- `PATCH /api/admin/users/:id/role` - Update user role
- `GET /api/admin/stores` - Get all stores (admin view)

## 🎯 Key Features Implemented

### ✅ All Requirements Satisfied
- [x] Three user roles (System Admin, Normal User, Store Owner)
- [x] Complete CRUD operations for users and stores
- [x] Rating system (1-5 stars)
- [x] Advanced search with multi-word support
- [x] Sorting and filtering
- [x] Form validations as per requirements
- [x] Role-based access control
- [x] JWT authentication
- [x] Responsive design with Tailwind CSS

### ✅ Additional Features
- [x] Debounced search functionality
- [x] Real-time form validation
- [x] Toast notifications
- [x] Loading states
- [x] Error handling
- [x] Database indexes for performance
- [x] Rate limiting
- [x] Security headers

## 🚀 Deployment

### Backend Deployment
1. Set up PostgreSQL database
2. Configure environment variables
3. Run `npm install` and `npm start`

### Frontend Deployment
1. Run `npm run build`
2. Deploy the `build` folder to your hosting service

## 📄 License

This project is created for the Roxiler FullStack Intern Coding Challenge.

## 💻 Author

Created by Dandipati Durga Praveen for the Roxiler FullStack Intern Coding Challenge 
