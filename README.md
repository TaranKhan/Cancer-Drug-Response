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

## 📊 Results Summary

**Random Forest Model**

- **R² (Coefficient of Determination):** 0.54  
- **RMSE (Root Mean Squared Error):** 0.12  
- **Spearman Correlation:** 0.80  

**Top Predictive Genes**
- GENE 5  
- GENE 77  
- GENE 301  

These were the same genes intentionally embedded in the synthetic dataset, confirming that the model identified the correct biological signal.

---

## 🎨 Visual Insights

**Predicted vs Actual Plot:**  
Shows a clear linear trend between predicted and actual IC50 values, validating the model fit.  

**Feature Importance Plot:**  
Highlights the most influential genes driving drug response prediction.  

**SHAP Summary Plot:**  
Explains each gene’s contribution to sensitivity or resistance. 
All figures are automatically saved in:  
`results/figures/`

---

## 💡 Biological Impact

Predicting cancer drug response before treatment is vital for **precision oncology**.  
This workflow demonstrates how integrating machine learning with gene expression can:

- Identify **biomarkers of drug sensitivity**  
- Reveal **molecular mechanisms of resistance**  
- Support **personalized therapy design**

While this prototype uses synthetic data, it can be directly applied to real-world datasets such as **GDSC** and **CCLE**.

---

## 🚀 Next Steps

- Integrate **real GDSC expression + IC50 data** (e.g., Trametinib, Cisplatin)  
- Extend to **multi-drug and multi-omics** models  
- Add pathway features using **GSEA/ssGSEA**  
- Deploy an **interactive Streamlit app** for visualization  

---

## 👩‍💻 Author

**Taran Khan**  
Bioinformatics & Data Science | Transcriptomics | Machine Learning for Precision Medicine  
📫 [LinkedIn](https://www.linkedin.com/in/taran-khan-bioinformatics)  
📂 [GitHub](https://github.com/TaranKhan)

---

## 🌟 Vision

> “The future of medicine is predictive.  
> The future of prediction is data.”


### Environment Setup
```bash
conda create -n drugresp python=3.10 -y
conda activate drugresp
pip install pandas numpy scikit-learn scipy matplotlib seaborn xgboost shap gseapy pyreadr pyarrow

---

