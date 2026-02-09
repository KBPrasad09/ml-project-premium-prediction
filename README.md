🏥 Health Insurance Premium Prediction App
This project is a machine learning–powered Streamlit web application that predicts a user’s annual health insurance premium based on demographic, lifestyle, and medical history inputs.
It provides a clean, interactive UI and uses trained ML models to generate accurate premium estimates.

🚀 Live Demo
Your app is deployed on Streamlit Cloud:

👉 (Add your Streamlit URL here once deployed)  
https://premium-predictor.streamlit.app


📌 Project Overview
This application predicts health insurance costs using:

User demographic data (age, gender, region, marital status)

Lifestyle factors (BMI category, smoking status, employment status)

Financial information (income, dependants)

Medical history (diabetes, thyroid, heart disease, etc.)

Genetical risk score

Normalized medical risk score (computed automatically)

The app uses two separate models:

Young Model → for users aged ≤ 25

Rest Model → for users aged > 25

Both models are pre‑trained and stored in the artifacts/ folder.

🧠 Machine Learning Workflow
✔ Data Preprocessing
One‑hot encoding for categorical variables

Normalization using MinMaxScaler

Custom medical risk scoring

Age‑based model selection

Scaling handled dynamically based on age group

✔ Models Used
model_young.joblib

model_rest.joblib

Both models were trained offline and exported using joblib.

✔ Scalers
scaler_young.joblib

scaler_rest.joblib

Each scaler contains:

cols_to_scale

scaler object

🗂 Project Structure
Code
ml-project-premium-prediction/
│
├── artifacts/
│   ├── model_rest.joblib
│   ├── model_young.joblib
│   ├── scaler_rest.joblib
│   └── scaler_young.joblib
│
├── main.py
├── prediction_helper.py
├── requirements.txt
└── README.md
🖥 How to Run Locally
1️⃣ Clone the repository
bash
git clone https://github.com/<your-username>/ml-project-premium-prediction.git
cd ml-project-premium-prediction
2️⃣ Install dependencies
bash
pip install -r requirements.txt
3️⃣ Run the Streamlit app
bash
streamlit run main.py
🌐 Deployment (Streamlit Cloud)
This app is deployed using Streamlit Cloud.

Deployment steps:

Push your project to GitHub

Go to https://share.streamlit.io

Click New App

Select:

Repository: ml-project-premium-prediction

Branch: main

Main file: main.py

Deploy

Streamlit Cloud automatically:

Installs dependencies from requirements.txt

Loads your models from artifacts/

Runs your app

📦 Dependencies
Your requirements.txt includes:

Code
streamlit
pandas
joblib
scikit-learn
xgboost
These are required to load your models and run the app.

⚠️ Important Notes
You may see warnings about scikit‑learn version mismatch — this is normal when loading joblib models trained on older versions.

XGBoost must be included in requirements.txt because your model artifacts depend on it.

The app uses age‑based model selection for improved accuracy.

🙌 Acknowledgements
This project was built as part of a machine learning learning journey, focusing on:

Data preprocessing

Feature engineering

Model training and evaluation

Streamlit UI development

Cloud deployment
