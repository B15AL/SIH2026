# SIH26145 — Passive AI Cyber-Threat Detection

> **Smart India Hackathon 2026 · PS 26145 · NTRO** — AI-based detection of cyber threats in unidirectional IP traffic using passive, read-only analysis.
## Demo principle

The primary detection path remains local and deterministic/measurable. The optional small local LLM only explains already-generated structured alerts; it does not make or change detection decisions.

## Run the local demo

### Option A: local processes

```bash
python -m pip install -e 'backend[test]'
uvicorn sih_detector.api:app --app-dir backend/src --reload
```

In a second terminal:

```bash
cd frontend
npm install
npm run dev
```

Open `http://localhost:5173`, select a scenario, and start replay. The dashboard uses the local API and WebSocket by default. No network capture, Appwrite credentials, or external AI API is required.

### Option B: Docker Compose

```bash
docker compose up
```

The same dashboard is available at `http://localhost:5173`.

## License

Licensed under the [Apache License, Version 2.0](LICENSE).
