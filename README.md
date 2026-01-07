
# 🧪 Metal Species Screening for PBA Catalyst Using XGBoost

This repository contains the **code and data** used to develop and evaluate **XGBoost regression models** for screening metal species in Prussian Blue Analogue (PBA) catalysts, leveraging **UV-Vis spectral data**, **feature selection**, and **clustering**.

---

## 📂 Repository Contents

### 📁 Code

- `XGB_metal_selection.ipynb`  
  ➤ Implements metal selection using XGBoost regression with spectral input features.

- `Clustering_spectra_with_PCA.ipynb`  
  ➤ Applies PCA to cluster reference spectra of similar chemical profiles.

- `UV_unmixing.ipynb`  
  ➤ Demonstrates spectral unmixing (simple version).  
  ➤ A more detailed implementation is available in [robowski-maps (GitHub)](https://github.com/yaroslavsobolev/robowski-maps), under `robowski/uv_vis_absorption_spectroscopy`.

---

### 📁 Data

#### 📦 `data/UV_spectra/`
Contains UV-Vis spectra for:
- **Solvent background**
- **Sample crude mixtures**
- **Reference basis sets**

##### 📄 Basis Set Files:
- **Model 1** (6 references):  
  `Basis_set_6refs_0.5mM.csv`

- **Model 2** (11 references):  
  `Basis_set_11refs_0.5mM.csv`

- **Model 3** (PCA-clustered, 11 references):  
  `Basis_set_11refs_with_PCA_0.5mM.csv`

##### 📄 Sample Spectra:
- **Round 1 screening (11 metals, Model 1)**:  
  `Sample_crude_spectra_11metals.csv`

- **Round 2 screening (6 metals, Models 2 & 3)**:  
  `Sample_crude_spectra_6metals.csv`

---

#### 📦 `data/UV_unmixing_result/`  
Contains spectral unmixing results that serve as inputs for XGBoost model training.

#### 📦 `data/XGB_dataset/`  
Prepared datasets used for training and 5-fold cross-validation of the XGB models.