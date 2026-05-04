# Introduction

This is some of my data visualization work from when I was being onboarded as an undergraduate intern at the Abbasi Lab at UCSF. I later went on to create ensemble models between the different RNN and CNN architectures on the MICRONs dataset. 

This work was based off the [MICRoNs](https://www.microns-explorer.org/) dataset.

The different correlational values visualized here are corresponding to predicted correlational scores of neuron firing patterns. 
These neural networks were trained off experimental data collected from the primary visual cortex from mice, with visual stimulus being quantified by sodium-fluorescence measurements. 
Visual enccoded data was inputted as training data, with correlational outputs as the end result. 

# Neuroglancer

Within `NeuroglancerDataExp.ipynb` you will find initial exploratory data analysis within the following three categories:
### Exploratory
- Correlation distributions by session (boxplots + stripplots)
- Scatter of correlation vs. cortical depth
- Heatmap of mean correlation by depth bin × session
- Boxplots of correlation by AIBS cell type

### Statistical
- Pearson correlation matrices + p-value matrices (lower-triangle heatmaps)
- Joint scatter/KDE plots: `correlation` vs `gOSI`, `volume`, `pref_ori`
- Polar plot of mean RNN correlation by preferred orientation bin

### Clustering & Heterogeneity
- K-means on pairwise feature combinations (k=7)
- Silhouette-score optimization for k selection
- 3D K-means visualization (correlation × gOSI × volume)
- Parallel coordinates plot across clusters
- ANOVA testing for cluster separation

I also included an anatomical analysis, pertaining to the anatomical features available in the MICRoNs dataset, which merges correlation data with `allen_column_mtypes_v2.csv` for spatial analysis. This showcases:
- A 3D spatial scatter of correlation values by `pt_position`
- Different XY/XZ/YZ projection maps
- A regression model on correlation value vs neuronal volume 
- Feature importance for anatomical predictors
- K-means clustering on anatomical features + t-SNE colored by correlation