BACE1 QSAR Modeling Using RDKit and Machine Learning

A machine learning-based QSAR(Quantitative Structure–Activity Relationship) model developed to predict the inhibitory activity (pIC50) of BACE1 inhibitors using molecular descriptors calculated with RDKit.

Overview:

Beta-secretase 1 (BACE1) is an important therapeutic target in Alzheimer's disease because it initiates the cleavage of amyloid precursor protein, leading to the formation of β-amyloid peptides. Computational approaches such as QSAR can be used to relate molecular properties to biological activity and assist in early-stage drug discovery.
This project implements a basic QSAR workflow using publicly available BACE1 bioactivity data from ChEMBL.

Datasets used:

1. ChEMBL Database
2. Target : BACE1
3. Bioactivity: IC50
4. Response variable: pIC50

QSAR Pipeline:

ChEMBL Database
        │
        ▼
Download BACE1 Bioactivity Data
        │
        ▼
Filter IC50 Measurements
        │
        ▼
Remove Duplicate Compounds
        │
        ▼
Convert SMILES → Molecular Structures
        │
        ▼
Calculate Molecular Descriptors
(MolWt, LogP, TPSA, HBD, HBA, RotBonds)
        │
        ▼
Generate pIC50 Values
        │
        ▼
Train-Test Split
        │
        ▼
Random Forest Regression
        │
        ▼
Model Evaluation
(R², MAE, RMSE)

Model performance:

| Metric   | Value     |
| -------- | --------- |
| R² Score | 0.429 |
| MAE      | 0.734 |
| RMSE     | 0.941 |


Planned enhancements include:

1. RDKit descriptor set (~200 descriptors)
2. Morgan (ECFP4) fingerprints
3. Feature selection
4. Hyperparameter optimization
5. Cross-validation
6. External validation
7. Model comparison (Random Forest, XGBoost, SVR)
8. Applicability domain analysis
9. Virtual screening of novel compoun
