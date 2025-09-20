# Robust Forecasting of Greenhouse Gas Emissions

[![Paper](https://img.shields.io/badge/Paper-PDF-blue)](./CISP_BMEI_2025_Yiteng.pdf)\
[![Dataset](https://img.shields.io/badge/Data-IPR%20Station-green)](https://meta.icos-cp.eu/objects/oCyeHuFmx9RcyUtZ7fM1C2i7)

## 📖 Introduction

This repository provides the official implementation of the paper:\
**"Robust Forecasting of Greenhouse Gas Emissions with Change Point and
Anomaly Detection"** (CISP-BMEI 2025).

Greenhouse gas (GHG) time series are often affected by anomalies and
structural breaks due to sensor errors, calibration periods, or episodic
meteorological events.\
Our framework integrates:
- **Anomaly detection** (hybrid STL decomposition + Isolation Forest)
- **Change point detection** (PELT algorithm)
- **Robust weighting strategies** (anomaly down-weighting, weighted
Huber loss)
- **Forecasting models**: Seasonal Naive, SARIMAX, and GRU

The results demonstrate that robustness mechanisms **substantially
improve statistical models (Naive, SARIMAX)**, while deep learning
models such as GRU are inherently more robust.

------------------------------------------------------------------------

## 🚀 Features

-   Data preprocessing for CO₂ monitoring datasets
-   Hybrid anomaly detection (statistical + ML-based)
-   Change point detection with regime encoding
-   Robust training strategies for time series models
-   Reproducible experiments with multiple baselines

------------------------------------------------------------------------

## 📂 Repository Structure

    ├── data/             # Scripts or links for dataset preparation
    ├── models/           # Seasonal Naive, SARIMAX, GRU implementations
    ├── utils/            # Preprocessing, anomaly & change point detection
    ├── experiments/      # Training & evaluation scripts
    ├── results/          # Forecasting results, figures & logs
    └── CISP_BMEI_2025_Yiteng.pdf   # Paper PDF

------------------------------------------------------------------------

## 📈 Results

  Model            Robustness   MAE     RMSE    MAPE (%)
  ---------------- ------------ ------- ------- ----------
  Seasonal Naive   Before       12.25   16.04   2.79
  Seasonal Naive   After        8.05    11.09   1.80
  SARIMAX          Before       7.64    9.41    1.73
  SARIMAX          After        7.00    9.10    1.58
  GRU              Before       2.95    4.50    0.66
  GRU              After        3.09    4.75    0.69

Figures and plots are available in the `results/` folder.

------------------------------------------------------------------------

## 📚 Citation

If you use this code in your research, please cite:

``` bibtex
@inproceedings{zhang2025robust,
  title={Robust Forecasting of Greenhouse Gas Emissions with Change Point and Anomaly Detection},
  author={Zhang, Yiteng and Pakrashi, Arjun and Dev, Soumyabrata},
  booktitle={17th International Congress on Image and Signal Processing, BioMedical Engineering and Informatics (CISP-BMEI)},
  year={2025}
}
```

------------------------------------------------------------------------

## Acknowledgements

-   CO₂ data from the [IPR monitoring station
    (ICOS)](https://meta.icos-cp.eu/objects/oCyeHuFmx9RcyUtZ7fM1C2i7)
-   Anomaly detection with **Isolation Forest** (Scikit-learn)
-   Change point detection using **PELT algorithm**
