# Coral-Anomaly-Detection

Unsupervised anomaly detection on deep-sea coral distrubtions using enviornmental ocean data from NOAA and World Ocean Atlas.

## Overview
Deep-sea corals play a critical role in marine ecosystems but are highly sensitive to environmental change. Detecting anomalous occurrences is therefore essential for identifying species or habitats under stress. However, anomaly detection in coral data is challenging due to sparsity and limited labeled observations. This project applies unsupervised machine learning techniques to identify unusual coral occurrences based on oceanographic conditions.

## Data Sources
- NOAA Deep-Sea Coral Research Dataset: https://www.kaggle.com/datasets/noaa/deep-sea-corals
- World Ocean Atlas 2023 (temperature, salinity, oxygen): https://www.ncei.noaa.gov/access/world-ocean-atlas-2023/

## Methodology

### Feature Engineering
- Spatial grid alignment
- Depth matching to WOA levels
- Log transformation of depth

### Models
- Mahalonabis Distance (baseline)
- Isolation Forest
- One-Class SVM

### Evaluation:
- Jaccard similartiy for model agreement
- Confidence tiers:
    - High: all models agree
    - Medium: two models agree
    - Low: one model flags anomaly
 
## Results
- Isolation Forest and One-Class SVM (strongest models) show ~57% agreement
- High-confidence aomalies occur near water mass boundaries

## Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- Seaborn, matplotlib

