# Polymer Properties Prediction

This repository contains a Kaggle notebook and related resources for the **Polymer Properties Prediction** competition. The notebook predicts target properties using models pre-trained with RDKit features.

## Dataset Locations
The notebook expects datasets from Kaggle:

- `/kaggle/input/precomp/test_with_rdkit_features.csv` – test features.
- `/kaggle/input/precomputed-rdkit-features/train_with_rdkit_features.csv` – training features and target values.
- `/kaggle/input/precomputed-rdkit-features/model_<target>.pkl` – pre-trained models for each target (`Tg`, `FFV`, `Tc`, `Density`, `Rg`).

## Environment
- **Python**: 3.11
- **Required packages**: `pandas`, `numpy`, `joblib`, `rdkit`

These dependencies are provided in Kaggle's standard Python image. If running locally, ensure the above packages are installed.

## Running the Notebook on Kaggle
1. Upload `neurips.ipynb` to Kaggle or open it directly from the repository.
2. Add the datasets `precomp` and `precomputed-rdkit-features` to the notebook from the *Add Data* menu.
3. Run all cells. This loads the test features, aligns columns with the training data, applies the pre-trained models and saves `submission.csv`.
4. Download `submission.csv` from the Kaggle output section and submit it to the competition.

## Competition Description
The goal of the competition is to predict glass transition temperature (`Tg`), free volume fraction (`FFV`), critical temperature (`Tc`), density (`Density`), and radius of gyration (`Rg`) for polymer molecules. Predictions are evaluated using mean squared error across these targets.
