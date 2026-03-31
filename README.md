# Mohammad Emad Hammami

**Software Engineer · AI Researcher · Scrum Master**  
Oslo, Norway · [emadhammami.site](https://emadhammami.site) · [LinkedIn](https://www.linkedin.com/in/emadhammami) · [ResearchGate](https://www.researchgate.net/profile/Mohammad-Emad-Hammami)

Software engineer and AI researcher specialising in **federated learning**, **distributed systems**, and **applied machine learning**, with peer-reviewed publications and hands-on experience across software engineering, Agile delivery, and digital transformation.

---

## Academic Publications

| Year | Title | Venue |
|---|---|---|
| 2026 | uAMBIT: Byte-Budgeted Update Compression with Error-Feedback for Federated Learning *(accepted)* | IEEE DCOSS-IoT 2026 |
| 2024 | [AMBIT: Efficient Pruning Technique for Edge Computing](https://ieeexplore.ieee.org/document/10707219) | IEEE Int. Conf. on Fog and Edge Computing (ICFEC) |
| 2023 | [Adaptive Mean Absolute Deviation Pruning in Federated Learning](https://www.duo.uio.no/bitstream/handle/10852/108659/Master_thesis-20-11-.pdf?sequence=11) | Master's Thesis, University of Oslo |

---

## Research Projects

### Federated Learning & Gradient Compression

A series of reproducible experiments on communication-efficient federated learning for time-series forecasting, all using a custom `DeltaCompressor` (MAD + top-k sparsification, sign encoding, gzip) to minimise uplink traffic.

| Repository | Key Idea | Input | Seq | Test MAE |
|---|---|---|---|---|
| [Compressed-Federated-Time-Series-Forecasting](https://github.com/emadhammami/Compressed-Federated-Time-Series-Forecasting) | Baseline fixed-sparsity compression | Tabular features | 10 | 639 |
| [Compressed-FL-Univariate-LSTM-Forecasting](https://github.com/emadhammami/Compressed-FL-Univariate-LSTM-Forecasting) | Pure univariate signal, longer window | Raw load values | 24 | 1159 |
| [Fed-Multivariate-LSTM-DeltaComp](https://github.com/emadhammami/Fed-Multivariate-LSTM-DeltaComp) | Load history + calendar features | Target + calendar | 24 | 1151 |
| [fed-lstm-budgeted-compression](https://github.com/emadhammami/fed-lstm-budgeted-compression) | Per-client KB budget via binary search | Tabular features | 10 | 644 |

All experiments: 3 clients · FedAvg · 100 rounds · TensorFlow 2.18 · ~0.3–0.5 KB/client/round

### uAMBIT: Byte-Budgeted Update Compression with Error-Feedback for Federated Learning

**Accepted — IEEE DCOSS-IoT 2026** · [GitHub](https://github.com/emadhammami/uambit-hard-cap-fl) · [Run on Colab](https://colab.research.google.com/github/emadhammami/uambit-hard-cap-fl/blob/main/notebooks/uambit_budget_cap.ipynb)

Enforces a strict **0.5 KiB/client/round** uplink hard cap with competitive accuracy vs. Top-k, STC, QSGD, and EF-Sign baselines. Benchmarked on BreastMNIST with threshold-based sparse compression, scale sharing, and error-feedback. Includes both a single-notebook experiment and a modular `src/` package.

---

## Other Projects

**DNB Digital Transformation Research** · University of Oslo  
In-depth research on DNB Bank's digital transformation, focusing on emerging technologies and organisational restructuring.

**Software Process Improvement Plan** · DNB Bank  
Comprehensive SPI plan emphasising Agile methodologies and process optimisation.

**Handbook of Scrum Methodology** · DNB Bank  
Authored a practical Scrum handbook outlining best practices for engineering teams.

---

## Experience

**Software Engineer / Scrum Master** · DNB Bank, Oslo *(2021 – present)*  
Agile transformation, sprint facilitation, QA with Octane, incident management in ServiceNow.

**Scrum Master** · Telia, Oslo *(2020 – 2021)*  
Agile team facilitation, backlog management, development contributions with Laravel & Onfido.

---

## Education

| Degree | Institution | Year |
|---|---|---|
| MSc Digitalization & Management *(ongoing)* | University of South-Eastern Norway | 2024 – present |
| MSc Informatics: Programming & Systems Architecture | University of Oslo | 2023 |
| BEng Software Engineering | OsloMet | 2026 |
| BSc Informatics: Programming & Systems Architecture | University of Oslo | 2025 |
| BSc Information Technology | OsloMet | 2021 |

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)
![Azure](https://img.shields.io/badge/Microsoft_Azure-0078D4?style=flat&logo=microsoftazure&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Jira](https://img.shields.io/badge/Jira-0052CC?style=flat&logo=jira&logoColor=white)

**Languages:** English · Norwegian · Arabic
