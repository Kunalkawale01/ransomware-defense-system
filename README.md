# AI-Based Ransomware Detection and Defense System

An intelligent, real-time ransomware detection and alerting system that monitors system processes, extracts behavioral features, applies a machine learning model to detect ransomware activity, and displays alerts on a web-based dashboard.

This project is designed for **academic use, demonstrations, and learning system security concepts**.
---
## Features
- **Machine Learning–based Detection**
- **Real-time Process Monitoring**
- **Automatic Ransomware Alerts**
- **Flask Web Dashboard**
- **Fake Ransomware Simulator for Testing**
- Feature-based behavioral analysis
---
## Project Architecture

    ransomware-defense-COMPLETE/
    │
    ├── agent/
    │ ├── agent.py # Main monitoring agent
    │ ├── ai/
    │ │ └── predictor.py # ML prediction logic
    │ ├── monitor/
    │ │ └── process_monitor.py # Process feature extraction
    │ └── init.py
    │
    ├── backend/
    │ └── api.py # Flask backend + dashboard
    │
    ├── fake_ransomware.py # Ransomware attack simulator
    ├── requirements.txt

---
## Tech Stack
- **Python 3.9+**
- **Flask**
- **scikit-learn**
- **psutil**
- **watchdog**
- **NumPy / Pandas**
- **Joblib**
---
## How to Run the Project
### step 1️ : Clone the repository

```
File is too long so mail me if you want this project kunalkawale62@gmail.com
cd ransomware-defense-system
```
---
### step 2 : Create & activate virtual environment

Windows
```
python -m venv venv
venv\Scripts\activate
```
---
Linux / macOS
```
python -m venv venv
source venv/bin/activate
```
---
### step 3 : Install dependencies
```
python -m pip install -r requirements.txt
```
This installs:
- psutil
- watchdog
- numpy
- pandas
- scikit-learn
- flask
- joblib
- web3
---
### step 4 : Start the backend server

Open Terminal 1:

Run 
```
python backend/api.py
```
Backend runs at:
```
http://127.0.0.1:5000
```
In your browser, go to:
```
http://127.0.0.1:5000
```
You’ll see the ransomware monitoring dashboard
---
### step 5 : Run the monitoring agent

Open Terminal 2 (keep backend running):

Must be run from project root
```
python -m agent.agent
```
You should see:
```
[INFO] Agent started
[INFO] System is NORMAL
```
---
### Detection Flow
```
Process Monitoring
        ↓
Feature Extraction
        ↓
ML Prediction Model
        ↓
Alert Generation
        ↓
Flask Dashboard
```
---
### Machine Learning Overview

- Behavioral features are extracted from running processes
- A trained ML model classifies activity as:
```
0 → Normal
1 → Ransomware
```
- Predictions trigger alerts sent to the backend API
---
### Common Issues

- Import errors

1. Always run agent using:
```
python -m agent.agent
```
2. Backend not receiving alerts
```
Ensure Flask server is running before starting agent
```
