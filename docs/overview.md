# Project Overview

## Vision

Learn quantum computing by building it. Every concept from the course (qubits, gates, entanglement, measurement, algorithms) gets a matching piece of working code and a written explanation.

## Goals

1. **Understand deeply**: keep clear, self-written notes that connect the math to the code.
2. **Build a simulator**: a from-scratch state-vector simulator that can run textbook circuits.
3. **Implement algorithms**: reproduce the canonical quantum algorithms on top of the simulator.
4. **Stay reproducible**: every example runnable with a single command.

## Non-goals

- Competing with production frameworks (Qiskit, Cirq, PennyLane).
- Running on real quantum hardware (may be explored later as a stretch goal).

## Components

### 1. Study notes (`notes/`)
Markdown (with LaTeX math) organized by course topic: linear algebra refresher, qubits and Bloch sphere, gates and circuits, measurement, entanglement, algorithms, error correction.

### 2. Simulator (`simulator/`)
- State-vector representation of n qubits
- Single- and multi-qubit gates (H, X, Y, Z, S, T, CNOT, CZ, SWAP, Toffoli, rotations)
- Measurement with sampling and collapse
- Circuit builder API and text/ASCII circuit drawing
- Later: noise models, density matrices

### 3. Algorithms (`algorithms/`)
Deutsch–Jozsa, Bernstein–Vazirani, Simon, Grover, Quantum Fourier Transform, phase estimation, Shor (small-scale).

### 4. Experiments (`experiments/`)
Notebooks and scratch programs: Bell inequality tests, teleportation, superdense coding, visualizations.

## Roadmap

- [ ] **M0: Foundations**: repo setup, README, overview *(this step)*
- [ ] **M1: Notes skeleton**: topic outline matching the course syllabus
- [ ] **M2: Simulator core**: state vector, basic gates, measurement
- [ ] **M3: Circuit API**: builder, drawing, tests against known results
- [ ] **M4: Algorithms**: Deutsch–Jozsa through Grover
- [ ] **M5: QFT, phase estimation, Shor**
- [ ] **M6: Noise and density matrices** *(stretch)*

## Open decisions

- **Implementation language** for the simulator (Python for fast iteration vs. Rust/C++ for performance, or Python with a native core later).
- **Monorepo vs. multiple repos** within the org.
- **License** (MIT or Apache-2.0 are likely candidates).
- **Docs tooling** for rendering notes (plain Markdown, mdBook, or MkDocs).

## References

- Nielsen & Chuang, *Quantum Computation and Quantum Information*
- Course lecture materials
