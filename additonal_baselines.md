## Additional Baselines

We report the performance of Deterministic Uncertainty Quantification (DUQ) and Spectral-normalized Neural Gaussian Process (SNGP) on the in-domain task (ResNet-20 on CIFAR-10) as well as the out-of-domain tasks (SVHN and Flowers102).

In-domain:
| **Optimizer** | **Top-1 Acc.** $\uparrow$ | **Top-5 Acc.** $\uparrow$ | **NLL** $\downarrow$ | **ECE** $\downarrow$ | **Brier** $\downarrow$ |
|---|---:|---:|---:|---:|---:|
| DUQ | 91.27 (0.20) | 99.60 (0.09) | 0.283 (0.010) | 0.023 (0.002) | 0.130 (0.003) | 
| SNGP | 91.39 (0.27) | 99.68 (0.04) | 0.305 (0.85) | 0.043 (0.001) | 0.133 (0.004) |
| **uCBOpt $(\vartheta=4 \cdot 10^{-6})$** | **92.52 (0.10)** | **99.67 (0.04)** | **0.278 (0.011)** | **0.038 (0.003)** | **0.118 (0.003)** |

Out-of-domain (SVHN):
| **Optimizer** | **FPR@95\%** $\downarrow$ | **Det. Err.** $\downarrow$  | **AUROC** $\uparrow$ | **AUPR-In** $\uparrow$ | **AUPR-Out** $\uparrow$ |
|---|---:|---:|---:|---:|---:|
| DUQ | 21.1 (2.9) | 19.5 (1.4) | 86.0 (1.4) | 76.8 (5.9) | 91.8 (1.2) | 
| SNGP | 22.4 (2.5) | 19.6 (1.3) | 85.9 (1.5) | 80.4 (1.7) | 91.3 (1.1) |
| **uCBOpt $(\vartheta=4 \cdot 10^{-6})$** | **21.9 (1.2)** | **19.0 (0.9)** | **86.7 (0.8)** | **81.7 (1.0)** | **91.8 (0.6)** |

Out-of-domain (Flowers102):
| **Optimizer** | **FPR@95\%** $\downarrow$ | **Det. Err.** $\downarrow$  | **AUROC** $\uparrow$ | **AUPR-In** $\uparrow$ | **AUPR-Out** $\uparrow$ |
|---|---:|---:|---:|---:|---:|
| DUQ | 25.5 (1.0) | 22.0 (1.7) | 84.2 (2.6) | 89.2 (3.1) | 74.8 (2.1) | 
| SNGP | 21.7 (0.7) | 19.8 (0.3) | 87.0 (0.3) | 92.5 (0.2) | 76.4 (0.6) |
| **uCBOpt $(\vartheta=4 \cdot 10^{-6})$** | **21.8 (1.4)** | **19.2 (1.4)** | **87.6 (1.1)** | **93.0 (0.8)** | **77.0 (1.6)** |
