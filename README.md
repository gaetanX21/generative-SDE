# Score-Based Generative Modeling in PyTorch

![pc_sample](https://github.com/gaetanX21/generative-SDE/blob/main/report/assets/pc.png)

_Realistic generated MNIST samples using Predictor-Corrector Sampling with reverse SDE + Langevin Dynamics._

## Overview

This repository implements score-based generative modeling techniques in PyTorch, based on the foundational works of Song et al. The project includes the construction and training of a score network using the MNIST dataset and implements various sampling methods derived from the original score-based framework. Additionally, it explores controlled generation techniques, including conditional generation and inpainting.

## Introduction

In 2020, Song et al. introduced a generative modeling framework where samples are produced using Langevin dynamics using gradients from the data distribution [[1]](https://github.com/gaetanX21/generative-SDE/blob/main/papers/score_langevin.pdf). These gradients are estimated through denoising a technique called denoising score matching [[3]](https://github.com/gaetanX21/generative-SDE/blob/main/papers/score_denoising.pdf). Song et. al then generalized their framework under the lens of stochastic differential equations (SDEs) [[2]](https://github.com/gaetanX21/generative-SDE/blob/main/papers/score_sde.pdf). This repository aims to summarize and connect the contributions of the three aforemetioned papers on score-based generative modeling.

### Key Contributions

1. **Score Network Construction**: A neural network (the score network $s_\theta(\mathbf{x}, t)$) is constructed and trained from scratch.
2. **Sampling Methods**: Implementation of various sampling methods as outlined in Song et al.'s works.
3. **Controlled Generation**: Extension of sampling methods to controlled generation, specifically:
   - Conditional generation
   - Inpainting

### File Structure

- `code/`: Contains the self-contained Jupyter notebook for the project.
- `report/`: Contains the project report, including a detailed explanation of the score-based generative modeling framework and the implementation of the score network, as well as illustrative results.
- `papers/`: Contains the foundational papers by Song et al. as well as Vincent's paper on denoising score matching.

## References

- [Song, Y., & Ermon, S. (2019). _Generative Modeling by Estimating Gradients of the Data Distribution_.](https://github.com/gaetanX21/generative-SDE/blob/main/papers/score_langevin.pdf) Advances in Neural Information Processing Systems 32 (NeurIPS).

- [Song, Y., Sohl-Dickstein, J., Kingma, D. P., Kumar, A., Ermon, S., & Poole, B. (2021). _Score-Based Generative Modeling through Stochastic Differential Equations_.](https://github.com/gaetanX21/generative-SDE/blob/main/papers/score_sde.pdf) arXiv preprint arXiv:2011.13456.

- [Vincent, P. (2011). _A Connection Between Score Matching and Denoising Autoencoders_.](https://github.com/gaetanX21/generative-SDE/blob/main/papers/score_denoising.pdf) Neural Computation, 23(7), 1661–1674.
