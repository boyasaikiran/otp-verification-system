🔐 OTP-Based Authentication System

This project is a secure and user-friendly OTP (One-Time Password) authentication system built using React.js for the frontend and Node.js (Express) for the backend. OTPs are delivered via email using Nodemailer with support for Gmail App Passwords.
🚀 Features

    📧 Email-based OTP registration and verification

    🔒 Password-protected registration and login

    🔁 OTP auto-expiry with resend functionality

    ⚙️ Configurable OTP length (4, 6, or 8 digits)

    🔐 Secure backend using Express.js and JWT

    🌐 Frontend built with React + React Router

🛠️ Tech Stack
Frontend

    React.js (with Vite)

    React Router DOM

    Axios for HTTP requests

Backend

    Node.js

    Express.js

    Nodemailer for sending OTPs

    JWT for authentication

    SQLite or MongoDB (depending on use case)


📦 How to Run
Backend (Node.js)

    Install dependencies:

npm install

Create a .env file:

EMAIL=your_email@gmail.com
EMAIL_PASS=your_app_password
JWT_SECRET=your_jwt_secret

Start the server:

    node server.js

Frontend (React)

    Navigate to frontend directory:

cd client

Install dependencies:

npm install

Start React app:

    npm run dev

✉️ Email Delivery Notes

    Uses Gmail App Passwords for secure email delivery.

    If some emails aren’t receiving OTPs:

        Check spam folders

        Avoid corporate/firewalled domains

        Consider using email providers like SendGrid for better deliverability

✅ To-Do / Future Enhancements

    SMS-based OTP (via Fast2SMS or Twilio)

    Rate-limiting & cooldown for OTP resend

    OTP expiration timers on frontend

    Email templates and branding

    Database integration for persistent user data
