# Robust Statistics -- Automated Anomaly Detection
## Objective
To implement and evaluate automated anomaly detection methodologies on highly skewed economic data to distinguish genuine structural outliers from artificial measurement errors.
## Methodology
- Computed robust vs. non-robust summary statistics (mean, median, trimmed mean, std, IQR, MAD) on California Housing data (20,640 obs)
- Implemented Tukey Fences manually to flag price outliers
- Applied Isolation Forest for multivariate anomaly detection
- Compared Tukey vs. IF results and found they flag different observations
- Ran a contamination experiment showing robust measures survive 5% corruption
## Key Findings
- Non-robust statistics fail on skewed economic data, while robust metrics successfully identify the center and spread of the distribution without being dragged by the extreme right tail.
- Univariate anomaly detection (Tukey Fences) strictly flags one-dimensional extremes, while multivariate algorithmic detection (Isolation Forest) identifies complex structural anomalies that look normal in isolation.
- Mean shifted by 67.1% after contamination; median shifted by only 3.6%.
