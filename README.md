# Medical-Cost-Prediction
This project explores a machine learning pipeline to predict individual medical insurance costs using demographic and lifestyle features. The work spans from basic regression to advanced modeling with XGBoost, Optuna hyperparameter tuning, SHAP explainability, and model ensembling.

---

## 📊 Dataset

- **Name**: Medical Cost Personal Dataset
- **Source**: [Kaggle](https://www.kaggle.com/datasets/mirichoi0218/insurance)
- **Target**: `charges` (predicted insurance cost)
- **Features**: 
  - Numerical: `age`, `bmi`, `children`
  - Categorical: `sex`, `smoker`, `region`

---

## 🧠 Project Goals

- Predict medical costs accurately using regression techniques
- Interpret the contribution of features using SHAP
- Improve accuracy via hyperparameter tuning and feature engineering
- Explore ensemble models for further performance gains

---

## ✅ Techniques Used

- Linear Regression as baseline
- **XGBoost** with **Optuna** tuning
- Feature Engineering:
  - Interaction terms (e.g., `bmi * age`)
  - Log transformation of `bmi`
- **SHAP** (SHapley Additive exPlanations) for feature importance
- Ensemble Model: XGBoost + RandomForest + Ridge

---

## 📈 Results

| Model                | R² Score |
|---------------------|----------|
| Linear Regression    | ~0.78    |
| Tuned XGBoost        | ~0.88    |
| Ensemble Regressor   | ✅ **0.882** |

- **Top Features (SHAP)**: `smoker`, `bmi × age`, `age`, `bmi`

---

## 🔬 SHAP Takeaways

- **Smoker** status drastically increases predicted costs
- Interaction between `age` and `bmi` improves explanatory power
- Model remains explainable and practical for real-world application

---

## 📂 Project Structure

medical-cost-prediction/
├── insurance.csv
├── medical_cost_modeling.ipynb
├── README.md
└── requirements.txt

---

## 🛠️ Technologies

- Python (Colab)
- Scikit-learn
- XGBoost
- SHAP
- Optuna
- Matplotlib / Seaborn

---

## 📌 License

This project is open-source and free to use under the [MIT License](LICENSE).
