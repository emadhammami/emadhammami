# Hi, I'm Emad Hammami 👋

I research and build **federated learning systems** with a focus on communication-efficient gradient compression for time-series forecasting.  
All experiments run on real-world electricity consumption data using classical deep learning — no cloud, no LLMs, just clean and reproducible science.

---

## Research: Compressed Federated Learning for Time-Series Forecasting

A series of four open-source experiments exploring how federated clients can collaboratively train LSTM models while minimizing uplink bandwidth through gradient compression.

| # | Repository | Key Idea | Input | Seq Len | Test MAE |
|---|---|---|---|---|---|
| 1 | [Compressed-Federated-Time-Series-Forecasting](https://github.com/emadhammami/Compressed-Federated-Time-Series-Forecasting) | Baseline — fixed sparsity `DeltaCompressor` | Tabular features (`feat_static_cat`, `hour`, `dayofweek`, `month`) | 10 | 639 |
| 2 | [Compressed-FL-Univariate-LSTM-Forecasting](https://github.com/emadhammami/Compressed-FL-Univariate-LSTM-Forecasting) | Pure univariate signal, longer window | Raw load values only | 24 | 1159 |
| 3 | [Fed-Multivariate-LSTM-DeltaComp](https://github.com/emadhammami/Fed-Multivariate-LSTM-DeltaComp) | Load history + calendar features together | `target` + `hour` + `dayofweek` + `month` | 24 | 1151 |
| 4 | [fed-lstm-budgeted-compression](https://github.com/emadhammami/fed-lstm-budgeted-compression) | Per-client KB budget via binary search threshold | Tabular features | 10 | 644 |

### What is DeltaCompressor?

Every experiment shares a custom compressor that:
1. Computes the **weight delta** (local weights − global weights) after each local training round
2. Sparsifies it using **MAD + top-k thresholding** (or binary search for a KB budget)
3. Sign-encodes survivors and **gzip-compresses** the payload
4. Accumulates residuals to prevent information loss across rounds

This achieves ~0.3–0.5 KB per client per round on a model with ~20K parameters.

### Shared Setup

- **Dataset:** [tulipa762/electricity\_load\_diagrams](https://huggingface.co/datasets/tulipa762/electricity_load_diagrams) via Hugging Face
- **Model:** LSTM (64 units) → Dense (32, ReLU) → Dense (1, linear)
- **Optimizer:** SGD with momentum 0.9, lr 0.01
- **Federation:** 3 clients, FedAvg aggregation, 100 rounds
- **Framework:** TensorFlow 2.18 / NumPy 1.26 / scikit-learn

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)

---

> All experiments are fully reproducible. Clone any repo, `pip install -r requirements.txt`, and run.
