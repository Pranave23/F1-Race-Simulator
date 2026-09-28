# Architecture Decision Records (ADR)

This directory contains the project's Architecture Decision Records. Each ADR documents a significant design choice, the context behind it, the considered alternatives, and the rationale for the final decision.

## How to Use
- New decisions should be captured in a separate markdown file following the naming convention `NNNN-description.md` (e.g., `0001-ml-simulation-as-library-not-service.md`).
- Reference the ADR number in code comments or documentation when the decision influences implementation.
- Review existing ADRs to understand why certain technologies or patterns were chosen (e.g., why the simulation is provided as a library rather than a separate service).

The existing ADRs provide background on:
- The choice to expose the ML simulation as a **Python library** for easy integration with the FastAPI backend.
- The decision to use **Monte Carlo** methods for handling uncertainty in race outcomes.
- The approach of using a **LLM** for natural‑language explanations rather than a rule‑based system.

---

