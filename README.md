# Adversarial Attacks on CNNs (FGSM) 🎯

Training a CNN on street-view digit images — then breaking it with imperceptible pixel perturbations.

PyTorch implementation of the Fast Gradient Sign Method (FGSM) against a CNN classifier trained on SVHN (Street View House Numbers), plus a contrastive-learning component.

## Highlights

- **CNN trained from scratch** on SVHN with heavy augmentation (random crop, flip, color jitter, rotation, random erasing) → **93.1% test accuracy** in 12 epochs
- **FGSM attack**: crafting adversarial examples by perturbing inputs along the gradient sign, demonstrating how confident classifiers fail on inputs that look unchanged to humans
- **Accuracy-vs-epsilon analysis**: quantifying how attack strength degrades model performance
- **Contrastive learning**: representation-learning experiments on the same data

## Why this matters

Adversarial robustness is where machine learning meets security: models deployed in the real world (fraud detection, malware classification, autonomous systems) face adversaries who actively craft inputs to fool them. This project demonstrates the attacker's side of that equation — the first step in building defensible models.

## Stack

PyTorch · torchvision · NumPy · scikit-learn · matplotlib/seaborn

## Run it

```bash
pip install torch torchvision scikit-learn seaborn
jupyter notebook adversarial_attacks_svhn.ipynb
```

SVHN downloads automatically via `torchvision.datasets`.

---

*Built as part of deep-learning coursework in the Data Science & Engineering program at the Technion; extended and cleaned for this repo.*
