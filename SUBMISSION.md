# Roxiler FullStack Intern Coding Challenge - Submission

## 🎯 Project Overview

This is a complete full-stack web application for store rating management that satisfies all the requirements specified in the Roxiler FullStack Intern Coding Challenge.

## ✅ Requirements Fulfillment

### Tech Stack Requirements
- ✅ **Backend**: Express.js (from the allowed options: ExpressJs/Loopback/NestJs)
- ✅ **Database**: PostgreSQL (from the allowed options: PostgreSQL/MySQL)
- ✅ **Frontend**: React.js

### Core Functionality
- ✅ **Store Rating System**: Users can submit ratings (1-5) for stores
- ✅ **Single Login System**: Unified authentication for all user roles
- ✅ **User Registration**: Normal users can sign up through registration page

### User Roles Implementation
1. ✅ **System Administrator**
   - Add new stores, normal users, and admin users
   - Dashboard with total users, stores, and ratings
   - View lists with Name, Email, Address, Rating/Role
   - Apply filters on all listings
   - View detailed user information including store ratings for store owners
   - Logout functionality

2. ✅ **Normal User**
   - Sign up and login functionality
   - Update password after login
   - View all registered stores
   - Search stores by Name and Address
   - Store listings with all required information
   - Submit and modify ratings (1-5)
   - Logout functionality

3. ✅ **Store Owner**
   - Login functionality
   - Update password after login
   - Dashboard showing users who rated their store
   - View average store rating
   - Logout functionality

### Form Validations
- ✅ **Name**: 20-60 characters (implemented in database schema and frontend)
- ✅ **Address**: Max 400 characters (implemented in database schema and frontend)
- ✅ **Password**: 8-16 characters, uppercase + special character (implemented in frontend validation)
- ✅ **Email**: Standard email validation (implemented in frontend and backend)

### Additional Requirements
- ✅ **Sorting**: All tables support ascending/descending sorting
- ✅ **Best Practices**: Followed for both frontend and backend
- ✅ **Database Schema**: Adheres to best practices with proper relationships and constraints

## 🚀 Key Features Implemented

### Advanced Functionality
- **Multi-word Search**: Search functionality supports multiple words and phrases
- **Debounced Search**: Prevents excessive API calls during typing
- **Role Management**: Admin can change user roles via dropdown interface
- **CRUD Operations**: Complete Create, Read, Update, Delete for users and stores
- **Real-time Validation**: Form validation with immediate feedback
- **Responsive Design**: Works on all device sizes
- **Security**: JWT authentication, password hashing, rate limiting

### User Experience
- **Toast Notifications**: Success and error feedback
- **Loading States**: Visual feedback during operations
- **Modal Forms**: Clean interface for adding/editing
- **Filtering Options**: Multiple filter criteria
- **Sorting Options**: Sort by various fields

## 🏗️ Project Structure

```
Roxiler_FullStack/
├── backend/                 # Express.js Backend
│   ├── config/database.js   # PostgreSQL connection
│   ├── database/schema.sql  # Database schema with constraints
│   ├── middleware/          # Auth & validation middleware
│   ├── routes/              # All API endpoints
│   └── package.json         # Backend dependencies
├── frontend/                # React.js Frontend
│   ├── src/
│   │   ├── components/      # Reusable components
│   │   ├── contexts/        # React contexts
│   │   ├── pages/           # All page components
│   │   └── services/        # API service layer
│   └── package.json         # Frontend dependencies
└── README.md               # Complete setup instructions
```

## 🔧 Technical Implementation

### Backend (Express.js)
- **Authentication**: JWT-based with role-based access control
- **Validation**: Express-validator for input validation
- **Database**: PostgreSQL with proper relationships and constraints
- **Security**: bcrypt for password hashing, helmet for security headers
- **Performance**: Database indexes, rate limiting

### Frontend (React.js)
- **State Management**: React hooks and context API
- **Form Handling**: React Hook Form with validation
- **Styling**: Tailwind CSS for responsive design
- **Icons**: Lucide React for consistent iconography
- **API Integration**: Axios for HTTP requests

### Database (PostgreSQL)
- **Schema**: Three main tables (users, stores, ratings)
- **Constraints**: Proper foreign keys, check constraints
- **Indexes**: Performance optimization for queries
- **Triggers**: Automatic timestamp updates

## 🎯 Demo Credentials

- **Admin Account**: `admin@roxiler.com` / `admin123`
- **Frontend URL**: http://localhost:3000
- **Backend API**: http://localhost:5000

## 📋 Setup Instructions

1. **Clone Repository**
2. **Install Dependencies**: `npm run install-all`
3. **Database Setup**: Create PostgreSQL database `roxiler_ratings`
4. **Environment**: Copy `backend/env.example` to `backend/.env` and configure
5. **Initialize**: `npm run db:init`
6. **Start**: `npm run dev`

## 🏆 Conclusion

This project successfully implements all requirements specified in the Roxiler FullStack Intern Coding Challenge. The application is production-ready with proper error handling, security measures, and user experience considerations.

**All requirements have been satisfied and the application is ready for submission!** 🎉

---

*Created with ❤️ for the Roxiler FullStack Intern Coding Challenge* 