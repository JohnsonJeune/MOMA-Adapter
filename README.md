# MOMA-Adapter

**From Simulated to Real-World Signals: Motion-Text Mutual Adaptation for Few-Shot Wearable Activity Recognition**

MOMA-Adapter is a lightweight multimodal adaptation framework built upon a frozen pretrained motion-language model. It establishes **bidirectional motion-text mutual guidance** to bridge the simulation-to-real distribution gap for few-shot wearable Human Activity Recognition (HAR).

> **Status:** This is a public manuscript draft. The **Methodology** (Section III) and **Experiments** (Section IV) sections are intentionally omitted and under active development; the paper skeleton mirrors the IEEE/DCT-PT structure.

## Contents

| File            | Description                                             |
|-----------------|---------------------------------------------------------|
| `main.tex`      | IEEE LaTeX manuscript (abstract, intro, related works)  |
| `refs.bib`      | Bibliography of referenced works                        |

## Build

Compile with a standard LaTeX toolchain (IEEEtran class, `cite`, `amsmath`):

```bash
pdflatex main
bibtex   main
pdflatex main
pdflatex main
```

## Key Ideas

- **Simulation-to-real gap:** pretrained motion-language models (e.g., UniMTS) are trained on simulated IMU signals and face a substantial distribution shift when transferred to real wearable sensing.
- **Bidirectional mutual guidance:** a Text-to-Motion Guidance Module (T2M-GM) injects textual semantics into motion prototypes, while a Motion-to-Text Guidance Module (M2T-GM) refines textual representations from real-world IMU prototypes.
- **MOMA-HP:** lightweight automatic hyperparameter optimization across few-shot scenarios.
- **MOMA-F:** preference-guided refinement of the classification decision boundary using few-shot motion-text relationships.

## License

TBD
