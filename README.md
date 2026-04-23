# 🚢 Titanic Survival Prediction — Logistic Regression from Scratch

## 📌 Overview

This project implements **Logistic Regression from scratch using NumPy**, without relying on machine learning libraries.

The goal is to deeply understand:

* Optimization using gradient descent
* Feature engineering and preprocessing
* Model evaluation and validation
* Real-world ML pipeline design

The model is trained on the **Titanic dataset from Kaggle**.

---

## ⚙️ Features

* Full ML pipeline (EDA → preprocessing → training → evaluation)
* Logistic Regression implemented from scratch (NumPy)
* Mini-batch gradient descent
* L2 regularization
* Numerical stability (clipped sigmoid)
* Feature scaling
* Evaluation metrics:

  * Accuracy, Precision, Recall, F1 Score
  * ROC-AUC (implemented from scratch)
* ROC Curve visualization
* Feature importance interpretation
* Comparison with sklearn (validation)

---

## 📂 Project Structure

```
project/
│
├── notebook.ipynb       # Complete Colab notebook
├── data/                # (optional) dataset
├── outputs/             # saved weights (optional)
└── README.md
```

---

## 🚀 How to Run

### Option 1: Google Colab (Recommended)

1. Open the notebook in Colab
2. Add your Kaggle API key
3. Run all cells

### Option 2: Local

```bash
pip install numpy pandas matplotlib scikit-learn
python train.py
```

---

## 📊 Results

| Metric    | From Scratch | sklearn |
| --------- | ------------ | ------- |
| Accuracy  | 0.79         | 0.79    |
| Precision | 0.68         | 0.68    |
| Recall    | 0.74         | 0.74    |
| F1 Score  | 0.71         | 0.71    |
| ROC-AUC   | 0.87         | 0.88    |

✅ Results closely match sklearn, validating correctness of implementation.

---

## 🧠 Feature Importance

| Feature | Weight | Insight                                      |
| ------- | ------ | -------------------------------------------- |
| Sex     | +1.33  | Strongest predictor (female survival higher) |
| Pclass  | -0.98  | Lower class → lower survival                 |
| Age     | -0.57  | Older passengers less likely to survive      |
| SibSp   | -0.41  | Larger family size reduces survival          |
| Fare    | +0.16  | Wealth proxy improves survival               |
| Others  | Small  | Minimal impact                               |

---

## 🔍 Key Insights

* Gender was the most important factor
* Socioeconomic status strongly influenced survival
* Younger passengers had higher survival rates
* Model aligns with known historical patterns

---

## ⚠️ Notes

* Feature importance is based on **log-odds**, not probabilities
* Correlated features may share importance
* Linear model → limited interaction modeling

---

## 🧠 What I Learned

* How gradient descent works in practice
* Importance of feature scaling for optimization
* Handling real-world messy data
* Validating models against industry standards

---

## 🔮 Future Improvements

* Class imbalance handling
* Feature interaction modeling
* Hyperparameter tuning
* Deployment as an API

---

## 👨‍💻 Author

Fayaz Hussain Syed
