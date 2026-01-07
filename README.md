
# Code & data for multimetallic PBAs catalysts

This repository contains the **code and data** used to develop and evaluate the related paper “Hyperspace mapping and iterative dimensionality reduction reveal radical cascade networks controlled by perovskite-type catalysts”.

---

## 📂 Repository Contents

### 📁 Code

- `XGB_metal_selection.ipynb`  
  ➤ Metal selection via feature importance analysis using XGBoost regression model.

- `Clustering_spectra_with_PCA.ipynb`  
  ➤ Clustering compounds with similar UV spectra by PCA.

- `UV_unmixing.ipynb`  
  ➤ A simple version working example of spectral unmixing.  
  ➤ A more detailed implementation is available in [robowski-maps (GitHub)](https://github.com/yaroslavsobolev/robowski-maps), under `robowski/uv_vis_absorption_spectroscopy`.

---

### 📁 Data

#### 📦 `data/UV_spectra/`
Contains UV-Vis spectra files for:
- **Solvent background**
- **Sample crude mixtures**
- **Reference basis sets**

##### 📄 Basis Set Files:
- **Model_1** (6 references):  
  `Basis_set_6refs_0.5mM.csv`

- **Model_2** (11 references):  
  `Basis_set_11refs_0.5mM.csv`

- **Model_3** (PCA-clustered, 11 references):  
  `Basis_set_11refs_with_PCA_0.5mM.csv`

##### 📄 Sample Spectra:
- **Round 1 screening (11 B site metals, Model 1)**:  
  `Sample_crude_spectra_11metals.csv`

- **Round 2 screening (6 B site metals, Models 2 & 3)**:  
  `Sample_crude_spectra_6metals.csv`

---

#### 📦 `data/UV_unmixing_result/`  
Contains spectral unmixing results that serve as inputs for XGBoost model training.

#### 📦 `data/XGB_dataset/`  
Prepared datasets used for training and 5-fold cross-validation of the XGB models.
