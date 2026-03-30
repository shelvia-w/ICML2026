## Computational Efficiency

We measure the average runtime for one training epoch and the peak GPU memory usage of ResNet-20 trained on CIFAR-10:

| **Optimizer** | uCBOpt | IVON | SGD | AdamW | DUQ | SNGP |
|---|---:|---:|---:|---:|---:|---:|
| **Time (sec)** | 18.9  | 18.5 | 17.2 | 17.6 | 50.5 | 21.5 | 
| **Memory (GiB)** | 0.28 | 0.28 | 0.27 | 0.28 | 0.60 | 0.81 | 

