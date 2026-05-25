# Home Network Intrusion Detection using Machine Learning

## Project Overview

This project was conducted as a machine learning term project for the 2026-1 semester.

The goal of this project is to build a binary classification model that can detect malicious network traffic in home network environments. The model classifies network traffic into two categories:

* Normal Traffic
* Attack Traffic

This project focuses not only on overall accuracy but also on reducing False Negatives (FN), since misclassifying attacks as normal traffic can lead to serious security risks in real-world environments.

---

## Dataset

This project uses the **CICIDS2017: Cleaned & Preprocessed** dataset.

* Original Dataset: CICIDS2017
* Source: Kaggle
* Dataset Type: Network Traffic Intrusion Detection
* Task: Binary Classification (Normal Traffic vs Attack Traffic)

The dataset file is not included in this repository due to file size limitations.

Please place the dataset file at:

```text
datasets/cicids2017_cleaned.csv
```

---

## Models

### Baseline Model

* K-Nearest Neighbors (KNN)

### Main Model

* Random Forest

---

## Evaluation Metrics

The following evaluation metrics were used:

* Accuracy
* Precision
* Recall
* F1-score
* False Positive (FP)
* False Negative (FN)
* False Positive Rate (FPR)

---

## Environment

* Python 3.10
* Jupyter Notebook
* Pandas
* NumPy
* Scikit-learn
* Matplotlib

---

## Project Structure

```text
project/
│
├── datasets/         # Dataset directory
├── notebooks/        # Jupyter notebooks for experiments
├── docs/             # Final report and presentation slides
├── .gitignore
├── README.md
└── requirements.txt
```

---

## Installation

Install required packages:

```bash
pip install -r requirements.txt
```

---

## How to Run

Run the notebooks in the following order:

```text
00_eda.ipynb
01_knn_baseline.ipynb
02_random_forest_model.ipynb
03_random_forest_full_model.ipynb
```

### Notebook Description

| Notebook                          | Description                                                        |
| --------------------------------- | ------------------------------------------------------------------ |
| 00_eda.ipynb                      | Dataset loading, preprocessing, and sample dataset generation      |
| 01_knn_baseline.ipynb             | Baseline KNN model training and evaluation                         |
| 02_random_forest_model.ipynb      | Random Forest hyperparameter tuning and sample dataset experiments |
| 03_random_forest_full_model.ipynb | Final Random Forest training on the full dataset                   |

---

## Final Results

The Random Forest model achieved significantly better performance than the KNN baseline model across all evaluation metrics.

In particular, the Random Forest model greatly reduced False Negatives (FN), which is especially important in intrusion detection tasks because undetected attacks can lead to serious security threats.

The project also analyzed feature importance to identify which network traffic features contributed most to attack detection.

---

## Report

The final report and presentation slides are available in the `docs/` directory.
