# StudyNotion — EdTech Platform

**StudyNotion** is a full-stack EdTech web application that enables students to discover, purchase, and consume online courses while empowering instructors to create, manage, and monetize educational content.

---

##  Features

###  For Students
* **Course Catalog & Search:** Browse courses by category, ratings, and popularity.
* **Seamless Enrollment & Checkout:** Add courses to a cart and complete purchases securely.
* **Interactive Learning Dashboard:** Watch video lectures, track course progress, and leave course reviews.
* **Profile Management:** Update personal details, profile pictures, and password settings.

###  For Instructors
* **Instructor Dashboard:** View total revenue, enrolled student counts, and course performance analytics.
* **Course Builder:** Create courses with structured sections, subsections, video uploads, and pricing.
* **Content Management:** Edit or delete existing courses and manage published drafts.

###  Security & Authentication
* **JWT & OTP Verification:** Secure user signup and login flows with email-based OTP verification and password reset links.
* **Role-Based Access Control (RBAC):** Dedicated routes and permissions for Students, Instructors, and Admins.

---

##  Tech Stack

* **Frontend:** React.js, Tailwind CSS, Redux Toolkit, React Router
* **Backend:** Node.js, Express.js
* **Database:** MongoDB, Mongoose
* **Media & Storage:** Cloudinary (for course videos and thumbnails)
* **Payments & Email:** Razorpay / Stripe, Nodemailer

---

##  Project Structure

```text
EdtechNiranjan/
├── public/                 # Static assets and index.html
├── server/                 # Backend Node.js & Express API
│   ├── config/             # Database, Cloudinary, and Razorpay configurations
│   ├── controllers/        # Route controllers (Auth, Course, Payment, Profile)
│   ├── middlewares/        # JWT authentication & role verification
│   ├── models/             # Mongoose schemas (User, Course, Section, Rating)
│   ├── routes/             # API endpoints
│   └── utils/              # Helper utilities (mail sender, image uploader)
├── src/                    # Frontend React application
│   ├── components/         # Reusable UI components
│   ├── pages/              # Application views (Home, Dashboard, Catalog, Login)
│   ├── services/           # API integration and Axios instances
│   ├── slices/             # Redux state management slices
│   └── utils/              # Frontend constants and helpers
├── package.json            # Frontend dependencies and scripts
└── tailwind.config.js      # Tailwind CSS configuration
```

---

##  Getting Started

Follow these steps to run the project locally on your machine.

### Prerequisites
* **Node.js** (check `.nvmrc` for the recommended version)
* **MongoDB** (Local instance or MongoDB Atlas URI)
* **Cloudinary** & **Payment Gateway** developer accounts

### 1. Clone the Repository
```bash
git clone https://github.com
cd EdtechNiranjan
```

### 2. Install Dependencies
Install dependencies for both the root frontend and the backend server:
```bash
# Install frontend dependencies
npm install

# Install backend dependencies
cd server
npm install
cd ..
```

### 3. Configure Environment Variables
Create a `.env` file in the root directory and another `.env` file inside the `server/` directory.

**Frontend (`.env` in root):**
```env
REACT_APP_BASE_URL=http://localhost:4000/api/v1
```

**Backend (`server/.env`):**
```env
PORT=4000
MONGODB_URL=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key

# Email Configuration (Nodemailer)
MAIL_HOST=://gmail.com
MAIL_USER=your_email@gmail.com
MAIL_PASS=your_app_password

# Cloudinary Configuration
CLOUD_NAME=your_cloudinary_cloud_name
API_KEY=your_cloudinary_api_key
API_SECRET=your_cloudinary_api_secret
FOLDER_NAME=StudyNotion

# Payment Gateway (e.g., Razorpay)
RAZORPAY_KEY=your_razorpay_key_id
RAZORPAY_SECRET=your_razorpay_secret
```

### 4. Run the Application
You can run the frontend and backend servers concurrently (if configured in root `package.json`) or in two separate terminals:

```bash
# Terminal 1: Start the backend server
cd server
npm run dev

# Terminal 2: Start the React frontend
npm start
```

The frontend will run on `http://localhost:3000` and the backend API on `http://localhost:4000`.

---

##  Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com).

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

##  License

Distributed under the MIT License. See `LICENSE` for more information.

---

##  Author

**Niranjan**
* GitHub: [@Niranjangkv](https://github.com/Niranjangkv)
