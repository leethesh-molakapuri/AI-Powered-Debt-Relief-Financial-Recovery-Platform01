# FinRelief AI 🚀
### AI-Powered Debt Relief & Financial Recovery Platform

FinRelief AI is a modern, full-stack application designed to empower individuals on their journey toward financial recovery and debt settlement. By integrating a responsive React frontend, a high-performance FastAPI backend, and Google Gemini AI, FinRelief AI helps users assess their financial health, prioritize debts, predict realistic settlement options, and generate tailored negotiation strategies.

---

## 🌟 Key Features

- **🔒 Secure Authentication:** JWT-based user registration and login with encrypted password hashing (Bcrypt).
- **📋 Debt & Loan Management:** Add, edit, and track loans, including principal balances, interest rates, minimum payments, and creditor information.
- **📊 Financial Profile Engine:** Calculates key metrics like Debt-to-Income (DTI) ratio, monthly disposable income, and a personalized Financial Health Score.
- **🔮 Settlement Prediction System:** Predicts recommended settlement targets and assigns priority levels to debts based on creditor history, age of debt, and financial capacity.
- **🤖 AI Negotiation Strategy Engine:** Uses the Google Gemini API to draft custom creditor negotiation strategies and formal settlement letters.
- **🛡️ Robust AI Fallback System:** Local rule-based engines automatically take over if the AI API is offline or rate-limited.
- **📈 Interactive Dashboard:** Beautiful data visualization using Recharts, giving users an immediate overview of their overall financial health and settlement opportunities.

---

## 🛠️ Technology Stack

### Frontend
- **Framework:** React.js (built with Vite)
- **Routing:** React Router v6
- **HTTP Client:** Axios
- **Data Visualization:** Recharts
- **Styling:** Premium Vanilla CSS Custom Design System

### Backend
- **Framework:** FastAPI (Python 3.10+)
- **Database ORM:** SQLAlchemy
- **Database Engine:** SQLite (stored locally as `finrelief.db`)
- **Authentication:** JWT (JSON Web Tokens) via `python-jose` and password hashing with `bcrypt`
- **AI Service:** Google Generative AI (Gemini SDK)
- **Validation:** Pydantic v2
- **Testing:** Pytest

---

## 📂 Project Structure

```text
FinReliefAI/
│
├── backend/                  # FastAPI Backend Service
│   ├── app/
│   │   ├── models.py         # SQLAlchemy Database Models
│   │   ├── database.py       # DB Connection & Session Management
│   │   ├── schemas.py        # Pydantic Schemas for Data Validation
│   │   ├── auth.py           # Authentication Utilities (JWT, Hashing)
│   │   ├── routers/          # API Endpoints (auth, loans, settlements, AI logs)
│   │   └── services/         # Core Engines (financial engine, AI, settlement prediction)
│   ├── tests/                # Test Suite (Pytest)
│   ├── requirements.txt      # Python Dependencies
│   └── .env.example          # Backend Environment Variables Template
│
├── frontend/                 # React Frontend Service
│   ├── src/
│   │   ├── api/              # Axios API Client Configuration
│   │   ├── components/       # Reusable Components (Charts, Navbar, Cards)
│   │   ├── pages/            # Page Views (Dashboard, Financial Health, Loans, etc.)
│   │   ├── App.jsx           # Main React App & Router Setup
│   │   └── index.css         # Styling Tokens & Custom Design System
│   ├── package.json          # Frontend Dependencies & Scripts
│   └── .env.example          # Frontend Environment Variables Template
│
└── docs/                     # Project Workflow & Database Schema Diagrams
```

---

## 🚀 Getting Started

### Prerequisites
Make sure you have the following installed:
- Python 3.10 or higher
- Node.js (v18 or higher) & npm

---

### Backend Setup

1. **Navigate to the backend folder:**
   ```bash
   cd backend
   ```

2. **Create a virtual environment & activate it:**
   ```bash
   python -m venv venv
   # On Windows (PowerShell)
   .\venv\Scripts\Activate.ps1
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install the dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables:**
   Copy `.env.example` to `.env` and fill in your variables:
   ```bash
   cp .env.example .env
   ```
   Add your `GEMINI_API_KEY` for AI features.

5. **Run the FastAPI server:**
   ```bash
   uvicorn app.main:app --reload
   ```
   The backend will be available at [http://127.0.0.1:8000](http://127.0.0.1:8000). You can access the interactive API docs at [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs).

---

### Frontend Setup

1. **Navigate to the frontend folder:**
   ```bash
   cd ../frontend
   ```

2. **Install the dependencies:**
   ```bash
   npm install
   ```

3. **Configure environment variables:**
   Copy `.env.example` to `.env`:
   ```bash
   cp .env.example .env
   ```

4. **Start the development server:**
   ```bash
   npm run dev
   ```
   The frontend will run locally at [http://localhost:5173](http://localhost:5173).

---

## 🧪 Running Tests

The backend includes a comprehensive suite of unit and integration tests. To run them, execute:

```bash
cd backend
pytest
```

---

## 📜 License

This project is licensed under the MIT License.
