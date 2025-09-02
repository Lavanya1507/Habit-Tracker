# Habit Tracker & Recommender System

A full-stack web application that helps users discover, track, and manage habits using AI-powered recommendations. Built with **FastAPI** (backend) and **Next.js** (frontend).

---

## Features

- **User Authentication:** Signup, login, and logout with secure JWT cookies.
- **Habit Management:** Create, view, and check-in habits. Track streaks and progress.
- **AI Recommendations:** Get personalized habit suggestions using Gemini API.
- **Progress Tracking:** Visualize daily completion and streaks.
- **Admin Panel:** (API only) Manage users.
- **Responsive UI:** Modern, mobile-friendly design with Tailwind CSS.

---

## Project Structure

```
Habit tracker/
├── backend/
│   ├── auth_utils.py
│   ├── database.py
│   ├── main.py
│   ├── requirements.txt
│   ├── schema.py
│   └── routes/
│       ├── __init__.py
│       └── routes.py
├── frontend/
│   ├── package.json
│   ├── jsconfig.json
│   ├── postcss.config.mjs
│   ├── next.config.mjs
│   ├── public/
│   └── src/
│       └── app/
│           ├── components/
│           ├── dashboard/
│           ├── signup/
│           ├── login/
│           ├── recommend/
│           ├── page.js
│           ├── layout.js
│           └── globals.css
└── .gitignore
```

---

## Getting Started

### 1. Backend Setup

**Requirements:** Python 3.10+, MongoDB Atlas (or local MongoDB)

1. Install dependencies:
    ```sh
    cd backend
    pip install -r requirements.txt
    ```
2. Create a `.env` file in `backend/`:
    ```
    SECRET_KEY=your_secret_key
    MONGO_DB=your_mongodb_connection_string
    ```
3. Run the FastAPI server:
    ```sh
    uvicorn main:app --reload
    ```
    The API will be available at `http://localhost:8000`.

### 2. Frontend Setup

**Requirements:** Node.js 18+

1. Install dependencies:
    ```sh
    cd frontend
    npm install
    ```
2. Create a `.env.local` file in `frontend/`:
    ```
    NEXT_PUBLIC_GEMINI_API_KEY=your_gemini_api_key
    ```
3. Start the Next.js dev server:
    ```sh
    npm run dev
    ```
    The app will be available at [http://localhost:3000](http://localhost:3000).

---

## Usage

- **Sign Up / Login:** Access via `/signup` or `/login`.
- **Dashboard:** View and manage habits at `/dashboard`.
- **Recommendations:** Get AI-powered suggestions at `/recommend`.
- **Progress:** Track daily completion and streaks.

---

## API Endpoints

See [backend/routes/routes.py](backend/routes/routes.py) for details.

- `POST /signup` — Register user
- `POST /login` — Login user
- `POST /logout` — Logout user
- `GET /habits` — List user habits
- `POST /habits` — Create habit
- `POST /check-in/{habit_id}` — Mark habit as done
- `GET /progress` — Get daily progress
- `GET /me` — Get current user info

---

## Technologies Used

- **Backend:** FastAPI, MongoDB (Motor), JWT, Passlib, Pydantic
- **Frontend:** Next.js, React, Tailwind CSS, Axios
- **AI:** Gemini API (Google Generative Language)

---

## License

This project is for educational/demo purposes.

---

