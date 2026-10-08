# Insurance Claims Support Copilot

FastAPI + LangChain/LangMem + ChromaDB backend with a Streamlit dashboard.

## Local setup (Windows / macOS / Linux)

1. Install [uv](https://docs.astral.sh/uv/). It fetches Python 3.11 automatically.
2. `uv sync --dev`
3. Copy `.env.example` to `.env` and fill in `GROQ_API_KEY` and `GOOGLE_API_KEY`.
4. Start the API: `uv run python main.py` (http://localhost:8000, docs at `/docs`)
5. In a second terminal, start the dashboard: `uv run streamlit run app.py` (http://localhost:8501)
6. Run tests: `uv run pytest -q`

Runtime data (SQLite DB and Chroma indexes) is written to `data/`.

## Docker

`docker compose up --build` (reads `.env`).

See `docs/` for architecture and EC2 deployment details.
