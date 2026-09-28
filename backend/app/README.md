# Backend Application

This directory contains the backend application layer for the F1 Race Simulator.
It is responsible for exposing the race reconstruction and simulation capabilities
to the frontend and for coordinating the supporting machine-learning and
simulation modules.

## Product Purpose

The platform reconstructs historical Formula 1 races lap by lap using public
telemetry. Users can change strategic variables, re-simulate the race, and
understand how those changes affect the outcome.

The simulation combines:

- Historical telemetry and race context
- A trained tyre and performance degradation model
- Monte Carlo simulation to represent uncertainty and alternate race outcomes
- An LLM explanation layer that summarizes results in plain language

## Application Responsibilities

The backend application should provide the boundary between the user-facing
product and the domain modules. Its responsibilities include:

1. Accepting race selections and user-defined strategy changes.
2. Loading or requesting the relevant historical race data.
3. Passing validated simulation inputs to the ML and simulation components.
4. Returning lap-by-lap timelines, race outcomes, and uncertainty information.
5. Requesting plain-language explanations of the results through the LLM layer.
6. Handling validation and clear errors when a race or strategy input is invalid.

The reusable degradation models and race simulation logic belong in
`backend/ml_simulation/`; this directory should focus on application orchestration
and the API contract presented to the frontend.

## Typical Request Flow

```text
Frontend request
	|
	v
Validate race and strategy inputs
	|
	v
Load historical telemetry and race context
	|
	v
Run degradation model + Monte Carlo simulation
	|
	v
Build race results and lap-by-lap data
	|
	v
Generate plain-language explanation
	|
	v
Return results to the frontend
```

## Design Goals

- Keep API concerns separate from simulation and model implementation.
- Make simulation inputs reproducible when a seed is supplied.
- Return enough intermediate information to explain why the result changed.
- Keep user-facing responses stable and understandable for the frontend.
- Treat telemetry and model outputs as uncertain estimates, not guarantees.
