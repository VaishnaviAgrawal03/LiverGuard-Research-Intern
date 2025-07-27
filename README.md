# 🛡️ LiverGuard – AI-Driven IoT System for Liver Disease Detection

LiverGuard is a smart, non-invasive system that integrates sensors and machine learning to **detect and monitor liver diseases**. This project combines **IoT-based health sensing** with **ML-based prediction** and presents it all through an intuitive Streamlit interface.

Built as a collaborative effort during our internship, LiverGuard leverages real-time biomedical data from skin sensors, thermal imaging, and temperature sensing to predict the likelihood of liver Health.
---

## 📌 Objectives

- 🎯 Enable **early diagnosis** of liver disease using non-invasive methods
- 🔬 Use real-time data from **skin impedance**, **color sensors**, and **thermal imaging**
- 📉 Reduce delay in medical intervention via at-home, connected systems
- 🤖 Leverage ensemble machine learning for **highly accurate predictions**

---

## 🧠 Technologies Used

### ⚙️ Hardware:
- ESP32 Microcontroller
- RGB Color Sensor (for skin tone/jaundice)
- GSR Sensor (for skin impedance)
- Thermal IR Array Camera
- Temperature Sensor Module

### 🧪 Software & Tools:
- **Streamlit** – Web app interface
- **Python** – Backend logic and ML
- **Scikit-learn**, **XGBoost**, **CatBoost** – Machine Learning
- **SMOTE**, **Random Noise Injection** – Data Augmentation
- **Arduino IDE** – Embedded code deployment

---

## 🏗️ Architecture

1. **Sensor Layer**: Captures skin, temp, and thermal data.
2. **ESP32 & Arduino Layer**: Sends data via serial.
3. **Preprocessing Layer**: Normalizes inputs and computes features.
4. **ML Inference Layer**: Uses stacked + voting ensemble models.
5. **Streamlit App**: Displays predictions and confidence scores.

---

## ⚙️ ML Pipeline Overview

- 📈 **Data Collection**: From college students and elderly patients.
- 🧪 **Data Augmentation**: SMOTE & random noise injection
- 🧼 **Preprocessing**: Color space transformation, feature encoding
- 🔁 **Training Models**: RF, SVM, LR, XGBoost, CatBoost
- 🧠 **Ensemble Models**: Stacking + Soft Voting
- ✅ **Evaluation**:
  - Accuracy: **95%**
  - ROC-AUC: **0.987**
  - F1 Score: **0.93 (Unhealthy)**, **0.96 (Healthy)**

---

## 🚀 Features

- 🧠 Trained ML models: **Stacked model** and **Voting classifier**
- 📊 Scaler to normalize inputs before prediction
- ⚙️ Built with **Streamlit** for quick and interactive deployment
- 🎥 Demo video: `demo.mp4` (optional walkthrough)
- ✅ Tested on real medical datasets

---

## 🧠 Models Used

- **Scaler (`scaler.pkl`)**: Normalizes input features  
- **Voting Model (`voting_model.pkl`)**: Ensemble of base classifiers using majority voting  
- **Stacked Model (`stacked_model.pkl`)**: Combines predictions of base models into a meta-model for final prediction  

---

## 🖥️ How to Run the App Locally

python -m venv venv

venv\Scripts\activate  # For Windows
# OR
source venv/bin/activate  # For macOS/Linux

pip install -r requirements.txt

streamlit run streamlit_app.py

## 📂 Project Structure


├── .streamlit/            # Streamlit config (theme, etc.)

│ └── config.toml

├── README.md              # Project description and instructions

├── scaler.pkl             # Feature scaler (e.g., StandardScaler) or or Pre-trained input scaler

├── stacked_model.pkl      # Stacked ensemble machine learning model 

├── voting_model.pkl       # Voting ensemble model or Trained voting classifier

├── requirements.txt       # Python package dependencies

├── demo.mp4               # Demo video walkthrough

├── streamlit_app.py       # Main Streamlit application file

└── .streamlit/config.toml    # Streamlit UI configuration
