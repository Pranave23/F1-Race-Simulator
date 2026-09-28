# ML Simulation Package

The **ml_simulation** package implements the core scientific engine of the F1 Race Simulator. It provides:

- **Degradation Model** – a trained model that predicts tyre wear, fuel consumption, and performance loss over laps based on historical telemetry.
- **Monte Carlo Engine** – runs thousands of stochastic race simulations to capture uncertainty in strategy outcomes.
- **API Layer** – simple Python functions that the backend can call to obtain lap‑by‑lap results and statistical summaries.

The package is deliberately stateless; given the same seed and inputs it will produce reproducible results, which is important for debugging and for the LLM explanation layer.

---
