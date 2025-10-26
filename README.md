# 🎬 URShow – Online Movie Ticket Booking Website

URShow is a **Full Stack Movie Ticket Booking Website** built using the **MERN Stack (MongoDB, Express.js, React.js, Node.js)**.  
It allows users to explore movies, choose preferred seats, and book tickets online — all with smooth authentication, email notifications, and admin management tools.

---

## 🚀 Features

### 👥 User Features
- **Signup & Login** using multiple options — Email, Social accounts, and Phone number (powered by Clerk)
- **Multi-session login** – easily switch between multiple accounts without signing out
- **Browse Movies** with details such as title, description, cast, and showtimes
- **Seat Selection** – pick your preferred seats before booking
- **Online Payment Integration**
- **Email Notifications**:
  - Booking confirmation email
  - Reminder email a few hours before the show
  - Notification when a new movie is added

### 🧑‍💼 Admin Features
- **Add new movies**
- **Manage existing movies**
- **View and manage all bookings**

---

## ⚙️ Tech Stack

| Layer | Technology |
|-------|-------------|
| **Frontend** | React.js, Tailwind CSS |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB |
| **Authentication** | Clerk |
| **Email & Background Jobs** | Inngest |
| **Payment System** | (e.g., Stripe / Razorpay / PayPal – mention whichever you used) |

---

## 🔄 Background Jobs with Inngest

URShow uses **Inngest** to handle asynchronous background tasks such as:
- Sending booking confirmation and reminder emails
- Notifying users when new movies are added
- Managing seat reservation timers:
  - If payment fails, the selected seats remain **reserved for 10 minutes**
  - After 10 minutes, seats are **automatically released** if payment is not completed

---

## 🔐 Authentication with Clerk

URShow integrates **Clerk** for secure and flexible authentication.  
Features include:
- Multi-provider sign-up (Email, Google, Phone, etc.)
- Multi-session handling (switch between profiles easily)
- Seamless authentication across client and server

---

## 🧩 Folder Structure
    URShow/
    │
    ├── client/                         # React frontend (Vite-based)
    │   ├── node_modules/
    │   ├── public/
    │   ├── src/                        # All React components, pages, hooks, etc.
    │   ├── .env                        # Frontend environment variables
    │   ├── eslint.config.js
    │   ├── index.html
    │   ├── package.json
    │   ├── package-lock.json
    │   ├── vercel.json                 # Vercel deployment config for frontend
    │   └── vite.config.js
    │
    ├── server/                         # Express backend
    │   ├── configs/                    # Database and environment configurations
    │   ├── controllers/                # Controller logic for routes
    │   ├── inngest/                    # Inngest background job functions
    │   ├── middleware/                 # Authentication, error handling, etc.
    │   ├── models/                     # Mongoose schemas and models
    │   ├── routes/                     # API endpoints
    │   ├── node_modules/
    │   ├── .env                        # Backend environment variables
    │   ├── package.json
    │   ├── package-lock.json
    │   ├── server.js                   # Entry point for Express server
    │   └── vercel.json                 # Vercel deployment config for backend
    │
    ├── .gitignore                      # Git ignored files (e.g., node_modules, .env)
    └── README.md


