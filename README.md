# PILA macOS / Apple Silicon Edition

This repository contains a macOS- and Apple Silicon–compatible implementation
of the PolyTrack Imitation Learning Agent (PILA).

This work is adapted from the original PILA project:
https://github.com/tryfonaskam/pila

The goal of this repository is to provide a stable macOS workflow
(screen capture, training, and inference) without affecting the main codebase.

## Key Differences

- macOS-safe screen capture backend
- Apple Silicon (MPS) training support
- Stable long-running training on macOS laptops

## Quick Start (macOS)

Environment setup:
```
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Record data:
```
python -m capture.datasetmake
```

Train:
```
python train.py
```

Run agent:
```
python play.py
```

## Credits

**[tryfonaskam](https://github.com/tryfonaskam)** — Project author and lead developer.
Designed and implemented the original PILA imitation learning pipeline, including data capture, dataset organization, neural network architecture, training workflow, checkpointing, and real-time inference. Responsible for the initial model training, experimentation, documentation, and overall project execution.

**[sahusaurya](https://github.com/sahusaurya)** — Project ideation and macOS / Apple Silicon pipeline implementation.
Contributed to early project direction by helping identify PolyTrack as an appropriate environment for imitation learning and assisting with test environment setup. Additionally designed and implemented a macOS- and Apple Silicon–specific variant of the PILA pipeline, including a rewritten screen capture and input subsystem, canonical 512×512 preprocessing across data collection, training, and inference, Apple Silicon (MPS)–based training support, and independent model training and experimentation on macOS systems.
