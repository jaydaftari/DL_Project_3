# MiniProject 3: Jailbreaking Deep Models
by Jay Daftari (jd5829@nyu.edu), Akshat Mishra (am15111@nyu.edu) and ,Siddhant Mohan (sm12766@nyu.edu).


A hands‑on exploration of adversarial attacks against a pre‑trained ResNet‑34 classifier on ImageNet‑1K. We implement and evaluate five attacks—clean baseline, FGSM, PGD, localized patch, and cross‑model transferability—demonstrating how small, worst‑case perturbations can dramatically degrade modern deep networks.

---

## Overview

This repository contains `dl-hw3.ipynb`, a Jupyter notebook implementing:

1. **Clean baseline evaluation** of ResNet‑34 on a test subset of ImageNet‑1K.  
2. **Fast Gradient Sign Method (FGSM)** for an $L_\infty$ single‑step attack.  
3. **Projected Gradient Descent (PGD)** multi‑step attack under the same perturbation budget.  
4. **Patch‑based attack**, restricting adversarial perturbations to a 32×32 region.  
5. **Transferability study**, evaluating how adversarial examples transfer to DenseNet‑121.

Each section includes code, explanatory text, visualizations, and quantitative results.

---

## Prerequisites

- Python 3.8+  
- PyTorch 1.12+  
- torchvision 0.13+  
- Jupyter Notebook  
- tqdm, numpy, matplotlib, scipy  

---

## Installation

1. Clone this repository
2. Open dl-hw3.ipynb in your browser.
3. Download the  ImageNet-1K dataset and set the path in code accordingly.
4. Execute cells top‑to‑bottom to reproduce baseline and adversarial attacks.

---

## Results

### ResNet‑34 vs. DenseNet‑121 Accuracy Comparison

| Dataset  | ResNet‑34 Top‑1 (%) | ResNet‑34 Top‑5 (%) | DenseNet‑121 Top‑1 (%) | DenseNet‑121 Top‑5 (%) |
|----------|---------------------|---------------------|------------------------|------------------------|
| Original | 76.0                | 94.2                | 74.8                   | 93.6                   |
| FGSM     | 3.4                 | 21.2                | 46.0                   | 76.2                   |
| PGD      | 0.0                 | 4.4                 | 54.8                   | 86.4                   |
| Patch    | 4.0                 | 42.0                | 68.0                   | 91.2                   |



---
## References
Madry, A., Makelov, A., Schmidt, L., Tsipras, D., & Vladu, A. (2018).
Towards Deep Learning Models Resistant to Adversarial Attacks. ICLR.

Goodfellow, I. J., Shlens, J., & Szegedy, C. (2015).
Explaining and Harnessing Adversarial Examples. ICLR.




