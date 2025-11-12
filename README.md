# 🧬 Predicting Cancer Drug Response from Gene Expression using Machine Learning

> "What if we could predict how a cancer cell would respond to a drug—before giving it?"  
> This project explores that question by combining **transcriptomics** and **machine learning** to model drug sensitivity in cancer.

---

## 🎯 Objective

The goal of this project is to predict **drug response (IC50/AUC)** from **gene expression profiles** of cancer cell lines.  
By learning molecular patterns that underlie sensitivity or resistance, the pipeline demonstrates how computational biology can power **precision oncology** — guiding treatment selection with data-driven insight.

---

## 🧠 Approach

### 1️⃣ Data Simulation (Prototype Stage)
To build the proof of concept, a **synthetic dataset** was created mimicking real transcriptomic data:
- 300 cancer cell lines × 1,000 genes  
- Response variable (IC50) representing drug sensitivity for a demo compound ("DemoDrug")

### 2️⃣ Feature Engineering
- Variance-based gene filtering (retain top 90% most variable genes)
- Normalization and alignment of sample IDs

### 3️⃣ Modeling
- Algorithms: **Random Forest** and **XGBoost**  
- Metrics: **R²**, **RMSE**, **Spearman correlation**  
- Interpretability: **Feature importance** and **SHAP (SHapley Additive Explanations)**

---

## ⚙️ Implementation

Built in **Python 3.10** using an **Anaconda** environment.

### Environment Setup
```bash
conda create -n drugresp python=3.10 -y
conda activate drugresp
pip install pandas numpy scikit-learn scipy matplotlib seaborn xgboost shap gseapy pyreadr pyarrow
