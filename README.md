# Lightweight Technical RAG Exam API

This version uses a small pure-Python BM25 retriever. It does not load neural
embedding models, NumPy, SciPy, or scikit-learn, helping it fit small RAM
instances.

## Render settings
Build command: `pip install -r requirements.txt`
Start command: `uvicorn main:app --host 0.0.0.0 --port $PORT`

## Endpoints
- `GET /health`
- `POST /query` with `{"question":"...", "top_k":3}`

The 50 technical passages are embedded in `main.py`.
