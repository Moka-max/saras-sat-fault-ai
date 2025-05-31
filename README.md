# 🛰️ SARAS-AI: Satellite Fault Prediction System

**SARAS-AI** (Surveillance-Aware Responsive AI System) is a cutting-edge artificial intelligence platform built to monitor, analyze, and predict faults in satellite subsystems—starting with the **power subsystem**.  

This project simulates real-time telemetry, processes critical health parameters like voltage, current, temperature, and solar input, and uses deep learning models (LSTM, Transformer) to issue early warnings and predictive alerts for spaceborne systems.

> 🧠 “In space, failure isn’t an option. SARAS makes sure it isn’t a surprise either.”  

---

## 🧭 Vision

- 🚨 **Early Fault Detection**: AI-based anomaly prediction before failure strikes.
- 🔐 **National Security Applications**: Ideal for ISRO, DRDO, private aerospace ventures.
- 🧪 **Modular R&D Tool**: Tailored for researchers, engineers, and institutions working on satellite health monitoring.

---

## 🧰 Features

- ✅ **AI Models**: LSTM & Transformer-based predictions
- ✅ **Real-Time Telemetry Simulation & Processing**
- ✅ **FastAPI REST Server for Fault Inference**
- ✅ **Custom CLI Alerts for Mission Control**
- ✅ **Scalable & Extendable** to other satellite subsystems
- ✅ **Dashboard-Ready** for Grafana / Plotly.js integration

---

## ⚙️ System Architecture


  [Simulated / Real Telemetry Input]
                ↓
        [Data Preprocessing]
                ↓
       [AI Model: LSTM / Transformer]
                ↓
          [Fault Predictor]
                ↓
  [API Server / CLI Alert / Dashboard Hook]
