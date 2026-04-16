# windmill-pitch-prediction
Extended ML implementation of IEEE ICEMCE 2023 paper on windmill pitch prediction. Built on the published research with updates: XGBoost model, 10-min data resolution, 250kW turbine spec, and 26 engineered features. Achieves 96% accuracy with 8.6%→2.3% error reduction and +21% energy gain.


# 🌬️ Windmill Pitch Prediction & Error Correction with Adaptive Control

**Author:** Rohit Suryaa Saravanan  
**Institution:** SRM Institute of Science and Technology, Chennai, India  
**Based on:** IEEE ICEMCE 2023 Paper  
**DOI:** [10.1109/ICEMCE57940.2023.10433983](https://doi.org/10.1109/ICEMCE57940.2023.10433983)

---

## 📌 About This Project

This notebook is an **extended and iterative implementation** of the following published IEEE paper:

> *"Windmill Pitch Prediction And Error Correction With Adaptive Control And Current Generation Analysis Using Data Analysis"*  
> M.S.Minu, Sharan S, **Rohit Suryaa S**, Jovan Titus J  
> 2023 International Conference on Energy, Materials, and Communication Engineering (ICEMCE), Madurai, India

The original paper established the core methodology and reported results using a simulation-based adaptive control system. After publication, several **iterations and improvements** were made to this implementation to make it more robust, reproducible, and scalable using modern machine learning techniques.

---

## 🔄 Updates from the Original Paper

| Aspect | Original Paper | This Implementation |
|--------|---------------|---------------------|
| Data interval | Hourly samples | **10-minute intervals** (higher resolution) |
| Turbine spec | General wind turbine | **3 × 250 kW machines** (real field spec) |
| Prediction model | Rule-based adaptive control simulation | **XGBoost ML model** |
| Error correction | Adaptive control rules | **Data-driven residual corrector** |
| Feature set | Pitch angle + power output | **26 engineered features** (lag, rolling, temporal, physics) |
| Validation | Results reported in paper | **Fully reproduced programmatically** |

---

## 📊 Key Results (Consistent with Paper)

| Metric | Existing System | Proposed System |
|--------|----------------|-----------------|
| Forecasting Error Rate | 8.6% | **2.3%** |
| Prediction Accuracy | — | **96%** |
| Energy Output (sample day) | 841.54 kWh | **1019.41 kWh** |
| Energy Gain | — | **+177.88 kWh (+21%)** |
| Turbines | 3 × 250 kW | 3 × 250 kW |
| Data Duration | 6 months | 6 months |

---

## 🏗️ System Architecture (from paper)

The 5-layer architecture described in the paper is implemented as follows:

- **Layer 1 — Data Collection:** Synthetic simulation of 3 × 250kW turbine sensors (wind speed, pitch angle, rotor RPM, power output, temperature)
- **Layer 2 — Data Preprocessing:** Data cleaning + 26 engineered features (lag features, rolling statistics, temporal encoding, physics interactions)
- **Layer 3 — Analysis & Prediction:** XGBoost pitch angle prediction model + residual error correction layer
- **Layer 4 — Control & Optimization:** Adaptive corrector trained on prediction residuals, power output simulation
- **Layer 5 — Reporting & Feedback:** Visualisations, model comparison, energy output improvement charts

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Language | Python 3.10+ |
| ML Models | XGBoost, Scikit-learn |
| Data Processing | Pandas, NumPy |
| Visualisation | Matplotlib, Seaborn |
| Environment | Jupyter Notebook / Google Colab |

---

## 📂 Repository Structure ##

windmill-pitch-prediction/
│
├── windmill_pitch_prediction.ipynb   # Main notebook
└── README.md                         # This file

---

## 📖 Citation

If you use or reference this work, please cite the original paper:


---

## 📬 Contact

**Rohit Suryaa Saravanan**  
📧 Rohitsuryaas21@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/rohit-suryaa-saravanan-197b33303/)  
📍 Fulda, Germany

