
# ðŸ›°ï¸ SARAS-AI: Satellite Fault Prediction System

**SARAS-AI** (Surveillance-Aware Responsive AI System) is a cutting-edge artificial intelligence platform built to monitor, analyze, and predict faults in satellite subsystemsâ€”starting with the **power subsystem**.  

This project simulates real-time telemetry, processes critical health parameters like voltage, current, temperature, and solar input, and uses deep learning models (LSTM, Transformer) to issue early warnings and predictive alerts for spaceborne systems.

> ðŸ§  â€œIn space, failure isnâ€™t an option. SARAS makes sure it isnâ€™t a surprise either.â€  

---

## ðŸ§­ Vision

- ðŸš¨ **Early Fault Detection**: AI-based anomaly prediction before failure strikes.
- ðŸ” **National Security Applications**: Ideal for ISRO, DRDO, private aerospace ventures.
- ðŸ§ª **Modular R&D Tool**: Tailored for researchers, engineers, and institutions working on satellite health monitoring.

---

## ðŸ§° Features

- âœ… **AI Models**: LSTM & Transformer-based predictions
- âœ… **Real-Time Telemetry Simulation & Processing**
- âœ… **FastAPI REST Server for Fault Inference**
- âœ… **Custom CLI Alerts for Mission Control**
- âœ… **Scalable & Extendable** to other satellite subsystems
- âœ… **Dashboard-Ready** for Grafana / Plotly.js integration

---

## âš™ï¸ System Architecture

```text
  [Simulated / Real Telemetry Input]
                â†“
        [Data Preprocessing]
                â†“
       [AI Model: LSTM / Transformer]
                â†“
          [Fault Predictor]
                â†“
  [API Server / CLI Alert / Dashboard Hook]
```

---

## ðŸ§  AI Models

| Model Type     | Description                          | Framework        |
|----------------|--------------------------------------|------------------|
| **LSTM**       | Predicts temporal sequences          | PyTorch          |
| **Transformer**| Handles long-range dependencies      | HuggingFace/Transformers |
| **Autoencoder**| Anomaly detection (optional)         | TensorFlow / PyTorch |

---

## ðŸ“‚ Project Structure

```bash
saras-ai/
â”œâ”€â”€ app/
â”‚   â”œâ”€â”€ main.py             # FastAPI Inference Server
â”‚   â”œâ”€â”€ predict.py          # Model loading & prediction
â”‚   â””â”€â”€ utils.py            # Preprocessing + alert logic
â”œâ”€â”€ models/
â”‚   â”œâ”€â”€ lstm_model.pt
â”‚   â””â”€â”€ transformer_model.pt
â”œâ”€â”€ data/
â”‚   â”œâ”€â”€ raw/
â”‚   â””â”€â”€ processed/
â”œâ”€â”€ notebooks/
â”‚   â”œâ”€â”€ 01_EDA.ipynb
â”‚   â””â”€â”€ 02_Model_Training.ipynb
â”œâ”€â”€ dashboard/              # Optional: React/Grafana UI
â”œâ”€â”€ requirements.txt
â”œâ”€â”€ LICENSE
â””â”€â”€ README.md
```

---

## ðŸ“Š Telemetry Format

| timestamp           | voltage | temperature | solar_input | current |
|---------------------|---------|-------------|-------------|---------|
| 2025-05-31 12:00:01 | 3.74V   | 26.4Â°C      | 102.3W      | 1.96A   |

---

## ðŸš€ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/saras-ai.git
cd saras-ai
```

### 2. Install Requirements

```bash
pip install -r requirements.txt
```

### 3. Run the Inference Server

```bash
uvicorn app.main:app --reload
```

### 4. Run CLI Alert Mode (Optional)

```bash
python app/main.py --input data/processed/telemetry.csv
```

---

## ðŸ“¡ API Endpoints (via FastAPI)

| Endpoint           | Method | Description                  |
|--------------------|--------|------------------------------|
| `/predict`         | POST   | Send telemetry data & get fault prediction |
| `/health-check`    | GET    | System status                |

Example payload:
```json
{
  "voltage": 3.42,
  "temperature": 26.8,
  "solar_input": 101.5,
  "current": 1.92
}
```

---

## âš ï¸ Sample CLI Alert Output

```bash
[ALERT] ðŸš¨ FAULT DETECTED!
Timestamp: 2025-05-31 12:02:43
Issue: Voltage dropped below 3.2V threshold.
Model Confidence: 93.2%
Suggested Action: Switch to backup power unit.
```

---

## ðŸ› ï¸ Tech Stack

- **Languages**: Python
- **Frameworks**: FastAPI, PyTorch, NumPy, Pandas
- **Visualization (Optional)**: Plotly, Grafana, React.js
- **Deployment**: Docker-ready, Uvicorn, cloud-native structure

---

## ðŸ“Œ Use Cases

| Domain        | Application                                 |
|---------------|---------------------------------------------|
| ðŸ›°ï¸ ISRO/DRDO    | AI-based satellite subsystem monitoring    |
| ðŸ§ª Academia     | Telemetry-based fault research             |
| ðŸ›¡ï¸ Defense      | Automated satellite alerting               |
| ðŸ“Š Startups     | Integrate AI telemetry into nanosats       |

---

## ðŸ‘¨â€ðŸ’» Author

**Moka Uday Bhushanam**  
Founder, **VoltEdge** | ECE + Aerospace + Data Science @ IITM & ECA  

> _"Satellites don't sleep â€” SARAS ensures they don't suffer."_  

ðŸ“Ž [LinkedIn](https://linkedin.com/) â€¢ [GitHub](https://github.com/your-username) â€¢ [Twitter](https://twitter.com/)

---

## ðŸ—ºï¸ Roadmap

- [x] LSTM training for power subsystem
- [x] Real-time CLI alerts
- [x] FastAPI server integration
- [ ] Transformer integration for multivariate prediction
- [ ] Add dashboard interface (React / Plotly / Grafana)
- [ ] Expand to other subsystems (thermal, propulsion, comm)
- [ ] Cloud-native deployment (AWS, Azure, or ISRO IN-SPACe)

---

## ðŸ“œ License

This project is licensed under the [MIT License](LICENSE).

---

## ðŸ¤ Contribution Guidelines

Pull requests, forks, and collaborations are welcome!  
To contribute:
1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request with a detailed explanation.

---

## ðŸ™Œ Acknowledgements

- Inspired by satellite missions like **IRNSS**, **RISAT**, **GSAT**, and **Chandrayaan**.
- Special thanks to AI research in aerospace and defense domains.

---

## ðŸ”­ Final Word

SARAS-AI isnâ€™t just a tool. Itâ€™s a **movement**â€”to make Indiaâ€™s space systems smarter, safer, and self-reliant.

> ðŸš€ _â€œIf satellites are the eyes in the sky, SARAS is the brain behind them.â€_
