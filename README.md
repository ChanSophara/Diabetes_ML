# 🧠 Diabetes Prediction using MLP Neural Network

> A machine learning project for predicting the likelihood of diabetes using the **Diabetes_012** dataset and Multi-Layer Perceptron (MLP) classifiers.

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Scikit-learn](https://img.shields.io/badge/ML-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📌 Project Overview

This project uses supervised learning to predict diabetes (binary classification) from health-related attributes. It experiments with different MLP architectures and evaluates them on training, validation, and test sets.

---

## 🧬 Dataset

- **Source**: `diabetes_012.csv`
- **Target variable**: `Diabetes_binary` (0 = no diabetes, 1 = diabetes)
- **Features**: Various health indicators (BMI, blood pressure, physical activity, etc.)
- **Missing values**: None (checked via `.isnull().sum()`)

---

## ⚙️ Workflow

1. 📥 Load and preprocess the data  
2. 🔀 Split into train, validation, and test sets (60/20/20)  
3. 🧠 Train multiple MLPClassifier models:
   - Model 1: `(100,)`
   - Model 2: `(100, 300)`
   - Model 3: `(100, 300, 500)`
4. 📈 Evaluate models on:
   - Training set
   - Validation set
   - Test set

---

## 🧪 Model Evaluation

| Model Architecture     | Validation Error | Test Accuracy |
|------------------------|------------------|---------------|
| (100)                 | ~0.215           | ~0.78         |
| (100, 300)            | ~0.208           | ~0.79         |
| (100, 300, 500)       | ~0.204           | ~0.79         |

> ⚠️ Results may vary slightly depending on random state or feature normalization.

---

## 📊 Key Learnings

- Adding more hidden layers improves validation performance slightly.
- Model complexity should be balanced with training time and generalization.
- Splitting data into train/val/test ensures robust evaluation.

## 🚀 How to Run

1. Clone the repository:
```bash
git clone https://github.com/yourusername/diabetes-ml-classifier.git

2.Install required libraries:
pip install pandas numpy scikit-learn

3.Run the notebook:
jupyter notebook diabetes_ML.ipynb
