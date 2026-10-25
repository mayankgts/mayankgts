<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
  <img src="assets/header-light.svg" alt="Mayank Sharma, AI engineer" width="100%">
</picture>

I study how deep learning models read real signals, mainly heartbeats and video, and I build the systems around them, from CUDA kernels to a build cache in Go. Currently an M.Tech CSE student at Manipal Institute of Technology, Bengaluru, and an intern on Medtronic's AI SDLC team.

[LinkedIn](https://www.linkedin.com/in/mayankgts/) · [Email](mailto:vashishth260302@gmail.com)

## Research

**Noise-Robust ECG Arrhythmia Detection with Explainable 1D-CNN**\
Presented at IEEE InC4 2026, CHRIST University, Bengaluru

Beat-level arrhythmia classification over the five AAMI classes (N, S, V, F, Q). A 1D-CNN with a squeeze-and-excitation block after each convolution learns which feature channels matter for each beat, and Grad-CAM shows which part of the waveform drove the prediction.

**When does temporal history help video super-resolution? An oracle analysis**\
In preparation, targeting IEEE Signal Processing Letters

Recurrent VSR models like BasicVSR++ reuse features from past frames, which helps on static content and causes ghosting where content is newly revealed. For every pixel, an oracle picks whichever output, with history or without, lands closer to ground truth, measured on REDS4 across a grid of HEVC compression levels. Earlier prototype: [temporal-confidence-vsr](https://github.com/mayankgts/temporal-confidence-vsr).

## Projects

### [Anvil](https://github.com/mayankgts/anvil)

A remote build cache for Bazel, written in Go. It implements the Remote Execution API, stores build outputs by their SHA-256 fingerprint, and returns them when anyone runs the same build step again.

| | First build | After `bazel clean` |
|---|---|---|
| Action | ran locally | remote cache hit |
| Critical path | 5.19 s | **0.05 s** |

Milestone 1 works with real Bazel builds. Eviction, remote execution and multi-node distribution are next.

| Project | What it does | Stack |
|---|---|---|
| [GPU Trading Simulator](https://github.com/mayankgts/GPU-Trading-Simulator) | Streams a live order book and estimates slippage and price impact on the GPU | CUDA C++, FastAPI, WebSockets |
| [Credit Risk Engine](https://github.com/mayankgts/Credit-Risk-Assessment) | PD model, WoE/IV feature selection, scorecard, and expected loss (PD × LGD × EAD) | Python, Scikit-learn, Power BI |
| [Car Popularity Classifier](https://github.com/mayankgts/car-popularity-classification) | Rates a car's popularity from its specs, with an interactive app | Scikit-learn, Streamlit |
| [Used Car Price Prediction](https://github.com/mayankgts/Data-Science-Projects) | Price model and market analysis for used cars in Indian metro cities | Pandas, Jupyter |

## Toolkit

**Languages** Python, Go, C++, CUDA, JavaScript\
**ML** PyTorch, Scikit-learn, Pandas, NumPy\
**Systems** gRPC, FastAPI, WebSockets, Bazel, Linux, Git
