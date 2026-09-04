# Quran Revision & Competition Web App

A full-stack Quran revision and memorization platform with Arabic-first RTL UI, responsive layout, and a maintainable architecture for future Quran data import and speech-recognition integration.

## Overview

This project follows a modular monorepo structure:

- frontend: Vite + React + TypeScript + RTL-first UI
- backend: FastAPI + SQLAlchemy + Pydantic
- database: SQLite by default, PostgreSQL-ready
- docs: architecture and roadmap notes

## Project structure

- frontend/
- backend/
- database/
- docs/
- .env.example
- README.md

## Requirements

- Node.js 20+
- Python 3.11+
- SQLite support (bundled with Python)

## Environment setup

1. Copy .env.example to .env.
2. Update secrets and database URL if needed.
3. Create a virtual environment for Python.

## Backend setup

```bash
cd backend
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```

## Frontend setup

```bash
cd frontend
npm install
npm run dev -- --host 0.0.0.0
```

## Database

Default development database is SQLite. The backend can later be pointed to PostgreSQL by updating DATABASE_URL in .env.

## Testing

```bash
cd backend
pytest
```

```bash
cd frontend
npm run build
```

## Known limitations

- Quran text data is intentionally not fabricated.
- A verified Riwayat Qalun dataset must be imported before production usage.
- Speech-recognition and error detection are intentionally left as future architecture placeholders.
