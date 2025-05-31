# 🚀 SARAS-AI: Satellite Fault Prediction System

**SARAS-AI** (Surveillance-Aware Responsive AI System) is a smart, real-time fault prediction system designed for satellites — starting with the **power subsystem**. It uses deep learning models (like LSTM and Transformers) to anticipate failures in satellite telemetry data and enables ground stations to act before disaster strikes.

> “Antariksh mein bhi ab AI ka rakhwala hoga.” 🇮🇳

---

## 📌 Objective

Predict faults in satellite subsystems using AI, ensuring:
- Early detection of anomalies in voltage, current, temperature, and solar input.
- Real-time alerts via backend APIs or CLI.
- A modular, scalable, and extendable architecture for use in **ISRO**, **DRDO**, startups, and academia.

---

## 🔧 Features

- ✅ LSTM & Transformer-based AI models for time-series telemetry prediction
- ✅ Real-time inference via FastAPI
- ✅ Optional CLI or dashboard alerting
- ✅ Modular data pipeline (raw → processed → prediction)
- ✅ Scalable: easily extendable to other subsystems like propulsion, thermal, communication

---

## 🧠 System Architecture
[Satellite Telemetry] ↓ [Data Ingestion Layer] ← CSV / API / Simulated Input ↓ [Preprocessing] → Normalization, Outlier Handling ↓ [AI Model (LSTM / Transformer)] ↓ [Fault Predictor] ↓ [FastAPI / CLI / Dashboard Alerting]
---

## 📂 Folder Structure
saras-ai/ ├── app/ │   ├── main.py            # FastAPI App │   └── utils.py           # Preprocessing + Alert Logic ├── data/ │   ├── raw/ │   ├── processed/ │   └── mock_satellite_data.csv ├── models/ │   ├── lstm_model.pt │   └── transformer_model.pt ├── notebooks/ │   ├── 01_EDA.ipynb │   └── 02_Model_Training.ipynb ├── dashboard/             # Optional: React or Grafana UI ├── requirements.txt └── README.md
---

## 📈 Sample Data Format

| timestamp           | voltage | temperature | solar_input | current |
|---------------------|---------|-------------|-------------|---------|
| 2025-05-31 12:00:01 | 3.74V   | 26.4°C      | 102.3W      | 1.96A   |

Use real or simulated telemetry data for training and inference.

---

## 🧠 AI Models

| Model        | Use Case                         | Libraries       |
|--------------|----------------------------------|------------------|
| LSTM         | Time-series prediction           | PyTorch          |
| Transformer  | Long-sequence modeling           | PyTorch, HuggingFace |
| Autoencoder  | Fault detection (unsupervised)   | TensorFlow / PyTorch |

---

## ⚠️ Real-Time CLI Alert Example

⚠️ [FAULT DETECTED]
Timestamp: 2025-05-31 12:02:43
Issue: Voltage dip below 3.2V threshold
Model Confidence: 91.6%
Recommendation: Switch to backup power immediately.
