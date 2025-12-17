# Flows

Lightweight playground to study normalizing flows and reproduce small toy models inspired by recent papers. Structure and styling loosely follow [janosh/awesome-normalizing-flows](https://github.com/janosh/awesome-normalizing-flows).

## Papers to Review
- [Likelihood-free MCMC with normalizing flows (2019)](https://arxiv.org/pdf/1912.02762)
- [Neural ODEs for continuous normalizing flows (2018)](https://arxiv.org/pdf/1812.01729)
- [FALCON: Few-step accurate likelihoods for continuous flows (2025)](https://arxiv.org/pdf/2512.09914) — hybrid training objective enabling fast few-step sampling and invertibility.

## Planned Toy Models
- **1D Gaussian mixture flow**: affine coupling layers to match a multi-modal target; visualize density before/after training.
- **Spiral to Gaussian CNF**: simple Neural ODE baseline to mirror ideas from the CNF paper.
- **Few-step FALCON-style flow**: small U-Net/MLP backbone with cycle-consistency loss to test few-step likelihood estimates.
- **MCMC + flow proposal**: pair a trained flow with Metropolis-Hastings to explore the likelihood-free MCMC setup.

## Repository Layout (planned)
- `notebooks/` — quick experiments and visualizations.
- `flows/` — minimal reusable layers (coupling, splines, CNF blocks).
- `scripts/` — training entrypoints for each toy setup.

## Getting Started
1) Create a venv and install deps (to be added).
2) Run the notebooks to reproduce the toy experiments.
3) Iterate on architectures/losses while comparing against the referenced papers.

## Goals
- Reproduce key behaviors from each paper with minimal code.
- Compare training stability, likelihood estimates, and sampling speed across discrete flows, CNFs, and the FALCON approach.
- Keep examples small, clear, and easy to extend.