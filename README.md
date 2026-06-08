<div align="center">

# 🏎️ F1 Pit Stop Strategy Prediction System

### Predicting Formula 1 Pit Stops using Machine Learning and Race Telemetry Data

[![Python](https://img.shields.io/badge/Python-3.11+-blue?style=for-the-badge&logo=python)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-black?style=for-the-badge&logo=pandas)](https://pandas.pydata.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?style=for-the-badge&logo=scikitlearn)](https://scikit-learn.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-blue?style=for-the-badge&logo=numpy)](https://numpy.org/)

---

### 🚦 Machine Learning for Real-Time Formula 1 Strategy Decisions

Predicts whether a driver is likely to pit on the next lap using race telemetry, tyre degradation, lap times, and race progression data.

</div>

---

## 📌 Project Overview

Pit stop timing is one of the most critical decisions in Formula 1.

A stop made too early sacrifices tyre life.

A stop made too late results in performance loss due to tyre degradation.

This project leverages historical Formula 1 race data and machine learning to predict:

> **"Will the driver pit on the next lap?"**

The system learns race strategy patterns from previous seasons and generates pit-stop predictions using race telemetry features.

---

## 🎯 Problem Statement

Given a driver's current race state:

- Current lap time
- Tyre life
- Position
- Previous lap performance
- Race progress
- Recent pace trends

Predict:

✅ Pit Next Lap

❌ Continue Current Stint

---

## 📊 Dataset Information

The dataset contains over:

| Metric              | Value            |
| ------------------- | ---------------- |
| Total Records       | 101,371+         |
| Seasons             | 2022 - 2025      |
| Features            | 16+ Raw Features |
| Engineered Features | 8+               |
| Target Variable     | PitNextLap       |

### Key Columns

```text
Driver
LapNumber
Compound
Stint
TyreLife
Position
LapTime
Race
Year
PitNextLap
```

---

## ⚙️ Feature Engineering

Several race-aware features were engineered to capture strategy behavior.

### Previous Lap Time

```python
prev_lap_time
```

Helps measure performance changes over time.

---

### Rolling Average Pace

```python
avg_last_3_laps
```

Captures recent performance trend.

---

### Lap Time Difference

```python
lap_time_diff
```

Measures pace degradation.

---

### Previous Position

```python
prev_position
```

Tracks track-position dynamics.

---

### Race Progress

```python
race_progress
```

Normalizes race stage.

---

### Laps Since Last Pit

```python
lap_since_last_pit
```

Captures stint length.

---

## 🧠 Machine Learning Model

### Random Forest Classifier

```python
RandomForestClassifier(
    n_estimators=100,
    class_weight="balanced",
    random_state=42
)
```

### Why Random Forest?

- Handles non-linear relationships
- Robust against noisy telemetry data
- Captures complex race strategy patterns
- Requires minimal preprocessing

---

## 📈 Model Performance

### Test Set (2024–2025)

| Metric            | Score   |
| ----------------- | ------- |
| Accuracy          | **81%** |
| Precision         | **80%** |
| Recall            | **81%** |
| Weighted F1 Score | **80%** |

### Classification Report

| Class            | Precision | Recall | F1   |
| ---------------- | --------- | ------ | ---- |
| No Pit (0)       | 0.83      | 0.88   | 0.86 |
| Pit Next Lap (1) | 0.74      | 0.65   | 0.69 |

---

## 🏗️ Project Structure

```text
F1-PitStop-Prediction/
├── F1Strategy.ipynb
│
└── README.md
```

---

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/F1-PitStop-Prediction.git

cd F1-PitStop-Prediction
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
F1Strategy.ipynb
```

Run all cells to:

- Load data
- Engineer features
- Train model
- Evaluate performance
- Generate predictions

---

## 🔬 Future Improvements

- XGBoost implementation
- LightGBM implementation
- Driver-specific strategy models
- Weather-aware predictions
- Safety Car prediction integration
- Real-time telemetry streaming
- Lap-by-lap race simulation engine

---

## 💡 Skills Demonstrated

### Machine Learning

- Supervised Learning
- Classification
- Model Evaluation
- Feature Engineering

### Data Science

- Pandas
- NumPy
- Exploratory Data Analysis
- Data Cleaning

### Sports Analytics

- Formula 1 Strategy Analysis
- Tyre Degradation Modeling
- Race Performance Metrics

### Software Engineering

- Modular ML Pipeline
- Reproducible Experiments
- Git & GitHub

---

## 📚 Technologies Used

| Category         | Tools            |
| ---------------- | ---------------- |
| Language         | Python           |
| Data Analysis    | Pandas, NumPy    |
| Machine Learning | Scikit-Learn     |
| Visualization    | Matplotlib       |
| Development      | Jupyter Notebook |
| Version Control  | Git, GitHub      |

---

## 🌟 Key Takeaways

- Built an end-to-end machine learning pipeline on 100K+ Formula 1 race records.
- Engineered race-specific features inspired by real-world F1 strategy decisions.
- Achieved **81% prediction accuracy** on unseen future seasons.
- Demonstrated application of machine learning in sports analytics.

---

<div align="center">

### ⭐ If you found this project interesting, consider giving it a star!

**Built with Python, Machine Learning, and a passion for Formula 1 🏎️**

</div>
