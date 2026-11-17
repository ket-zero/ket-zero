# ket-zero

> Learning quantum computing by building it: study notes, an open-source quantum simulator in Go, and the tools around it.

[![License: Apache-2.0](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](LICENSE)

`ket-zero` is named after the |0⟩ state, the starting point of nearly every quantum computation. This repository is the hub of the **ket-zero** organization. It holds the study notes and explains how the other projects fit together.

## What's in the org

| Project | What it is | Where | Status |
|---------|-----------|-------|--------|
| Study notes | Math and physics foundations, course notes, derivations and worked problems | `notes/` in this repo | Starting week 1 (23 Nov 2026) |
| **qgo** (working name) | A state-vector and density-matrix quantum simulator in Go, with a CLI, circuit drawer, OpenQASM 3 import and a browser playground | separate repo, `github.com/ket-zero/qgo` | v0.1 planned for week 5 |
| Q# algorithm library | QFT, phase estimation, Grover, Shor-15 and arithmetic circuits in Q#, exported to OpenQASM and cross-checked on qgo | separate repo | Planned, weeks 17–19 |
| OpenQASM standard library | Reusable OpenQASM 3 gate definitions (QFT, adders, oracles, Grover diffuser) that ship with qgo | inside qgo | Planned, week 20 |
| Post-quantum crypto notes | What quantum computers mean for today's cryptography, including a resource estimate for breaking RSA-2048 | `notes/pqc/` in this repo | Ongoing |

See [docs/overview.md](docs/overview.md) for goals, scope and the roadmap.

## Repository layout

```
ket-zero/
├── README.md        # you are here
├── LICENSE          # Apache-2.0
├── docs/
│   └── overview.md  # goals, scope, roadmap, decisions
└── notes/           # study notes (added from week 1)
```

## Contributing

This is primarily a personal learning project, done in public. Corrections to the notes, questions and issues are very welcome. Please read the [contributing guide](https://github.com/ket-zero/.github/blob/main/CONTRIBUTING.md) and open an issue before sending a large pull request.

## License

Licensed under the [Apache License, Version 2.0](LICENSE).
