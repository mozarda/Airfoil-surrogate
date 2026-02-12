# 📅 10-Day Sprint: Physics-AI Bridge Project
**Status:** Day 3 (Friday Baseline Phase)

## ✅ Phase 1: Identity & Infrastructure (Completed)
- [x] Bilingual LinkedIn & Wantedly profiles.
- [x] GitHub branding with professional badges.
- [x] Repository skeletons for 3 major projects.

## 🛠 Phase 2: The Baseline (Completed)
- [x] Initial EDA on Airfoil Self-Noise dataset.
- [x] Benchmarking established:
  - **XGBoost:** $R^2 = 0.94$ (MSE: 3.19, RMSE: 1.79)
  - **Random Forest:** $R^2 = 0.93$ (baseline comparison)
  - **Vanilla MLP:** $R^2 = 0.65$ (identified scaling as bottleneck)
- [x] Results documented in README baseline report.
- [x] Confirmed data-driven approach with quantified metrics.

## 🚀 Phase 3: Deep Learning Exploration (In Progress)
- [ ] Investigate advanced architectures (attention mechanisms, residual networks).
- [ ] Implement proper normalization and regularization (BatchNorm, Dropout).
- [ ] Hyperparameter grid search (learning rate, layer sizes, activation functions).
- [ ] **Goal:** Exceed XGBoost performance ($R^2 > 0.94$).
- [ ] Implement PyTorch Lightning `DataModule` and `LightningModule`.
- [ ] Export optimal model to **ONNX**.
- [ ] Deploy React + ONNX demo to **Cloudflare Pages**.

## 🔬 Phase 4: Advanced Domain Projects (Future)
- [ ] NASA Milling Dataset: Time-series signal processing with LSTMs.
- [ ] Concrete PINN: Physics-informed neural networks with monotonicity constraints.
- [ ] Multi-fidelity surrogate modeling.