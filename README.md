# Gazepoint — Eye-Tracking Analysis of UI Animations

**Investigating how interface animations affect users' visual attention through eye-tracking data, statistical analysis, and machine learning.**

## Project Overview

Gazepoint is a research-oriented data science project that analyzes eye-tracking recordings collected during user interaction with animated interfaces.

The goal is to examine differences in visual attention when animations are active (ON) versus inactive (OFF), and to investigate how animation properties such as direction, easing, and delay relate to gaze behavior.

The analysis combines data preprocessing, feature engineering, statistical testing, and machine learning.

## Research Questions

- How does visual attention differ between animated and non-animated interface states?
- Which eye-tracking features are associated with different animation conditions?
- Can machine learning distinguish animation ON and OFF states using gaze-derived features?

## Methodology

### 1. Data Processing

Eye-tracking recordings are aligned with participant sessions and task information. The preprocessing notebooks organize fixation and gaze data and associate observations with experimental conditions.

### 2. Feature Engineering

The project extracts and analyzes features related to:

- Fixation frequency, duration, and spatial behavior
- Gaze movement and saccade characteristics
- Pupil measurements
- Areas of Interest (AOIs)
- Temporal changes in eye-tracking behavior

Several notebooks aggregate observations into short time windows to study changes over time.

### 3. Statistical Analysis

The project investigates differences between animation conditions using statistical methods including:

- Mann–Whitney U and Kruskal–Wallis tests
- Spearman correlation
- Effect-size calculations
- Statistical visualizations and exploratory analysis

### 4. Machine Learning

Logistic Regression and Random Forest classifiers are used to investigate whether eye-tracking features can distinguish animation ON and OFF conditions.

The modeling notebooks include:

- Feature preprocessing and standardization
- Group-aware cross-validation
- Hyperparameter tuning
- ROC-AUC, precision-recall, and F1-based evaluation
- Feature importance analysis

Exploratory notebooks also investigate dimensionality reduction and clustering using PCA and K-Means.

## Technologies

| Area | Tools |
| --- | --- |
| Programming | Python |
| Data Processing | pandas, NumPy |
| Machine Learning | scikit-learn |
| Statistical Analysis | SciPy, statsmodels |
| Visualization | Matplotlib, Seaborn |
| Development | Jupyter Notebook |

## Repository Structure

| Path | Purpose |
| --- | --- |
| `all_tasks.csv` | Task and session metadata |
| `notebooks/03_all_participants_data_cleaning.ipynb` | Cleaning and merging participant recordings |
| `notebooks/labelling.ipynb` | Labelling animation ON and OFF periods |
| `notebooks/features_v3.ipynb` | Eye-tracking feature engineering |
| `notebooks/04_all_participants_stats.ipynb` | Statistical comparison of animation conditions |
| `notebooks/LR_RF.ipynb` | Logistic Regression and Random Forest experiments |
| `notebooks/improving models/` | Additional modeling and task-specific experiments |
| `notebooks/older notebooks/` | Earlier exploratory analyses |

## Getting Started

The project uses Python and Jupyter Notebook.

Install the main analysis libraries:

```bash
python -m pip install pandas numpy scipy statsmodels scikit-learn matplotlib seaborn jupyter
```

The notebooks currently contain machine-specific file paths and reference intermediate data files that are not all included. Before reproducing the experiments, configure the input paths and obtain appropriately authorized datasets.

This repository documents an exploratory research workflow rather than a fully automated application.

## Limitations and Future Improvements

- Replace absolute local file paths with portable paths.
- Add a reproducible environment and dependency file.
- Consolidate experimental notebooks into a clearer workflow.
- Improve documentation of datasets, experimental conditions, and validated results.
- Ensure that participant-level eye-tracking recordings are shared only with appropriate permission.

## Author

**Ferola Hima**

MSc Computer Science — Sapienza University of Rome

BSc Applied Computer Science and Artificial Intelligence — Sapienza University of Rome
