# F1 Race Simulator

A web platform that reconstructs historical Formula 1 races lap‑by‑lap from publicly available telemetry data. Users can tweak strategic variables (e.g., tyre choices, pit‑stop timing), re‑run the race using a trained degradation model combined with a Monte Carlo simulation, and receive plain‑language explanations of the outcomes powered by an LLM.

## Key Features
- **Historical reconstruction** – Ingests public telemetry and builds a lap‑by‑lap timeline.
- **Strategic experimentation** – Adjust tyre compounds, fuel loads, pit‑stop windows, etc.
- **Monte Carlo engine** – Runs thousands of stochastic simulations to forecast race results under varied strategies.
- **LLM insight layer** – Generates human‑readable summaries and rationales for simulated outcomes.
- **Modular architecture** – Front‑end (React), back‑end (FastAPI/Python), ML‑simulation library, and documentation.

## Quick Start
```bash
# Clone the repo
git clone https://github.com/Pranave23/F1-Race-Simulator.git
cd F1-Race-Simulator

# Launch services with Docker Compose
docker-compose up --build
```

The API will be available at `http://localhost:8000`, and the UI at `http://localhost:3000`.

## Repository Layout
- `backend/` – FastAPI server, ML simulation package, and model artefacts.
- `frontend/` – React application for the UI.
- `docs/` – Architecture decision records and project documentation.


<<<<<<< HEAD
Default tyre compound: Soft
=======
Default tyre compound: Hard
>>>>>>> contributor-b
