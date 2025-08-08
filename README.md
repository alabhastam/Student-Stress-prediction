# 🧠 Student Stress Monitoring – Machine Learning Project

## 📌 Project Overview
This project applies **machine learning** to predict students' stress levels  
using behavioral, lifestyle, and academic-related features from the  
[Student Stress Monitoring Dataset](https://www.kaggle.com/) on Kaggle.

We explore the dataset, preprocess features, build and evaluate baseline models,  
and compare model performances using **Accuracy**, **F1-scores**, **Execution Time**,  
and **Confusion Matrices**.

---

## 📂 Dataset
- **Source**: Kaggle – *Student Stress Monitoring* you can find dataset in my notebook in *kaggle*
- **Target**: `stress_level` (0 = Low, 1 = Medium, 2 = High)
- **Number of Features**: Mixed numerical & categorical (e.g., sleep duration, diet, study time)
- **Number of Samples**: N (depending on dataset size)

---

## 📊 Exploratory Data Analysis
- Mapped target labels:  
```python
{0: "Low", 1: "Medium", 2: "High"}
```
- Checked target distribution for class balance.
- Plotted correlation heatmap to identify most influential features.

---

## ⚙️ Data Preprocessing
1. **Feature / Target Split** (`X`, `y`)
2. **Scaling** with `StandardScaler` for numeric columns
3. **Train-Test Split** (80% / 20%) with `stratify` on target

---

## 🤖 Model Training
We trained **10 baseline models**:

| Model                 |
|-----------------------|
| Logistic Regression   |
| Random Forest         |
| Decision Tree         |
| KNN                   |
| Linear SVM            |
| RBF SVM               |
| Gradient Boosting     |
| XGBoost               |
| LightGBM              |
| CatBoost              |

---

## 📈 Leaderboard (Test Set Performance)
| Rank | Model               | Accuracy | F1_macro | F1_weighted | Exec Time (sec) |
|------|---------------------|----------|----------|-------------|-----------------|
| 1    | Random Forest       | 0.8909   | 0.8909   | 0.8907      | 0.0103          |
| 2    | Linear SVM          | 0.8864   | 0.8862   | 0.8861      | 0.0002          |
| 3    | Logistic Regression | 0.8818   | 0.8820   | 0.8817      | 0.00015         |
| ...  | ...                 | ...      | ...      | ...         | ...             |

> **Note:** Execution time measured for prediction stage only.

---

## 📊 Confusion Matrices (Top 3 Models)
Confusion matrices are visualized for the top 3 models with human-readable class labels (*Low*, *Medium*, *High*).



## 🛠 Requirements
- Python 3.8+
- pandas, numpy
- scikit-learn
- seaborn, matplotlib
- xgboost, lightgbm, catboost



---

## 📌 Next Steps
- Hyperparameter tuning of top models
- Try ensemble/voting classifier
- Deploy the best model with Flask/FastAPI

---

## 📜 License
This project is open-source under the [MIT License](LICENSE).
