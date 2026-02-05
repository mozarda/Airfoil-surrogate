# ✈️ Airfoil Self-Noise Surrogate
**Real-time Aeroacoustic Prediction via ONNX Runtime Web**

## 📌 Overview
This project develops a high-fidelity surrogate model to predict the scaled sound pressure level of airfoil blade sections. By approximating complex CFD/Acoustic data with a Neural Network, we reduce simulation time from hours to milliseconds.

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