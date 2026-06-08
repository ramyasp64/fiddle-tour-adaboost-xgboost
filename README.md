# 🚕 Fiddle Tour, Efficient Trajectory-Based Fraudulent Taxi Trip Detection using AdaBoost and XGBoost

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/XGBoost-red?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/Type-B.Tech%20Thesis-blue?style=for-the-badge"/>
</p>

> **B.Tech Thesis Project** · National Engineering College, India · Jun 2022  
> Final Year Capstone, Information Technology

---

## 🎯 Project Overview

Building on the KNN foundational study, this thesis introduces a complete, production-oriented fraud detection system, **Fiddle Tour**, using **ensemble learning methods** (AdaBoost and XGBoost) combined with a **novel heuristic trajectory construction algorithm** for handling sparse GPS data.

Conventional fraud detection methods prove challenging in real-world scenarios: GPS data is noisy, fraud routes are designed to look legitimate, and rule-based systems fail on edge cases. Fiddle Tour addresses all three problems simultaneously.

---

## 🆕 What's New vs. the KNN Baseline

| Aspect | KNN (Mini Project) | AdaBoost + XGBoost (Thesis) |
|--------|--------------------|-----------------------------|
| Classifier | K-Nearest Neighbour | AdaBoost + XGBoost (ensemble) |
| Trajectory handling | Raw GPS features | Novel heuristic trajectory construction |
| Sparse data | Suboptimal | Robust reconstruction algorithm |
| Accuracy | Improved over map-matching | Outperforms KNN baseline |
| Scale | Mini project | Full B.Tech thesis + final report |

---

## 🧠 Methodology

### 1. Heuristic Trajectory Construction
A novel algorithm reconstructs complete, spatially coherent taxi trajectories from sparse, noisy GPS coordinate sequences, filling gaps that GPS dead zones and irregular sampling create.

```
Sparse GPS points (irregular intervals)
    → Heuristic gap-filling (speed constraints + road network geometry)
    → Reconstructed dense trajectory
    → Feature extraction
```

### 2. Feature Engineering
Trajectory-level fraud signals extracted per trip:
- Route deviation index (actual vs. expected shortest path)
- Speed profile consistency (sudden changes indicate route manipulation)
- Distance ratio: metered estimate vs. GPS-measured distance
- Temporal features: pickup/dropoff time, trip duration
- Spatial features: origin-destination pair risk scores

### 3. Ensemble Classifiers

**AdaBoost:** Sequentially weights misclassified examples, effective at learning subtle decision boundaries where fraud and legitimate patterns overlap.

**XGBoost:** Gradient-boosted decision trees with regularisation, handles high-dimensional trajectory features robustly, providing feature importance scores for interpretability.

```
Engineered Features
    → AdaBoost Classifier ─┐
    → XGBoost Classifier  ─┴─► Fraud / Legitimate Label
                               + Feature Importance
```

---

## 📁 Report

The full thesis report is available in this repository:  
📄 `PROJECT_FINAL_REPORT.pdf`

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Scikit-learn | AdaBoost, preprocessing, evaluation |
| XGBoost | Gradient boosted classifier |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib / Seaborn | Visualisations |
| IDLE | Development environment |
| Tkinter | GUI (demo application) |

---

## 🔗 Related Work

This thesis is the advanced successor to:  
⬅️ **[Fiddle Tour, KNN (Mini Project)](https://github.com/ramyasp64/fiddle-tour-knn)**, the foundational published study

---

## 👩‍💻 Author

**Ramya Subramanian Porselva Bharathi**  
B.Tech Information Technology · National Engineering College, India (First-Class Distinction · CGPA 8.65/10.0)  
[LinkedIn](https://www.linkedin.com/in/ramya_sp) · [GitHub](https://github.com/ramyasp64)
