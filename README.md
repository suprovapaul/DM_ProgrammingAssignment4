# DM_ProgrammingAssignment4

This notebook contains the solution for Programming Assignment 4.  
The goal is to perform clustering using features extracted from a pretrained ResNet18 model.

## Steps in the Notebook

- Upload and unzip the image dataset used in previous assignments.
- Load the dataset using ImageFolder and apply resizing and normalization.
- Extract 512-dimensional features from the last convolution layer of ResNet18.
- Reduce the feature dimension to 2D using PCA.
- Run all required clustering methods:
  - KMeans (random)
  - KMeans (k-means++)
  - Bisecting KMeans
  - Spectral Clustering
  - DBSCAN (eps = 0.5, min_samples = 5)
  - Agglomerative (single, complete, average, ward)
- Compute evaluation metrics:
  - Fowlkes–Mallows index
  - Silhouette score
- Rank the clustering methods based on both metrics.
- Display FM and Silhouette scores for all methods.

## Dataset

Used a 4-class dataset: **New_Dataset_CNN** (buildings, forest, glacier, sea).

## Plotting

- PCA 2D plots are included for all clustering methods.
- All plots use the same color pattern, and cluster labels are aligned with the true labels.
- These visualizations show which methods form clear four-cluster structures and where DBSCAN fails due to noise.
