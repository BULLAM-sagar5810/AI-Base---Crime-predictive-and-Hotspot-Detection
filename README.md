# 🚔 AI-Based Crime Prediction and Hotspot Detection System for India

An intelligent web-based analytics platform that predicts future crime trends and identifies crime hotspot regions across India using Machine Learning and Geospatial Visualization.

This project combines historical crime analysis, predictive modeling, clustering algorithms, and interactive mapping to support proactive decision-making and crime prevention.

---

## 📌 Overview

Traditional crime analysis systems mostly depend on historical records and static reporting. This project transforms crime analysis into a predictive and data-driven process by combining:

- Machine Learning for crime forecasting
- Hotspot detection using clustering
- Interactive geospatial visualization
- District-level crime intelligence
- Risk classification and analytics

The system predicts future crime occurrences and identifies **High**, **Medium**, and **Low** risk regions.

---

## ✨ Features

### 🔮 Crime Prediction
- Predicts future crime counts using historical crime records
- Uses **Random Forest Regression**
- Supports district-level forecasting

### 📍 Hotspot Detection
- Detects crime-prone areas using **K-Means Clustering**
- Hybrid risk classification approach:
  - Cluster-based classification
  - Threshold-based validation

### 🗺️ Geospatial Visualization
- Interactive hotspot maps using **Leaflet.js**
- Color-coded risk markers:
  - 🔴 High Risk
  - 🟡 Medium Risk
  - 🟢 Low Risk

### 🌳 Hierarchical Risk Tree
Structured visualization:

```text
State
 ├── High Risk
 │    ├── District A
 │    └── District B
 ├── Medium Risk
 └── Low Risk
```

### ⚡ Data Processing
- Automated preprocessing
- Label encoding
- Feature engineering
- Lag features
- Rolling averages

---

# 🧠 Machine Learning Pipeline

## Prediction Model
**Random Forest Regression**

Used for:
- Crime count forecasting
- Pattern learning from historical data

Features:
- State Encoding
- District Encoding
- Crime Encoding
- Year
- Lag Features (1–4 years)
- Rolling Means (2–4 years)

---

## Hotspot Detection Model
**K-Means Clustering**

Used for:
- District segmentation
- Risk classification

Risk Levels:
- High
- Medium
- Low

---

# 🏗️ System Architecture

```text
Frontend (React + Tailwind)
          ↓
REST API (Flask)
          ↓
Data Processing
(Pandas + NumPy)
          ↓
Machine Learning
(Random Forest + KMeans)
          ↓
Visualization Layer
(Leaflet Maps)
```

---

# 🛠️ Tech Stack

## Frontend
- React (Vite)
- TypeScript
- Tailwind CSS
- Framer Motion
- Leaflet.js

## Backend
- Python
- Flask
- REST API

## Machine Learning
- Scikit-learn
- Random Forest Regression
- K-Means Clustering

## Data Processing
- Pandas
- NumPy

## Storage
- CSV
- JSON
- Joblib (.pkl)

---

# 📂 Project Structure

```bash
crime-prediction-system/
│
├── frontend/
│   ├── src/
│   ├── components/
│   └── pages/
│
├── backend/
│   ├── app.py
│   ├── models/
│   ├── data/
│   └── utils/
│
├── models/
│   ├── model.pkl
│   ├── trend_classifier.pkl
│   ├── state_encoder.pkl
│   ├── district_encoder.pkl
│   └── crime_encoder.pkl
│
├── data/
│   ├── crime_data_district_long.csv
│   └── district_coordinates.json
│
└── README.md
```

---

# 🚀 Installation

## Clone Repository

```bash
git clone https://github.com/your-username/crime-prediction-system.git

cd crime-prediction-system
```

---

## Backend Setup

Create virtual environment:

```bash
python -m venv venv
```

Activate:

**Windows**
```bash
venv\Scripts\activate
```

**Linux/Mac**
```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run backend:

```bash
python app.py
```

Backend runs at:

```text
http://localhost:5000
```

---

## Frontend Setup

Install packages:

```bash
npm install
```

Start application:

```bash
npm run dev
```

Frontend:

```text
http://localhost:5173
```

---

# 📡 API Endpoints

## Get Configuration

```http
GET /api/config
```

Returns:
- States
- Districts
- Crime Categories

---

## Predict Crime

```http
POST /api/predict
```

Request:

```json
{
  "state": "KARNATAKA",
  "district": "BANGALORE",
  "year": 2026,
  "crime": "MURDER"
}
```

Response:

```json
{
  "prediction": "Predicted Murder Cases = 530"
}
```

---

## Detect Hotspots

```http
POST /api/hotspots
```

Request:

```json
{
  "state": "KARNATAKA",
  "start_year": 2015,
  "end_year": 2025
}
```

---

# 📊 Results

- Prediction Accuracy: **~89%**
- District-level hotspot detection
- Interactive map visualization
- Risk classification support

---

# 🔒 Future Enhancements

- Real-time crime data integration
- Cloud deployment
- Mobile application
- Deep Learning (LSTM)
- Automated alerts
- GIS integration
- Role-based access control

---

# 📚 References

- NCRB Crime Reports
- Scikit-learn Documentation
- Leaflet Documentation
- Flask Documentation
- Kaggle Crime in India Dataset

---

# 👨‍💻 Author

**Student Name**  
Master of Computer Applications (MCA)

Guided by: **Dr. Name**

---

# 📄 License

This project is developed for educational and research purposes.
