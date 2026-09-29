# CompMind — Competitive Intelligence Agent

A memory-first competitive intelligence agent. It connects new competitor signals with historical context using Hindsight when configured, and falls back to demo memory without API keys.

## Local run

```bash
python -m venv .venv
# Windows
.venv\\Scripts\\activate
# macOS/Linux
# source .venv/bin/activate
pip install -r requirements.txt
copy .env.example .env
uvicorn app.main:app --reload
```

Open http://127.0.0.1:8000

## Render

The included `render.yaml` is configured for a Python web service using:
`uvicorn app.main:app --host 0.0.0.0 --port $PORT`

Set `HINDSIGHT_API_KEY` (and optionally `GROQ_API_KEY`) in Render environment variables. Never commit `.env` or API keys.
