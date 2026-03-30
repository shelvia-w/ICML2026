# Low-data Setting

We report the performance of uCBOpt and other baselines on ResNet-20 trained on CIFAR-10 with reduced training samples, for both in-domain and out-of-domain tasks.

## Train Fraction = 10% (5000 training samples)

In-domain:
| **Optimizer** | **Top-1 Acc.** $\uparrow$ | **Top-5 Acc.** $\uparrow$ | **NLL** $\downarrow$ | **ECE** $\downarrow$ | **Brier** $\downarrow$ |
|---|---:|---:|---:|---:|---:|
| **uCBOpt $(\vartheta\to0^{+})$** | **75.98 (1.15)** | **97.96 (0.19)** | **0.938 (0.065)** | **0.130 (0.011)** | **0.369 (0.019)** |
| **uCBOpt $(\vartheta=1 \cdot 10^{-5})$** | **76.80 (0.85)** | **98.09 (0.17)** | **0.886 (0.047)** | **0.122 (0.007)** | **0.354 (0.015)** | 
| IVON@mean | 75.99 (0.33) | 97.94 (0.10) | 0.924 (0.048) | 0.130 (0.006) | 0.367 (0.006) |
| SGD | 76.00 (1.59) | 98.08 (0.16) | 0.942 (0.083) | 0.132 (0.013) | 0.370 (0.026) | 
| AdamW | 66.54 (0.23) | 96.06 (0.20) | 2.374 (0.049) | 0.261 (0.002) | 0.575 (0.004) |

Out-of-domain (SVHN):
| **Optimizer** | **FPR@95\%** $\downarrow$ | **Det. Err.** $\downarrow$  | **AUROC** $\uparrow$ | **AUPR-In** $\uparrow$ | **AUPR-Out** $\uparrow$ |
|---|---:|---:|---:|---:|---:|
| **uCBOpt $(\vartheta\to0^{+})$** | **36.6 (1.4)** | **34.4 (1.2)** | **68.7 (1.8)** | **57.1 (2.0)** | **80.6 (1.3)** |
| **uCBOpt $(\vartheta=1 \cdot 10^{-5})$** | **** | **** | **** | **** | **** | 
| IVON@mean |  |  |  |  |  |
| SGD |  |  |  |  |  | 
| Laplace |  |  |  |  |  | 

Out-of-domain (Flowers102):
| **Optimizer** | **FPR@95\%** $\downarrow$ | **Det. Err.** $\downarrow$  | **AUROC** $\uparrow$ | **AUPR-In** $\uparrow$ | **AUPR-Out** $\uparrow$ |
|---|---:|---:|---:|---:|---:|
| **uCBOpt $(\vartheta\to0^{+})$** | **** | **** | **** | **** | **** |
| **uCBOpt $(\vartheta=1 \cdot 10^{-5})$** | **** | **** | **** | **** | **** | 
| IVON@mean |  |  |  |  |  |
| SGD |  |  |  |  |  | 
| Laplace |  |  |  |  |  | 

## Train Fraction = 5% (1000 training samples)

| **Optimizer** | **Top-1 Acc.** $\uparrow$ | **Top-5 Acc.** $\uparrow$ | **NLL** $\downarrow$ | **ECE** $\downarrow$ | **Brier** $\downarrow$ |
|---|---:|---:|---:|---:|---:|
| **uCBOpt $(\vartheta\to0^{+})$** | **60.07 (1.47)** | **94.73 (0.46)** | **1.806 (0.245)** | **0.245 (0.025)** | **0.623 (0.036)** |
| **uCBOpt $(\vartheta=5 \cdot 10^{-6})$** | **61.51 (1.27)** | **94.88 (0.23)** | **1.742 (0.108)** | **0.238 (0.012)** | **0.604 (0.019)** | 
| IVON@mean | 59.66 (1.79) | 94.51 (0.50) | 1.832 (0.102) | 0.251 (0.012) | 0.630 (0.026) |
| SGD | 60.81 (3.33) | 94.90 (0.98) | 1.764 (0.296) | 0.242 (0.030) | 0.613 (0.061) | 
| AdamW | 54.88 (1.29) | 92.92 (0.45) | 3.246 (0.138) | 0.353 (0.012) | 0.775 (0.022) |
