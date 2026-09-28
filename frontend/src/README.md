# Frontend Source Overview

The `frontend/src` directory contains all source code for the React application.

- **components/** – Re‑usable UI components (race selector, strategy editor, results charts, explanation panel).
- **pages/** – Top‑level route components built with React Router.
- **store/** – Redux Toolkit slices that hold the selected race, strategy parameters, simulation results, and loading/error state.
- **api/** – Small wrapper around `fetch`/`axios` that calls the FastAPI backend (`/api/...`).
- **styles/** – Global CSS and theme definitions (Material‑UI theme customisation).
- **utils/** – Helper functions for data transformation, e.g., converting telemetry JSON into chart‑friendly formats.

All components communicate via the Redux store; the UI updates automatically when new simulation data arrives. Development scripts (`npm start`, `npm build`) operate from the top‑level `frontend` folder.

---
