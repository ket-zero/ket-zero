# ket-zero

> Study notes, a quantum circuit simulator, and experiments from my quantum computing course, all in one place.

`ket-zero` is named after the |0⟩ state, the starting point of nearly every quantum computation. This repository is the hub of the **ket-zero** organization: it describes the project, links to the sub-projects, and explains how everything fits together.

## What's in the org

| Area | Purpose | Status |
|------|---------|--------|
| Study notes | Course notes, derivations, and worked problems | Planned |
| Simulator | A state-vector quantum circuit simulator built from scratch | Planned |
| Algorithms | Implementations of standard algorithms (Deutsch–Jozsa, Grover, QFT, Shor, …) | Planned |
| Experiments | Small programs and notebooks for exploring ideas | Planned |

See [docs/overview.md](docs/overview.md) for goals, scope, architecture, and the roadmap.

## Getting started

```bash
git clone https://github.com/ket-zero/ket-zero.git
cd ket-zero
```

Setup instructions for each sub-project will live in that project's own README.

## Repository layout

```
ket-zero/
├── README.md        # you are here
├── docs/
│   └── overview.md  # project overview, goals, roadmap
└── .gitignore
```

Sub-projects will be added as separate repositories in the org (or as top-level folders if kept together).

## Contributing

This is primarily a personal learning project, but suggestions, corrections to the notes, and issues are welcome. Open an issue before sending a large pull request.

## License

To be decided. Until a license file is added, all rights are reserved.
