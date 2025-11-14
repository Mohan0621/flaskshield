FlaskShield 🔐 — A Modular Flask + MongoDB Backend Starter
<p align="center"> <img src="https://img.shields.io/badge/Framework-Flask-blue?logo=flask"> <img src="https://img.shields.io/badge/Database-MongoDB-green?logo=mongodb"> <img src="https://img.shields.io/badge/Auth-JWT-yellow?logo=jsonwebtokens"> <img src="https://img.shields.io/badge/Python-3.10+-blue?logo=python"> <img src="https://img.shields.io/badge/License-MIT-purple"> </p>

FlaskShield is a production-oriented modular backend template built using Flask, Blueprints, MongoDB, a layered services architecture, and JWT authentication.
It gives you a clean and scalable structure for building real-world apps without rewriting boilerplate every time.

🔥 Key Features
🧩 Modular Architecture

Clean folder structure

Blueprint-based routing

Services & models separation

Easy to scale

🔐 JWT Authentication

Login, Register

Protected routes using decorators

Password hashing (Werkzeug)

🗄 MongoDB Integration

Global client setup

Dedicated model layer

Users collection with indexes

⚙️ Developer Friendly

Auto-formatted JSON responses

Error handling

Logging layer

Environment-based config

📁 Project Structure
FlaskShield/
│
├── app/
│   ├── __init__.py            # App factory
│   ├── config.py              # Dev/Prod config
│   ├── extensions.py          # Mongo + JWT registrations
│   ├── routes/
│   │   ├── auth_routes.py
│   │   ├── user_routes.py
│   │   ├── __init__.py
│   ├── services/
│   │   ├── auth_service.py
│   │   ├── user_service.py
│   ├── models/
│   │   ├── user_model.py
│   ├── utils/
│       ├── decorators.py
│       ├── hashing.py
│       ├── responses.py
│
├── run.py
├── requirements.txt
└── README.md

🚀 Getting Started
1. Clone the Repository
git clone https://github.com/<your-username>/FlaskShield.git
cd FlaskShield

2. Create Virtual Environment
python -m venv venv
venv\Scripts\activate       # Windows
source venv/bin/activate    # macOS/Linux

3. Install Dependencies
pip install -r requirements.txt

4. Create .env file
SECRET_KEY=your_secret_key
JWT_SECRET_KEY=your_jwt_key
MONGO_URI=mongodb://localhost:27017
DATABASE_NAME=flaskshield

▶️ Run the Application
python run.py


App runs at:
👉 http://127.0.0.1:5000

🧪 API Endpoints
Auth Routes
Register
POST /auth/register


Body:

{
  "name": "Mohan",
  "email": "mohan@example.com",
  "password": "mypassword"
}

Login
POST /auth/login


Body:

{
  "email": "mohan@example.com",
  "password": "mypassword"
}

Response
{
  "token": "your_jwt_token"
}

User Routes
Get Profile (Protected)
GET /user/profile
Authorization: Bearer <token>

Response:
{
  "name": "Mohan",
  "email": "mohan@example.com"
}

🧠 Tech Stack
Category	Tools
Backend Framework	Flask
Database	MongoDB
Authentication	JWT
Language	Python 3.10+
Environment	python-dotenv
Password Security	werkzeug.security
🏗️ Why This Architecture?

✔ Prevents spaghetti code
✔ Encourages scalable development
✔ Services/Models separation = easier unit testing
✔ Blueprints help maintain modularity
✔ Cleaner logic and better readability

📝 Future Enhancements

Refresh + Access token cycle

Role-based authorization

Swagger/OpenAPI documentation

Rate limiting

Uploads support (images, files)

Admin dashboard

📜 License

This project is licensed under the MIT License.

⭐ Support

If you like this project, consider giving it a star ⭐ on GitHub!
