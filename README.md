# 🔧 Hydraulic Pump Leakage Prediction using Machine Learning

This project uses machine learning to detect **internal pump leakage** in hydraulic systems, a critical component in the oil & gas industry. The goal is to support **predictive maintenance** by analyzing sensor data collected from a real-world industrial test rig.

---

## 📊 Dataset

- **Source**: [UCI / Kaggle - Condition Monitoring of Hydraulic Systems](https://archive.ics.uci.edu/ml/datasets/Condition+monitoring+of+hydraulic+systems)
- **Samples**: 2205 machine cycles
- **Sensors Used**:  
  - Pressure sensor (PS1)  
  - Motor power sensor (EPS1)  
  - Temperature sensor (TS1)  
  - Vibration sensor (VS1)  

Each sensor provides time-series readings during a 60-second operational cycle.

---

## 🔍 Problem Statement

Over time, pumps in hydraulic systems can develop **internal leakage**, which causes inefficiency and potential breakdown. The goal is to:
- Detect pump leakage early
- Enable predictive maintenance
- Prevent unplanned downtime

---

## 📈 Features & Approach

1. **Time-series data** is collected from 4 sensors.
2. For each sensor, we extract:
   - Mean
   - Standard Deviation
   - Minimum
   - Maximum
3. This gives a total of **16 features per sample**.
4. Labels are derived from `profile.txt`, where:
   - 0 = No leakage
   - 1/2 = Leakage present (combined into 1 for binary classification)

---

## 🤖 Model

- **Algorithm**: Random Forest Classifier
- **Train/Test Split**: 75/25
- **Accuracy**: ~99.8%
- **Evaluation Metrics**: Confusion Matrix, Classification Report

---

## 📊 Results

- The model accurately predicts whether internal leakage is occurring.
- Feature importance analysis reveals which sensor readings are most critical.

![Feature Importance](plots/feature_importance.png)

---

## 🚀 Future Improvements

- Include more sensors (flow, temp at multiple points)
- Multiclass classification (no, weak, severe leakage)
- Real-time data streaming
- Deploy via Streamlit dashboard or API

---

## 🛠️ Tech Stack

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Jupyter Notebook

---

## 📂 Files

- `pump_leakage_model.ipynb`: Full notebook with feature extraction, training, and evaluation
- `plots/`: Visualizations like feature importance
- `README.md`: Project summary and instructions

---

## 📌 How to Run

1. Clone the repository
2. Make sure you have the `.txt` data files in the working directory
3. Run the notebook: `pump_leakage_model.ipynb`

---

