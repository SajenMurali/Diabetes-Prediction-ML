# 🩺 Diabetes Prediction using Machine Learning

This project predicts whether a patient is diabetic based on medical diagnostic measurements using a Machine Learning model.

## 📊 Dataset
Dataset used: **PIMA Indian Diabetes Dataset**  
Attributes include:
- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age
- Outcome (0 = Non-diabetic, 1 = Diabetic)

> ⚠️ Note: If you upload the dataset, mention proper credits. Avoid sharing copyrighted data.

## 🤖 Model Used
- **SVM** (baseline)
- Data Preprocessing with **StandardScaler**
- 80%-20% train-test split

## 🚀 How to Run

### 1️⃣ Install dependencies
```bash
pip install -r requirements.txt
### Train the model
```bash
python src/train_model.py
### 📁 Project Structure
```bash
Diabetes-Prediction-ML/
├── data/
├── notebook/
├── src/
├── models/
├── requirements.txt
└── README.md
### CODE
```bash

---

### 💾 Save Your Model and Scaler

In `train_model.py`:

```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LogisticRegression
import joblib

df = pd.read_csv("data/diabetes.csv")

X = df.drop('Outcome', axis=1)
y = df['Outcome']

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

model = LogisticRegression()
model.fit(X_scaled, y)

joblib.dump(model, "models/diabetes_model.pkl")
joblib.dump(scaler, "models/scaler.pkl")
import numpy as np
import joblib

model = joblib.load("models/diabetes_model.pkl")
scaler = joblib.load("models/scaler.pkl")

input_data = (1,103,30,38,83,43.3,0.183,33)
input_array = np.asarray(input_data).reshape(1, -1)

input_scaled = scaler.transform(input_array)
prediction = model.predict(input_scaled)

if prediction[0] == 1:
    print("The patient is diabetic")
else:
    print("The patient is not diabetic")


