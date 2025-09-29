# To Run Locally
uvicorn app.main:app --reload

# Setup Instructions

### 1. Backend (FastAPI)

```bash
cd backend
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt
uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
```

> Make sure to create `.env` file and fill in:

```env
DATABASE_URL=postgresql+asyncpg://<user>:<pass>@<host>/<db>
SECRET_KEY=your-secret-key
```

### 2. Frontend (React Native + Expo)

```bash
cd frontend
yarn install
npx expo start
```

> Update API URL in `frontend/config.js`:

```js
export const API_BASE_URL = "http://<your-laptop-ip>:8000";
```

---
