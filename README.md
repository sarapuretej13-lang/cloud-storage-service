# ☁️ Cloud Storage Service

A full-stack cloud storage web application similar to Google Drive, built from scratch.

## Features
- 📧 Email & Google OAuth authentication
- 📁 File & folder management (upload, download, rename, move)
- 👁️ File preview (images, PDFs, videos)
- ⭐ Starred files
- 🗑️ Trash & restore
- 🔗 File sharing with permissions (Viewer / Editor / Owner)
- 🌐 Public shareable links with expiry
- 🔍 Search & sort
- 📊 Storage stats

## Tech Stack
- **Backend:** Python, FastAPI, SQLAlchemy, PostgreSQL (Supabase), JWT, Google OAuth
- **Frontend:** HTML, CSS, Vanilla JavaScript
- **Database:** PostgreSQL hosted on Supabase

## Run Locally

### Backend
```
cd backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
```

### Frontend
```
cd frontend
python -m http.server 5500
```

Open `http://localhost:5500/index.html` in your browser.

## Environment Variables
Create a `.env` file in the `backend` folder:
```
DATABASE_URL=your_postgresql_url
SECRET_KEY=your_secret_key
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
GOOGLE_REDIRECT_URI=http://localhost:8000/auth/google/callback
FRONTEND_URL=http://localhost:5500
```
