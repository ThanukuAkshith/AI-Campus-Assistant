text
# AI Campus Assistant Chatbot

An intelligent AI-powered campus assistant built with FastAPI that helps students explore, search, and enroll in AI/ML-related courses through natural language conversations. The chatbot uses simple intent detection logic to understand user queries and respond accordingly.

## 🚀 Features

- 💬 **AI Chatbot** – Responds to user queries like greetings, course listings, and enrollments.
- 🎓 **Course Management** – View, search, and filter available AI/ML courses.
- 🧾 **Student Enrollment** – Enroll students into specific courses directly via chat.
- 🕓 **Session Handling** – Manages user sessions for personalized chat history.
- 💡 **Intent Detection** – Detects intents like greeting, search, enroll, and exit.
- 🗂 **Database Integration** – Stores courses, chat messages, sessions, and enrollments using SQLAlchemy ORM.

## 🏗️ Tech Stack

| Component          | Technology          |
|--------------------|---------------------|
| Backend Framework  | FastAPI             |
| Database           | SQLite              |
| ORM                | SQLAlchemy          |
| Data Models        | Pydantic            |
| Language           | Python              |
| API Format         | REST API (JSON)     |

## 📁 Project Structure

AI-Campus-Assistant-Chatbot/
│
├── main.py # Main FastAPI application with all routes & chatbot logic
├── models.py # Database models (Courses, Sessions, Enrollments, Messages)
├── schemas.py # Pydantic schemas for data validation
├── database.py # SQLite database configuration and session management
├── requirements.txt # Required Python dependencies
└── README.md # Project documentation

text

## ⚙️ Installation & Setup

cd AI-Campus-Assistant-Chatbot

Create a virtual environment
python -m venv venv

Activate virtual environment
source venv/bin/activate # For Mac/Linux
venv\Scripts\activate # For Windows

Install dependencies
pip install fastapi uvicorn sqlalchemy pydantic

Run the application
uvicorn main:app --reload

text

## 🔗 Access API

- Open your browser at 👉 [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
- Interactive API docs at 👉 [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

## 💬 API Endpoints

| Method | Endpoint                   | Description                   |
|--------|----------------------------|-------------------------------|
| GET    | /                          | Welcome message               |
| POST   | /session                   | Create a new chat session     |
| GET    | /courses                   | Get all available courses     |
| GET    | /courses/search?keyword=ml | Search for specific courses   |
| POST   | /chat                      | Send a message to chatbot     |
| POST   | /enroll                    | Enroll a student in a course  |
| GET    | /chat-history?email=example@gmail.com | View previous chat history |

## 🧩 Example Chat

User: "Hi"
Bot: "Hello! I can help you explore AI/ML courses."

User: "List all courses"
Bot: "Available courses: Python for AI, ML Fundamentals, Deep Learning, NLP Basics."

User: "Enroll in ML201"
Bot: "To enroll, please provide your course code and details."

text

## 📚 Available Courses

{"code": "ML201", "name": "ML Fundamentals", "category": "Machine Learning",
"instructor": "Prof. Arjun Nair", "keywords": "machine learning,ml,supervised"},

{"code": "DL301", "name": "Deep Learning", "category": "Deep Learning",
"instructor": "Dr. Kavita Reddy", "keywords": "deep learning,neural networks,tensorflow"},

{"code": "NLP201", "name": "NLP Basics", "category": "NLP",
"instructor": "Dr. Rohan Sharma", "keywords": "nlp,text,language"}
