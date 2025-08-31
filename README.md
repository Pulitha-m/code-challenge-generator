# Code Challenge Generator Platform

A full-stack web application designed to help developers, educators, and interviewers generate, manage, and store coding challenges and multiple-choice questions (MCQs) efficiently. Built with a modern tech stack for a seamless experience.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=flat&logo=fastapi)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-B73BFE?style=flat&logo=vite&logoColor=FFD62E)
![Clerk](https://img.shields.io/badge/Clerk-1C1E24?style=flat&logo=clerk&logoColor=6E4BF1)

## ✨ Features

- 🧠 AI-Powered Generation: Generate diverse coding challenges and MCQs powered by AI.
- 📚 Challenge Management: Create, view, and manage your library of challenges.
- 🔐 Secure Authentication: Full user authentication and session management powered by Clerk.
- 💾 Persistent History: All your generated challenges are saved to your personal history.
- 📱 Responsive Design: A clean, modern interface that works perfectly on desktop and mobile.
- ⚡ Real-Time API: A high-performance backend built with FastAPI and SQLite.

## 🛠️ Tech Stack

### Frontend
- React.js - UI Framework
- Vite - Build Tool & Dev Server
- CSS Modules - Styling

### Backend
- FastAPI - Python Web Framework
- SQLite - Database
- SQLAlchemy - ORM
- UV - Dependency Management

### Authentication
- Clerk.dev - User Management & Auth

### Version Control
- Git & GitHub

## 📁 Project Structure

```
code-challenge-generator/
├── backend/                 # FastAPI Application
│   ├── src/
│   │   ├── app.py                 # Main FastAPI application instance
│   │   ├── ai_generator.py        # Logic for AI challenge generation
│   │   ├── database/
│   │   │   ├── db.py              # Database connection & session setup
│   │   │   └── models.py          # SQLAlchemy data models
│   │   └── routes/
│   │       ├── challenge.py       # Routes for challenge generation & history
│   │       └── webhooks.py        # Routes for Clerk webhooks
│   ├── requirements.txt            # UV dependencies
│   ├── .env.example              # Example environment variables
│   └── .gitignore
├── frontend/                # React.js Application
│   ├── src/
│   │   ├── App.jsx                 # Main application component
│   │   ├── index.css              # Global styles
│   │   ├── auth/
│   │   │   ├── AuthenticationPage.jsx  # Sign-in/Sign-up page
│   │   │   └── ClerkProviderWithRoutes.jsx # Auth context provider
│   │   ├── challenge/
│   │   │   ├── ChallengeGenerator.jsx # UI for generating new challenges
│   │   │   └── MCQChallenge.jsx      # Component for displaying an MCQ
│   │   ├── history/
│   │   │   └── HistoryPanel.jsx      # Component for viewing challenge history
│   │   └── layout/
│   │       └── Layout.jsx            # Main layout component (header, nav, etc.)
│   ├── package.json
│   ├── vite.config.js           # Vite configuration
│   ├── .env.example              # Example environment variables
│   └── .gitignore
└── README.md                   # This file
```

## 🚦 Getting Started

### Prerequisites
- Node.js (v18 or higher) - [Download](https://nodejs.org/)
- Python (3.9 or higher) - [Download](https://www.python.org/)
- UV - Install via: `pip install uv` or see [official docs](https://docs.astral.sh/uv/)
- Git

### Installation & Setup

1. Clone the Repository

```
git clone <your-repo-url>
cd code-challenge-generator
```

2. Setup the Backend

```
# Navigate to the backend directory
cd backend

# Copy the example environment file and configure your secrets
cp .env.example .env
# Edit .env with your API keys (OpenAI, Clerk)

# Install Python dependencies using UV
uv pip install -r requirements.txt

# Start the FastAPI development server
uvicorn src.app:app --reload
```

The backend API will now be running on http://localhost:8000. You can explore the interactive API docs at http://localhost:8000/docs.

3. Setup the Frontend (in a new terminal)

```
# Navigate to the frontend directory from the project root
cd frontend

# Install npm dependencies
npm install

# Copy the example environment file
cp .env.example .env
# Edit .env and add your Clerk Frontend API key

# Start the Vite development server
npm run dev
```

The frontend application will now be running on http://localhost:5173.

4. Open Your Browser

Navigate to http://localhost:5173 and start using the application!

### ⚙️ Environment Variables

For the application to run correctly, you need to set up API keys.

**Backend** (/backend/.env):

```
DATABASE_URL="sqlite:///./database.db"
CLERK_SECRET_KEY="sk_test_..."
OPENAI_API_KEY="sk-..."
```

**Frontend** (/frontend/.env):

```
VITE_CLERK_PUBLISHABLE_KEY="pk_test_..."
VITE_API_BASE_URL="http://localhost:8000" # Points to your local backend
```

You must create accounts with [OpenAI](https://openai.com/) and [Clerk](https://clerk.dev/) to obtain these keys.

## 🤝 Contributing

We love contributions! Please follow these steps to contribute:

1. Fork the project on GitHub.
2. Create a Feature Branch: `git checkout -b feature/amazing-feature`
3. Commit your Changes: `git commit -m 'Add some amazing feature'`
4. Push to the Branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

Please ensure your code follows existing styles and includes tests where appropriate.

## 📄 License

This project is distributed under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- [Clerk.dev](https://clerk.dev/) for providing an excellent and easy-to-use authentication service.
- [FastAPI team](https://fastapi.tiangolo.com/) for the fantastic, modern Python framework.
- [OpenAI](https://openai.com/) for the powerful GPT API that drives challenge generation.
- [Shields.io](https://shields.io/) for the cool badges.

## 📧 Contact

**Pulitha Marasinghe**

- **GitHub**: [@Pulitha-m](https://github.com/Pulitha-m)
- **Email**: pulithamarasinghe@gmail.com
- **Project Link**: [https://github.com/Pulitha-m/code-challenge-generator](https://github.com/Pulitha-m/code-challenge-generator)
