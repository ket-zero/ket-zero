# Project overview

## Vision

Learn quantum computing by building it. Every concept from the course (qubits, gates, entanglement, measurement, algorithms, noise) gets a matching piece of working code and a written explanation.

## Goals

1. **Understand deeply:** keep clear, self-written notes that connect the math and physics to the code.
2. **Ship a real simulator:** an open-source Go simulator (`qgo`, working name) with a clean API, tests, CI, releases and docs.
3. **Implement the algorithms:** reproduce the standard quantum algorithms, in Go on top of qgo and in Q#.
4. **Stay reproducible:** every example runs with a single command, and simulator results are cross-checked against Qiskit Aer in CI.
5. **Connect to today's work:** track post-quantum cryptography alongside the quantum material.

## Non-goals (for v1.0)

- Beating Qiskit Aer, qsim or GPU simulators on speed.
- Pulse-level control, real hardware backends, or the full OpenQASM 3 language.
- A Python-first API. Python access comes later through a job server.

## Components

### 1. Study notes (`notes/` in this repo)
Markdown with LaTeX math, organized by topic: linear algebra and complex numbers, quantum mechanics postulates, qubits and the Bloch sphere, gates and circuits, measurement, entanglement, algorithms, noise and error correction, and post-quantum cryptography.

### 2. qgo, the simulator (`ket-zero/qgo`, separate repo)
- State-vector engine for about 28 qubits on a laptop, standard library only in the core
- Gate library (1- and 2-qubit, controlled, parametric), sampling and partial measurement
- Density-matrix engine with standard noise channels
- OpenQASM 3 importer (a documented subset)
- CLI (`qgo run`, `qgo draw`, `qgo bench`), ASCII and SVG circuit drawings
- WASM build and a browser playground
- Reference algorithms: Bell, GHZ, teleportation, QFT, QPE, Grover, Shor-15

### 3. Quantum-language tools
- **Q# algorithm library:** QFT, QPE, Grover, Shor-15 and arithmetic circuits with Q# unit tests, exported to OpenQASM and checked against qgo in CI.
- **OpenQASM standard library:** reusable `.inc` gate definitions shipped with qgo.
- **"When does RSA break?" report:** Q# resource estimates for Shor on RSA-2048 and ECC P-256.

## Roadmap

Weeks count from Monday 23 November 2026 (week 1) to Sunday 6 June 2027 (week 28).

- [ ] **Week 1:** org and repo setup, licence, community files *(in progress)*
- [ ] **v0.1 (week 5):** 1 to n qubits, gate library, CNOT, sampling measurement, tests, CI
- [ ] **v0.2 (week 12):** circuit API, partial measurement, Bell and teleportation examples, Qiskit cross-checks, `qgo run`, first docs
- [ ] **v0.3 (week 16):** OpenQASM 3 import, `qgo draw`, fuzz tests, parallelism
- [ ] **v0.3.x (weeks 17–20):** algorithms package, WASM playground, Q# library, OpenQASM stdlib
- [ ] **v0.4 (week 24):** density-matrix backend, noise channels, `qgo bench`
- [ ] **RSA report (weeks 25–26):** Q# resource estimation write-up
- [ ] **v1.0 (week 27):** API freeze, polished playground, tutorials, benchmark page
- [ ] **v1.1 (after week 28):** job server, Python/Qiskit provider, stabilizer backend (stretch)

## Decisions

| Decision | Choice | Why |
|----------|--------|-----|
| Simulator language | Go | Daily working language; easy to ship as a single binary and a WASM build |
| Repo layout | Notes and hub here; the simulator in its own repo | Clean Go module path, pkg.go.dev docs, independent tags and releases |
| License | Apache-2.0 | Permissive, with an explicit patent grant |
| Simulator name | `qgo` for now | Check it is free on GitHub and pkg.go.dev before the first public tag |

## Open decisions

- Docs tooling for rendering the notes (plain Markdown, mdBook or MkDocs).
- Whether the notes should also carry a content license such as CC BY 4.0.

## References

- Nielsen & Chuang, *Quantum Computation and Quantum Information*
- Course lecture materials
