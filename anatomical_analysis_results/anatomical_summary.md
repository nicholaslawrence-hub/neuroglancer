# Anatomical Data Analysis - Summary Report

Date: 2025-03-11 13:13:28

Dataset Overview:
- Total cells analyzed: 1351
- Number of cell types: 10

### Cell Type Distribution:
- Other: 550 cells (40.7%)
- L4b: 126 cells (9.3%)
- L6tall-c: 103 cells (7.6%)
- L3b: 98 cells (7.3%)
- L4a: 97 cells (7.2%)
- L4c: 83 cells (6.1%)
- L6tall-a: 82 cells (6.1%)
- L3a: 73 cells (5.4%)
- L2c: 71 cells (5.3%)
- L2b: 68 cells (5.0%)

## Volume Analysis
- Mean volume: 295.70
- Median volume: 287.72
- Volume range: 165.07 to 1073.88

### Volume by Cell Type:
- L3a: 335.27 ± 36.01 (n=73)
- Other: 317.04 ± 78.72 (n=550)
- L2c: 306.68 ± 46.15 (n=71)
- L3b: 290.18 ± 30.69 (n=98)
- L6tall-a: 282.96 ± 35.78 (n=82)

## Spatial Analysis
- Spatial extent: 38224.00 × 182624.00 × 5457.00
- Mean cell-to-cell distance: 55260.52
- Median cell-to-cell distance: 47859.52

## Cluster Analysis
- Optimal number of clusters: 2

### Cluster Sizes:
- Cluster 0: 940 cells (69.6%)
- Cluster 1: 411 cells (30.4%)

Clusters based on features: volume, x_pos, y_pos, z_pos

## Feature Importance for Predicting Cell Volume
- y_pos: 0.422
- z_pos: 0.390
- x_pos: 0.188

Prediction performance: R² = 0.252, RMSE = 52.023

## Key Correlations
- y_pos vs z_pos: r = 0.655, p = 1.565e-166 (significant)
- x_pos vs y_pos: r = 0.351, p = 1.752e-40 (significant)
- x_pos vs z_pos: r = 0.341, p = 4.893e-38 (significant)
- volume vs z_pos: r = -0.080, p = 3.356e-03 (significant)
- volume vs y_pos: r = 0.049, p = 7.363e-02 (not significant)