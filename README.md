🧠 Stroke Prediction and Nearby Hospital Recommendation System
This project is a Machine Learning-based web application that predicts the risk of stroke using patient medical data. If a user is at high risk, it also suggests nearby hospitals using OpenStreetMap and Overpass API — all without using any paid services like Google Maps.

🚀 Features
🔍 Predicts stroke likelihood based on medical attributes.

🗺️ Displays nearby hospitals on an interactive map.

🧪 Built using a trained machine learning model (Logistic Regression/XGBoost).

🌍 Uses Folium + Overpass API for map rendering and hospital discovery.

🎛️ User-friendly Streamlit interface.

✅ Runs locally or can be deployed on platforms like GitHub, Streamlit Cloud, or Heroku.

📊 Input Features
Feature Name	Description
gender	Male, Female, Other
age	Age of the person
hypertension	0 = No, 1 = Yes
heart_disease	0 = No, 1 = Yes
ever_married	Yes / No
work_type	e.g., Private, Self-employed, Govt job
Residence_type	Urban / Rural
avg_glucose_level	Average glucose level in blood
bmi	Body Mass Index
smoking_status	Never smoked / Formerly smoked / Smokes

🧠 Model Overview
Algorithm: Logistic Regression / XGBoost Classifier

Preprocessing: Label encoding, standardization

Training: Based on Stroke Prediction Dataset

Evaluation Metrics: Accuracy, Precision, Recall, F1-Score

🌍 Hospital Mapping (Folium + Overpass API)
Uses OpenStreetMap and Overpass API to locate hospitals near the user.

Gets geolocation based on IP or input manually (latitude/longitude).

No usage of Google Maps API, making it cost-effective and open-source friendly.

🛠️ Tech Stack
Component	Technology
Frontend	Streamlit
ML Model	Scikit-learn, XGBoost
Mapping	Folium, OpenStreetMap, Overpass API
Backend	Python
Deployment	Streamlit / GitHub Pages / Heroku

📦 Installation
bash
Copy
Edit
git clone https://github.com/yourusername/stroke-predictor.git
cd stroke-predictor
pip install -r requirements.txt
streamlit run app.py
📁 File Structure
bash
Copy
Edit
stroke-predictor/
│
├── model.pkl                  # Trained ML model
├── app.py                     # Main Streamlit application
├── hospital.py                # Hospital recommendation logic
├── utils.py                   # Preprocessing / Encoding functions
├── requirements.txt
└── README.md
🌐 Sample UI
A form where users input their medical info.

A prediction button that shows:

Result: "You are at high risk" or "Low risk"

Map: Nearby hospitals based on user location

