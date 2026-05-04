# Neural Correlation Analysis - Summary Report

Date: 2025-03-04 01:20:18

Dataset Overview:
- Total neurons analyzed: 8458
- Number of sessions: 4
- Number of scans: 6

## Correlation Statistics

### Overall Correlations:
- RNN Correlation with gOSI: r = 0.081, p = 1.012e-13 (Significant)
- RNN Correlation with volume: r = 0.038, p = 5.505e-04 (Significant)
- RNN Correlation with pref_ori_norm: r = 0.048, p = 1.107e-05 (Significant)

### Session-Specific Findings:
- Session 4 (n=986): RNN-gOSI correlation = 0.040, p = 2.108e-01 (Not significant)
- Session 5 (n=1947): RNN-gOSI correlation = 0.182, p = 5.900e-16 (Significant)
- Session 6 (n=4171): RNN-gOSI correlation = 0.117, p = 2.878e-14 (Significant)
- Session 7 (n=1354): RNN-gOSI correlation = 0.098, p = 3.009e-04 (Significant)

## Linear Regression Results

### Correlation vs gOSI:
- Slope: 0.078
- Intercept: 0.228
- R²: 0.007
- p-value: 1.012e-13

### Correlation vs Volume:
- Slope: 16.874
- Intercept: 298.378
- R²: 0.001
- p-value: 5.505e-04

## Feature Importance for Predicting RNN Correlation
- Model performance: R² = -0.030, RMSE = 0.152

### Relative Feature Importance:
- cc_abs: 0.228
- gOSI: 0.203
- volume: 0.193
- pref_ori_norm: 0.189
- gDSI: 0.187

## Cluster Analysis Results
- Optimal number of clusters: 4
- Number of neurons in each cluster:
  - Cluster 0: 1638 neurons
  - Cluster 1: 1349 neurons
  - Cluster 2: 3100 neurons
  - Cluster 3: 2371 neurons

### ANOVA Results for Differences Between Clusters:
- corrn: F = 360.217, p = 3.663e-220 (Significant)
- gOSI: F = 2940.708, p = 0.000e+00 (Significant)
- volume: F = 2963.527, p = 0.000e+00 (Significant)
- pref_ori_norm: F = 3127.807, p = 0.000e+00 (Significant)

## Bootstrap Confidence Intervals

### CNN Correlation vs gOSI:
- Observed correlation: 0.081
- 95% CI: [0.059, 0.103]

### CNN Correlation vs Volume:
- Observed correlation: 0.038
- 95% CI: [0.016, 0.060]

## Key Interpretations
- Neurons with higher orientation selectivity (gOSI) tend to have stronger correlations, suggesting that the RNN model more effectively captures the responses of orientation-selective neurons.
- Larger neurons tend to have stronger RNN correlations, possibly because they provide stronger, more reliable signals that are easier for the RNN to model.
- cc_abs was identified as the most important feature for predicting RNN correlation, indicating its particular relevance to the RNN's performance in modeling neural responses.
- Cluster analysis identified distinct subpopulations of neurons with significantly different characteristics, suggesting functional heterogeneity in how neurons relate to the RNN model.