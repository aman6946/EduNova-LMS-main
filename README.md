# AI-Powered Learning Management System

A full-stack Learning Management System where students can explore and purchase courses, while instructors can create and manage their own courses and content.

The project also includes an AI-powered course search feature using Google's Gemini API. If a user searches for something using natural language, the system tries to understand what they want to learn and finds relevant courses.

## Features

### For Students

* Create an account and log in securely
* Sign in using Google OAuth
* Browse all available courses
* Search courses normally or using AI-powered search
* Purchase courses using Razorpay
* Access enrolled courses
* Watch course lectures
* Rate and review courses
* Manage and update profile information
* Forgot password and OTP-based password recovery

### For Instructors

* Separate dashboard for course creators
* Create and manage courses
* Add course thumbnails and content
* Create and manage lectures
* Publish courses
* Track and manage created courses

### AI-Powered Course Search

The project uses the Google Gemini API to make course searching more flexible.

For example, instead of searching for an exact course category, a user can search for something like:

> "I want to learn how to build websites"

The AI understands the user's intent and maps it to a relevant category such as **Web Development**, then the application searches for matching courses.

The application first tries to find courses using the user's original query. If no relevant courses are found, Gemini helps identify the most suitable category or level and performs another search.

## Authentication

The application supports multiple authentication features:

* JWT-based authentication
* Secure password hashing using bcrypt
* Google OAuth login using Firebase
* Cookie-based authentication
* Forgot password functionality with OTP verification

## Payment Integration

Razorpay is integrated to handle paid course enrollment.

The payment flow includes:

1. User selects a course
2. Payment order is created
3. User completes the payment
4. Payment is verified
5. User is enrolled in the course

## Tech Stack

### Frontend

* React.js
* Redux Toolkit
* React Router
* Tailwind CSS
* Axios
* Firebase
* Recharts

### Backend

* Node.js
* Express.js
* MongoDB
* Mongoose
* JWT
* bcryptjs

### Other Services

* Google Gemini API for AI-powered course search
* Firebase for Google Authentication
* Razorpay for payments
* Cloudinary for media storage
* Multer for file uploads
* Nodemailer for email and OTP functionality

## Project Structure

```text
LMS/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── redux/
│   │   ├── customHooks/
│   │   └── assets/
│   │
│   └── package.json
│
└── backend/
    ├── configs/
    ├── controllers/
    ├── middlewares/
    ├── models/
    ├── routes/
    ├── index.js
    └── package.json
```

## API Modules

The backend is divided into different modules:

* `/api/auth` - Authentication and user login
* `/api/user` - User profile and user-related operations
* `/api/course` - Course and lecture management
* `/api/payment` - Razorpay payment and enrollment
* `/api/ai` - AI-powered course search
* `/api/review` - Course ratings and reviews

## Getting Started

### Clone the repository

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

### Install Backend Dependencies

```bash
cd backend
npm install
```

### Install Frontend Dependencies

```bash
cd frontend
npm install
```

## Environment Variables

Create a `.env` file inside the backend directory and add the required environment variables.

Example:

```env
PORT=5000

MONGO_URI=your_mongodb_connection_string

JWT_SECRET=your_jwt_secret

CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret

GEMINI_API_KEY=your_gemini_api_key

EMAIL=your_email
EMAIL_PASSWORD=your_email_password
```

For the frontend, add the required Firebase configuration variables.

```env
VITE_API_URL=your_backend_url
VITE_FIREBASE_API_KEY=your_firebase_api_key
```

## Run the Project

### Start the Backend

```bash
cd backend
npm run dev
```

### Start the Frontend

```bash
cd frontend
npm run dev
```

The frontend will run on the Vite development server, usually at:

```text
http://localhost:5173
```

## What I Learned From This Project

While building this project, I worked with different parts of full-stack development including authentication, API design, database relationships, payment integration, cloud storage, and state management.

I also experimented with integrating Generative AI into a real application instead of using it as a standalone chatbot. The AI search feature was built to understand what a user wants to learn and connect that intent with the courses available on the platform.

## Future Improvements

Some features I would like to improve in the future:

* Better instructor analytics dashboard
* Course progress tracking
* Certificates after course completion
* Improved AI recommendations
* Course wishlist
* Better search and filtering
* Email notifications
* Deployment with a production-ready architecture

## Author

**Aman Singh**

If you found this project interesting, feel free to explore the code and share your feedback.
