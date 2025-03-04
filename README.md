# User Authentication System

## 📌 Project Overview

This is a **secure user authentication system** built using **Node.js, Express, and MongoDB**. It provides **user registration, login, password reset, and authentication** using JWT. The system includes proper **input validation, error handling, and security features** such as **rate limiting, CORS, and helmet for protection**.

## 🚀 Features

- ✅ **User Registration** (with email & password validation)
- ✅ **User Login** (JWT-based authentication)
- ✅ **User Profile Retrieval**
- ✅ **Forgot Password & Reset Password** (with email verification)
- ✅ **Middleware Protection** (JWT authentication)
- ✅ **Security Measures** (Helmet, CORS, Rate Limiting, Environment Variables)
- ✅ **Error Handling & Logging**

---

## 🏗️ Tech Stack

- **Backend:** Node.js, Express.js
- **Database:** MongoDB (Mongoose ORM)
- **Authentication:** JWT (JSON Web Tokens)
- **Email Service:** Nodemailer (for password reset emails)
- **Security:** Helmet, CORS, Express-rate-limit

---

## 🔧 Installation & Setup

### **1️⃣ Clone the Repository**

```sh
git clone https://github.com/your-username/auth-system.git
cd auth-system
```

### **2️⃣ Install Dependencies**

```sh
npm install
```

### **3️⃣ Configure Environment Variables**

Create a `.env` file in the project root and add the following:

```env
PORT=5000
NODE_ENV=development
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
JWT_EXPIRE=30d
SMTP_HOST=smtp.mailtrap.io
SMTP_PORT=2525
SMTP_EMAIL=your_email@example.com
SMTP_PASSWORD=your_password
FROM_EMAIL=no-reply@example.com
```

### **4️⃣ Start the Server**

```sh
npm start
```

Server will run on `http://localhost:5000`

---

## 🛠️ API Endpoints

### **1️⃣ User Registration**

- **Endpoint:** `POST /api/auth/register`
- **Body:**
  ```json
  {
    "name": "John Doe",
    "email": "john@example.com",
    "password": "password123"
  }
  ```
- **Response:**
  ```json
  {
    "success": true,
    "token": "your-jwt-token"
  }
  ```

### **2️⃣ User Login**

- **Endpoint:** `POST /api/auth/login`
- **Body:**
  ```json
  {
    "email": "john@example.com",
    "password": "password123"
  }
  ```
- **Response:**
  ```json
  {
    "success": true,
    "token": "your-jwt-token"
  }
  ```

### **3️⃣ Get User Profile**

- **Endpoint:** `GET /api/auth/me`
- **Headers:** `{ Authorization: Bearer your-jwt-token }`
- **Response:**
  ```json
  {
    "success": true,
    "data": {
      "_id": "user-id",
      "name": "John Doe",
      "email": "john@example.com"
    }
  }
  ```

### **4️⃣ Forgot Password**

- **Endpoint:** `POST /api/auth/forgotpassword`
- **Body:**
  ```json
  {
    "email": "john@example.com"
  }
  ```
- **Response:** `{ "success": true, "message": "Email sent" }`

### **5️⃣ Reset Password**

- **Endpoint:** `PUT /api/auth/resetpassword/:resettoken`
- **Body:**
  ```json
  {
    "password": "newpassword123"
  }
  ```
- **Response:** `{ "success": true, "token": "new-jwt-token" }`

---

## 🔒 Security Features

- **✅ JWT Authentication:** Secure login & user sessions
- **✅ Input Validation:** Prevents invalid/malicious data
- **✅ Helmet:** Protects from web vulnerabilities
- **✅ CORS:** Restricts API access to trusted sources
- **✅ Rate Limiting:** Limits requests to prevent brute force attacks

---

## 📌 Future Improvements

- 🔹 Add social login (Google, GitHub, etc.)
- 🔹 Implement two-factor authentication (2FA)
- 🔹 Create an admin dashboard for user management
- 🔹 Store refresh tokens for extended login sessions

---

## 🤝 Contributing

1. Fork the project
2. Create a feature branch (`git checkout -b feature-branch`)
3. Commit changes (`git commit -m 'Added new feature'`)
4. Push to branch (`git push origin feature-branch`)
5. Open a Pull Request 🚀

---

## 📧 Contact

For any queries or suggestions, feel free to reach out!

- Email: [abhi798yadav@gmail.com](mailto\:abhi798yadav@gmail.com)
- **GitHub:** Abhishekyadav7987

**🚀 Happy Coding!** 🎉

