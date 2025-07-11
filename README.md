# 🌧️ High-Resolution Rainfall Prediction Using GFS Reanalysis & Machine Learning

This project focuses on classifying high rainfall days over the Mumbai-Goa region using NOAA GFS reanalysis data (2019–2024). The goal is to predict whether a day will fall into the top 15% of rainfall based on spatial-temporal atmospheric features.

## 🗂️ Dataset
- GFS data at 0.25° × 0.25° resolution
- Initialization Times: 00Z (previous day), 06Z, 12Z, 18Z
- Variables: Precipitation Rate, Precipitable Water, Temperature, Pressure, Relative Humidity
- Labels: Binary (top 15% rainfall days = 1)

## 🛠️ Feature Engineering
- Daily feature vector from multi-init 3-hourly forecasts
- Near-point mapping and IDW interpolation
- Attempted Kriging (excluded due to compute limitations)

## 🤖 Models
- **Baselines**: Random Forest, XGBoost
- **Advanced Architectures**: CNN, LSTM, Transformer
- **Graph-Augmented**: GAT-LSTM, GCN-CNN, etc.

## 📈 Evaluation Metrics
- Hit Rate, False Alarm Rate, Precision, Recall, Accuracy, F1-score

## 📂 Structure
- `notebooks/`: Training and evaluation notebooks
- `results/`: Plots and metric summaries
- `data/`: Placeholder (raw data not included due to size)

## 🚧 Future Work
- GPU-optimized Kriging for spatial interpolation
- Transfer learning from MetNet/FourCastNet
- More robust temporal modeling

---

**Note**: This is a self-initiated project. Broad guidance was sought from Prof. Manjesh Hanawal.
