# Neural Correlation Analysis - Summary Report

Date: 2025-03-04 00:07:28

Dataset Overview:
- Total neurons analyzed: 256
- Number of sessions: 4
- Number of scans: 6

## Correlation Statistics

### Overall Correlations:
- RNN Correlation with gOSI: r = -0.020, p = 7.493e-01 (Not significant)
- RNN Correlation with volume: r = -0.003, p = 9.607e-01 (Not significant)
- RNN Correlation with pref_ori_norm: r = 0.085, p = 1.753e-01 (Not significant)

### Session-Specific Findings:
- Session 4 (n=56): RNN-gOSI correlation = -0.253, p = 6.033e-02 (Not significant)
- Session 5 (n=45): RNN-gOSI correlation = 0.105, p = 4.919e-01 (Not significant)
- Session 6 (n=113): RNN-gOSI correlation = 0.061, p = 5.242e-01 (Not significant)
- Session 7 (n=42): RNN-gOSI correlation = -0.029, p = 8.555e-01 (Not significant)

## Linear Regression Results

### RNN Correlation vs gOSI:
- Slope: -0.013
- Intercept: 0.294
- R²: 0.000
- p-value: 7.493e-01

### RNN Correlation vs Volume:
- Slope: -0.805
- Intercept: 311.292
- R²: 0.000
- p-value: 9.607e-01

## Feature Importance for Predicting RNN Correlation
- Model performance: R² = -0.153, RMSE = 0.262

### Relative Feature Importance:
- gDSI: 0.250
- cc_abs: 0.215
- pref_ori_norm: 0.201
- gOSI: 0.179
- volume: 0.154

## Cluster Analysis Results
- Optimal number of clusters: 7
- Number of neurons in each cluster:
  - Cluster 0: 61 neurons
  - Cluster 1: 100 neurons
  - Cluster 2: 95 neurons

### ANOVA Results for Differences Between Clusters:
- corrn: F = 152.605, p = 3.349e-44 (Significant)
- gOSI: F = 2.580, p = 7.778e-02 (Not significant)
- volume: F = 6.508, p = 1.754e-03 (Significant)
- pref_ori_norm: F = 323.642, p = 1.844e-70 (Significant)

## Bootstrap Confidence Intervals

### RNN Correlation vs gOSI:
- Observed correlation: -0.020
- 95% CI: [-0.143, 0.105]

### RNN Correlation vs Volume:
- Observed correlation: -0.003
- 95% CI: [-0.123, 0.121]

## Key Interpretations
- No significant overall relationship was found between orientation selectivity (gOSI) and RNN correlation, suggesting that the RNN's performance is not systematically affected by a neuron's orientation tuning strength.
- Neuron volume does not significantly predict RNN correlation, suggesting that physical size is not a major determinant of how well the RNN can model a neuron's responses.
- gDSI was identified as the most important feature for predicting RNN correlation, indicating its particular relevance to the RNN's performance in modeling neural responses.
- Cluster analysis identified distinct subpopulations of neurons with significantly different characteristics, suggesting functional heterogeneity in how neurons relate to the RNN model.