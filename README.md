# 🧬 Molecular Subtype Classification of Prostate Cancer Using High-Dimensional RNA Sequencing

This repository presents a machine learning framework designed to distinguish prostate cancer samples from non-cancerous tissue using **20,530-gene RNA sequencing data**.  
Unlike traditional binary diagnostic models, this project emphasizes:

- **Sensitivity to rare non-cancer tissue samples**  
- **Transcriptomic subtype characterization**  
- **Detection of subtle prostate-specific gene expression shifts**

The goal is not just prediction, but understanding **molecular instability patterns** characteristic of prostate cancer.

---

## 📌 Dataset Overview

- **Total genes:** 20,530  
- **Sample types:**  
  - `0.0` → Non-cancer tissue  
  - `1.0` → Cancer tissue  
- **Challenge:** High dimensionality × strong class imbalance  
- **Objective:** Learn prostate-specific transcriptional disruptions with reliable generalization.

---

## 🔍 Novelty of This Project

### ⭐ 1. Focus on Rare-Class Sensitivity  
Prostate datasets frequently contain **very limited normal tissue samples**.  
This model handles that challenge through:

- Careful feature selection  
- Class imbalance–aware validation  
- Emphasis on **robust minority class recall**

### 🧬 2. Subtype-Oriented Interpretation  
Instead of broad cancer detection, this project highlights **prostate-specific regulatory shifts** by examining genes strongly tied to prostate cell differentiation and chromosomal instability.

### 🧠 3. Transcriptomic Instability Analysis  
Top-ranked genes (e.g., **APOBEC3C**, **C1orf190**, **TUBB3**) suggest distinct genomic alteration patterns, providing insights useful for prostate cancer subtype research.

---

## ⚙️ Methodology Overview

1. **Data Preprocessing**  
   - Expression normalization  
   - Handling high-dimensional RNA-seq features

2. **Feature Selection**  
   - Mutual Information for identifying prostate-relevant genes  

3. **Classification**  
   - XGBoost model optimized for imbalanced gene expression data  

4. **Evaluation**  
   - Classification metrics  
   - Cross-validation  
   - Explainable gene-level insights  

---

## 📈 Model Performance

### **Classification Report**

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0.0 (Non-Cancer) | 0.93 | 0.88 | 0.90 | 16 |
| 1.0 (Cancer)     | 0.99 | 0.99 | 0.99 | 149 |

- **Accuracy:** 0.98  
- **Macro F1 Score:** 0.95  
- **Weighted F1 Score:** 0.98  

> Strong performance despite highly imbalanced data, demonstrating robustness.

---

## 🔁 Cross-Validation Performance (5-Fold)

| Fold | Accuracy |
|------|----------|
| 1 | 0.9351 |
| 2 | 0.9221 |
| 3 | 0.9351 |
| 4 | 0.9740 |
| 5 | 0.9740 |

**Average Accuracy:** 0.9481  

This stability across folds indicates that the model learns **consistent prostate-specific patterns**.

---

## 🧬 Top Molecular Markers Identified (Feature Importance)

| Rank | Gene | Importance |
|------|-------|------------|
| 1 | **APOBEC3C** | 0.14885 |
| 2 | **C1orf190** | 0.11584 |
| 3 | TUBB3 | 0.04180 |
| 4 | PLA2G7 | 0.03374 |
| 5 | PAX1 | 0.03114 |
| 6 | PLP2 | 0.02737 |
| 7 | POM121 | 0.02494 |
| 8 | B3GNT6 | 0.02432 |
| 9 | KCNH8 | 0.02392 |
| 10 | LOC644936 | 0.02267 |
| 11 | TOR1AIP1 | 0.02179 |
| 12 | RPGRIP1 | 0.02127 |
| 13 | DLX2 | 0.01781 |
| 14 | PGM5P2 | 0.01689 |
| 15 | C17orf96 | 0.01657 |
| 16 | PDDC1 | 0.01367 |
| 17 | DPY19L4 | 0.01217 |
| 18 | CENPQ | 0.01111 |
| 19 | TCEAL1 | 0.01104 |
| 20 | MAT2B | 0.01026 |

### 🧠 Biological Interpretation
- **APOBEC3C** and **C1orf190** dominate importance → strong indicators of genomic instability.  
- Several genes (e.g., **PLA2G7**, **PAX1**) are linked to prostate tumor progression pathways.  
- Highlights transcriptomic shifts consistent with aggressive prostate cancer phenotypes.

---

## 🧠 Key Takeaways

- Handles **extreme dimensionality and class imbalance** effectively.  
- Achieves **98% accuracy** with strong minority-class performance.  
- Reveals prostate-specific genomic alterations through explainability.  
- Demonstrates model reliability using cross-validation.

---

## 🛠 Tools Used

- Python  
- XGBoost  
- Scikit-Learn  
- NumPy & Pandas  
- Matplotlib (optional for visualization)

---

## 🤝 Contribution

This repository serves as a reproducible demonstration of molecular subtype analysis using RNA-seq and explainable ML.  
For questions, collaborations, or suggestions — feel free to open an issue.
