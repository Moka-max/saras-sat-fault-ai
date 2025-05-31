# 🚀 SARAS-AI: Satellite Fault Prediction System 🛰️  
*A real-time AI-powered system to forecast faults in satellite subsystems.*

> Developed by **Moka Uday Bhushanam**  
> Aerospace + AI | ECE + Data Science | 🇮🇳

---

## 📌 Overview

**SARAS-AI** (Surveillance-Aware Responsive AI System) is a deep-tech fault prediction system for satellites. It uses time-series machine learning models (LSTM, Transformer) to detect anomalies in satellite telemetry — beginning with the **Power Subsystem**.

The goal: build an operational prototype that can plug into ground stations, simulate real telemetry, and detect faults before they escalate — combining aerospace engineering with AI firepower.

---

## 🌟 Key Features

- ✅ LSTM and Transformer models for fault prediction
- ⚠️ Real-time anomaly detection with alerting
- 📈 Dashboard visualization (React.js / Grafana)
- 📡 Mock & real satellite telemetry supported
- 🔐 Modular backend using FastAPI

---

## 💼 Use Cases

- 🛰 Satellite mission operations (LEO/MEO/GEO)
- 🚨 Fault prediction for power, thermal, and attitude subsystems
- 🧪 Academic and industrial R&D (ISRO/DRDO)
- 📚 Learning-grade open-source demo project

---

## 🧠 Model Architecture

| Model         | Use Case                     | Strengths                     | Limitations                  |
|---------------|------------------------------|-------------------------------|------------------------------|
| **LSTM**      | Basic time-series prediction | Simple, interpretable         | Struggles with long patterns |
| **Transformer** | Long-term dependencies       | Accurate, scalable            | Heavier compute              |
| **AutoEncoder** | Unlabeled data anomaly detection | Unsupervised, flexible     | Less precision               |

We start with **LSTM**, then upgrade to **Informer** or **TSFormer** for large-scale testing.

---

## 📂 Project Folder Structure
saras-sat-fault-ai/
├── data/
│   ├── raw/                   # Raw telemetry datasets (unprocessed)
│   ├── processed/             # Cleaned and labeled data for training/testing
│   └── mock_satellite_data.csv # Sample generated telemetry data
├── models/                    # Trained AI models and checkpoints
│   └── lstm_fault_predictor.pt
├── notebooks/                 # Jupyter notebooks for EDA & model development
│   ├── 01_EDA.ipynb
│   └── 02_LSTM_Training.ipynb
├── app/                       # Backend API and utilities
│   ├── main.py                # FastAPI app entry point
│   └── utils.py               # Helper functions for data processing
├── dashboard/                 # Frontend UI for real-time visualization
│   ├── src/                   # React components and assets
│   └── public/                # Static files
├── tests/                     # Unit and integration tests
│   └── test_model.py
├── requirements.txt           # Python dependencies
├── README.md                  # Project documentation (you’re here!)
└── .gitignore                 # Git ignore rules
---

## ⚙️ Tech Stack

- **Languages**: Python 3.10
- **AI/ML**: PyTorch, NumPy, Scikit-learn
- **Backend**: FastAPI
- **Frontend**: React.js + Plotly.js OR Grafana
- **Database**: InfluxDB (optional) / CSV
- **DevOps**: Git, Docker (future scope)

---

## 🔧 Setup Instructions

# Clone the repo
git clone https://github.com/<your-username>/saras-sat-fault-ai.git
cd saras-sat-fault-ai

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Run the FastAPI backend 
uvicorn app.main:app --reload
