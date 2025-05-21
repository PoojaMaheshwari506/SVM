# SVM Parameter Optimization 
This project demonstrates the process of optimizing Support Vector Machine (SVM) hyperparameters for multi-class classification using a subset of the UCI Letter Recognition dataset. The workflow includes repeated train-test splits, random hyperparameter search, result logging, and convergence visualization.

---

## 📚 Dataset

- **Source:** [UCI Letter Recognition Dataset](https://archive.ics.uci.edu/ml/datasets/letter+recognition)
- **Classes:** 26 (A–Z, uppercase letters)
- **Features:** 16 numerical attributes per sample
- **Sample Size Used:** 5,000 randomly selected rows for computational efficiency

---

## 🚦 Workflow Overview

1. **Data Preparation**
    - Download and load the dataset from the UCI repository.
    - Encode the target variable (letters) as integers (A=0, ..., Z=25).
    - Randomly sample 5,000 rows for the experiment.
    - Display basic statistics and class distribution.

2. **SVM Hyperparameter Optimization**
    - For each of 5 random 70-30 train-test splits:
        - Randomly sample SVM hyperparameters (`kernel`, `C`, `gamma`) for 50 iterations.
        - Train and evaluate an SVM classifier on each configuration.
        - Track the best accuracy and corresponding parameters for each split.
        - Record accuracy progression for convergence analysis.

3. **Result Analysis & Visualization**
    - Save the best results for each split in a CSV file (`svm_results.csv`).
    - Plot and save the convergence graph (accuracy vs. iteration) for the best-performing split (`convergence_plot.png`).

---

## ▶️ How to Run

1. **Install Dependencies**
    ```bash
    pip install numpy pandas scikit-learn matplotlib seaborn
    ```

2. **Run the Script**
    ```bash
    python svm_optimization.py
    ```

3. **Check Outputs**
    - `svm_results.csv`: Table of best accuracy and SVM parameters for each split
    - `convergence_plot.png`: Accuracy progression plot for the best split

---
