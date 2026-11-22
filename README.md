---
title: Technical RAG Exam API
sdk: docker
app_port: 7860
---

FastAPI RAG endpoint for the 50-passage technical knowledge base.

- `GET /health`
- `POST /query` with JSON `{"question":"...", "top_k":3}`

The service embeds the 50 passages with `sentence-transformers/all-MiniLM-L6-v2`,
ranks them by cosine similarity, extracts relevant factual sentences, and abstains
when retrieval confidence is too low.
