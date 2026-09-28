# Simulation Submodule

The **simulation** submodule implements the Monte Carlo engine that drives the race outcome predictions. It provides:

- **run_simulation** – a function that accepts a race context, strategy parameters, and a random seed, then executes thousands of stochastic runs of the degradation model.
- **aggregate_results** – utilities to compute statistical summaries (e.g., win probability, lap‑time distributions, pit‑stop timing histograms).
- **visualisation helpers** – optional functions to produce data structures ready for plotting on the frontend (e.g., per‑lap position charts).

The engine is deliberately decoupled from data loading; it operates on already‑preprocessed telemetry and model inputs, making it easy to test and benchmark.

---

