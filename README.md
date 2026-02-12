# ✈️ Airfoil Self-Noise Surrogate
**Real-time Aeroacoustic Prediction via ONNX Runtime Web**

## 📌 Overview
This project develops a high-fidelity surrogate model to predict the scaled sound pressure level of airfoil blade sections. By approximating complex CFD/Acoustic data with machine learning models, we reduce simulation time from hours to milliseconds.

## 📊 Baseline Results & Benchmarking
**Data-driven engineering approach:** Establishing baseline metrics before iterative improvement.

| Model | $R^2$ Score | MSE | RMSE | Status |
|-------|---------|-----|------|--------|
| **XGBoost** | 0.94 | 3.19 | 1.79 | ✅ Baseline Champion |
| **Random Forest** | 0.93 | - | - | ✅ Ensemble Baseline |
| **Vanilla MLP** | 0.65 | 17.37 | 4.17 | 🔧 Needs Optimization |

**Observations:**
- Gradient boosting outperforms ensemble averaging by 1 point.
- Neural network significantly underperforms; scaling and architecture are key bottlenecks.
- **Next phase:** Deep learning with proper normalization, regularization, and architecture design to exceed XGBoost's $R^2 = 0.94$.

## 🏗️ Technical Architecture
Developed with **PyTorch Lightning**, this repository features a modular pipeline:
- `src/datasets`: Handles NASA Airfoil Self-Noise data (Frequency, Alpha, Chord, Velocity).
- `src/modules`: LightningModule for training logic and metric tracking.
- `src/pipeline`: Automated export to **ONNX** for browser-based inference.

## 🚀 Web Demo
The model is deployed via **Cloudflare Pages**, utilizing **ONNX Runtime Web** for client-side execution. 
[View Live Demo →](https://ai-demo.rosyada.my.id)

## 📊 Dataset
NASA dataset consisting of 1,503 instances from aerodynamic and acoustic tests in anechoic wind tunnels.