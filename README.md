# 🔐 Secure Web Application (Flask + JWT)

> **Demonstrating secure authentication and authorization aligned with OWASP Top 10 security principles.**

This project is a secure RESTful web application built using **Flask** that implements industry-standard authentication and authorization mechanisms. It demonstrates secure coding practices including password hashing, token-based authentication, protected API routes, and mitigation of common web vulnerabilities.

---

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Built with Python](https://img.shields.io/badge/Built%20with-Python-blue?logo=python&logoColor=white)
![Framework: Flask](https://img.shields.io/badge/Framework-Flask-black?logo=flask&logoColor=white)
![Database: SQLite](https://img.shields.io/badge/Database-SQLite-lightblue?logo=sqlite&logoColor=white)
![Auth: JWT](https://img.shields.io/badge/Auth-JWT-orange?logo=jsonwebtokens&logoColor=white)

---

## 📑 Table of Contents

- [Project Overview](#-project-overview)
- [Features Implemented](#-features-implemented)
- [Security Measures](#%EF%B8%8F-security-measures)
- [OWASP Top 10 Mapping](#-owasp-top-10-mapping)
- [Tech Stack](#%EF%B8%8F-tech-stack)
- [API Endpoints](#-api-endpoints)
- [Setup & Installation](#%EF%B8%8F-setup--installation)
- [Learning Outcome](#-learning-outcome)
- [Creators](#%E2%80%8D-creators)
- [License](#-license)
- [Contributing](#-contributing)
- [Contact](#-contact)

---

## 📌 Project Overview

This project is a secure web application built using Flask that demonstrates secure authentication and authorization mechanisms aligned with the **OWASP Top 10** security framework.

It includes:

- User registration with secure credential storage
- JWT-based authentication
- Token-protected routes
- SQL injection prevention
- Secure environment configuration

The project follows a **security-first development approach**, making it suitable for cybersecurity-focused internships and academic submissions.

---

## 🚀 Features Implemented

| Feature | Description |
|---|---|
| 👤 **User Registration** | Create new user accounts with validated credentials |
| 🔒 **Secure Password Hashing** | Passwords hashed using Bcrypt before storage |
| 🪙 **JWT-based Authentication** | Token-based login system for stateless authentication |
| 🛡️ **Protected Routes** | Endpoints accessible only with a valid JWT token |
| 💉 **SQL Injection Prevention** | Parameterized queries used throughout |
| ⏱️ **Token Expiration** | Tokens automatically expire after 1 hour |
| 🌱 **Environment Variable Security** | Secret keys stored securely using `.env` |

---

## 🛡️ Security Measures

- Passwords hashed using Bcrypt before storing in the database
- SQL Injection prevented using parameterized queries
- JWT tokens required to access protected endpoints
- Token expiration set to 1 hour
- Secret keys managed via environment variables
- Stateless authentication to reduce session hijacking risks

---

## 🧠 OWASP Top 10 Mapping

This project aligns with the **OWASP Top 10 (2021)** security risks:

| OWASP Risk | Implementation in This Project |
|---|---|
| **A01 – Broken Access Control** | Protected routes require valid JWT tokens |
| **A02 – Cryptographic Failures** | Passwords securely hashed using Bcrypt |
| **A03 – Injection** | Parameterized queries prevent SQL Injection |
| **A05 – Security Misconfiguration** | Secret keys stored in environment variables |
| **A07 – Identification & Authentication Failures** | Secure login system with token expiration |

> This mapping demonstrates **practical implementation** of secure development principles rather than just theoretical understanding.

---

## 🛠️ Tech Stack

| **Layer** | **Technology** | **Purpose** |
|---|---|---|
| **Language** | Python | Core application logic |
| **Framework** | Flask | Web server and routing |
| **Password Security** | Flask-Bcrypt | Secure password hashing |
| **Authentication** | Flask-JWT-Extended | JWT token generation and validation |
| **Database** | SQLite | Lightweight local data storage |

<p align="center">
  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white" alt="Python" /></a>
  <a href="https://flask.palletsprojects.com/"><img src="https://img.shields.io/badge/Flask-Latest-000000?logo=flask&logoColor=white" alt="Flask" /></a>
  <a href="https://flask-bcrypt.readthedocs.io/"><img src="https://img.shields.io/badge/Flask--Bcrypt-Security-blue" alt="Flask-Bcrypt" /></a>
  <a href="https://flask-jwt-extended.readthedocs.io/"><img src="https://img.shields.io/badge/Flask--JWT--Extended-Auth-orange" alt="Flask-JWT-Extended" /></a>
  <a href="https://www.sqlite.org/"><img src="https://img.shields.io/badge/SQLite-Database-lightblue?logo=sqlite&logoColor=white" alt="SQLite" /></a>
</p>

---

## 🔄 API Endpoints

### 1️⃣ Register

**POST** `/register`

**Request Body:**
```json
{
  "username": "your_username",
  "password": "your_password"
}
```

**Response:**
```json
{
  "message": "User registered successfully"
}
```

---

### 2️⃣ Login

**POST** `/login`

**Request Body:**
```json
{
  "username": "your_username",
  "password": "your_password"
}
```

**Response:**
```json
{
  "message": "Login successful",
  "access_token": "<your_jwt_token>"
}
```

---

### 3️⃣ Protected Route

**GET** `/protected`

**Headers:**
```
Authorization: Bearer <your_jwt_token>
```

**Response:**
```json
{
  "message": "Welcome, your_username! This is a protected route."
}
```

---

## ⚙️ Setup & Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2️⃣ Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Create a `.env` File

```env
SECRET_KEY=your_secret_key
JWT_SECRET_KEY=your_jwt_secret_key
```

### 5️⃣ Run the Application

```bash
python app.py
```

By default, Flask runs on: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## 🎯 Learning Outcome

This project demonstrates:

- Secure credential storage with bcrypt hashing
- Token-based stateless authentication using JWT
- Secure REST API development
- Practical mitigation of OWASP Top 10 vulnerabilities
- Backend security implementation using Flask

It reflects applied cybersecurity knowledge suitable for internships and academic evaluation.

---

## 👩‍💻 Creators

**Diksha Manwani** — [manwanidiksh@gmail.com](mailto:manwanidiksh@gmail.com)

---

## 🧾 License

This project is licensed under the **MIT License** — feel free to use, modify, and share with attribution.
See the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributing

Contributions, issues, and feature requests are **welcome!**

If you'd like to improve security features or add enhancements, feel free to fork the repository and submit a pull request.

---

## 📬 Contact

For support, questions, or collaboration, reach out via email: **[manwanidiksh@gmail.com](mailto:manwanidiksh@gmail.com)**

---

<p align="center">⭐ If you found this project helpful, consider starring it on GitHub!</p>
