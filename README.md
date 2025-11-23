🩺 Diabetes Prediction using Machine Learning

This project predicts whether a patient is diabetic using Machine Learning on the PIMA Indian Diabetes Dataset. The model is trained using Logistic Regression and includes preprocessing with StandardScaler.

📊 Dataset Used

PIMA Indian Diabetes Dataset
It contains medical attributes such as:

Feature	Description
Pregnancies	Number of pregnancies
Glucose	Plasma glucose concentration
Blood Pressure	Diastolic BP
Skin Thickness	Triceps skin fold thickness
Insulin	Serum insulin concentration
BMI	Body Mass Index
DiabetesPedigreeFunction	Diabetes hereditary factor
Age	Age
Outcome	1 = Diabetic, 0 = Not Diabetic

⚠️ Dataset belongs to UCI Repository.

🤖 Machine Learning Model

Logistic Regression

StandardScaler preprocessing

Train-Test Split (80%–20%)

🚀 How to Run the Project
✔ 1. Install Requirements
pip install -r requirements.txt

✔ 2. Train the Model
python src/train_model.py

✔ 3. Predict for a Patient
python src/predict.py

📁 Project Structure
Diabetes-Prediction-ML/
│
├── data/
│── ── diabetes.csv (optional)
│
├── notebook/
│── ── diabetes_prediction.ipynb
│
├── src/
│   ├── train_model.py
│   ├── predict.py
│   └── utils.py
│
├── models/
│   ├── diabetes_model.pkl
│   └── scaler.pkl
│
├── requirements.txt
├── README.md
└── LICENSE (optional)

🎯 Future Enhancements

Streamlit Web App

FastAPI REST API

Model Comparison (SVM, Random Forest, XGBoost)

Feature Importance Analysis

📜 License

This project is open-source and free to use with proper credit.

🙌 Contributions

Contributions are welcome!
Fork the repo, improve the project, and create a pull request.

📌 Step 2: Add and Push README to GitHub

Run these commands in your terminal:

git add README.md
git commit -m "Add README file"
git push
