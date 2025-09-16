GUVI Internship Project – User Authentication System

This project is a full-stack authentication system built during the GUVI Internship.
It provides user registration, login, and profile management using modern web technologies.

🚀 Features

✅ Signup – Register with name, email, and secure password (validation included).

✅ Login – Authenticate users and generate a session token.

✅ Profile Page – View and update user details (name, email, DOB, phone).

✅ Token-Based Authentication – Secure login using Redis-backed tokens.

✅ MySQL + MongoDB – User details stored in MySQL, with profile synced to MongoDB.

✅ AJAX & jQuery – Frontend communicates with backend without page reloads.

✅ Bootstrap 5 – Clean, responsive UI.

🛠️ Tech Stack

*Frontend: HTML5, CSS3, Bootstrap 5, JavaScript, jQuery
*Backend: PHP 8+
*Databases: MySQL (primary), MongoDB (secondary, for profiles)
*Cache / Session Store: Redis (for tokens)
*Package Manager: Composer (for MongoDB driver & dependencies)

📂 Project Structure
guvi-internship-project/
│
├── html/                # Frontend pages (login, signup, profile)
├── php/                 # Backend PHP code
│   ├── api/             # API endpoints (login.php, register.php, profile.php)
│   ├── db/              # Database connection files
│   ├── repo/            # User repository (MySQL queries)
│   ├── service/         # AuthService (register, login, logout, validateToken)
│   ├── redis/           # Redis client for token storage
│   └── utils/           # Helper functions (token generator)
│
├── sql/                 # SQL scripts for MySQL tables
├── vendor/              # Composer dependencies (auto-generated)
├── composer.json        # Project dependencies
├── composer.lock        # Locked dependency versions
├── .gitignore           # Ignored files (vendor, env, etc.)
└── README.md            # Project documentation

⚙️ Setup Instructions
1. Clone the repo
git clone https://github.com/VardhiDimple/guvi-internship-project.git
cd guvi-internship-project

2. Install dependencies
*composer install

3. Configure .env

*Create a .env file in the project root with your credentials:

DB_HOST=localhost
DB_NAME=guvi_db
DB_USER=root
DB_PASS=yourpassword
DB_CHARSET=utf8mb4

REDIS_HOST=127.0.0.1
REDIS_PORT=6379
REDIS_TTL=3600

4. Setup MySQL

*Run the SQL script from /sql to create the users table.

5. Start Services

*MongoDB server
*Redis server
*Apache/Nginx with PHP

🔐 How Authentication Works

*User logs in → PHP verifies credentials in MySQL.
*If valid → generates a token and stores it in Redis.
*Browser stores token in localStorage.
*Profile/API requests must include token (Authorization: Bearer <token>).
*Token is validated via Redis before granting access.

👨‍💻 Author
Dimple Vardhi
GUVI Internship Project – 2025
