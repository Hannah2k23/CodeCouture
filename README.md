Myntra-style Baseline E-commerce Prototype (Local Hackathon Build)
Summary: This repository provides a runnable baseline e-commerce application styled and branded for the Myntra hackathon. It includes a product catalog, product pages, search/filter/sort, cart, wishlist, mock checkout, local (mock) auth, and a minimal admin upload interface. The frontend is a Vite + React app and the backend is FastAPI (Python) using a lightweight JSON/SQLite data store. All brand text is set to Myntra; no trademarked logos are included. Run locally on CPU — demo-ready with generated sample data.
Quick start (2–3 minutes)
# 1. Create virtualenv and install backend deps
python -m venv .venv
source .venv/bin/activate
pip install -r backend/requirements.txt

# 2. Generate sample data (200 SKUs)
python scripts/generate_sample_catalog.py --count 200

# 3. Start backend
cd backend
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

# 4. Start frontend (in another terminal)
cd frontend
npm install
npm run dev

# 5. Visit frontend (Vite will show the local host port) and backend OpenAPI docs:
Backend OpenAPI: http://localhost:8000/docs
# Run with Docker Compose
docker-compose up --build

# Tests
# Ensure backend is running, then:
cd backend
pytest -q



