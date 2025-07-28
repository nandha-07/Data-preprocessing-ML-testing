# 🧪 Diabetes Dataset Preprocessing (UCI Pima Indians)

This project focuses on applying essential data preprocessing steps to the **Pima Indians Diabetes dataset** from the UCI Machine Learning Repository.  
The goal is to clean, transform, and prepare the dataset for further modeling and analysis.

---

## 📂 Dataset Details

- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/pima+indians+diabetes)
- **Instances**: 768
- **Features**: 8 (numeric)
- **Target**: `Outcome` (0 = Non-Diabetic, 1 = Diabetic)

---

## ✅ Preprocessing Steps Covered

### 1. 🔍 Handling Missing Values
- Certain features (like `Glucose`, `BMI`, etc.) had invalid zero values.
- These were replaced with `NaN` and then filled using **column mean**.

```python
df[invalid_cols] = df[invalid_cols].replace(0, np.nan)
df.fillna(df.mean(), inplace=True)
