# Multiclass Clustering Analysis Pipeline

## Overview

This repository contains a comprehensive Python notebook for multiclass clustering analysis with advanced techniques for dataset comparison, feature engineering, and model evaluation. The pipeline implements multiple clustering algorithms, evaluates them using various metrics, and visualizes the results for easy interpretation.

## Features

- **Multiple Dataset Variants**: Compares clustering performance across four dataset variants:
  - Standard dataset
  - VIF-filtered dataset (reduced multicollinearity)
  - PCA-transformed dataset
  - UMAP-transformed dataset

- **Comprehensive Clustering Algorithms**:
  - K-Means
  - DBSCAN
  - OPTICS
  - Spectral Clustering
  - HDBSCAN
  - Gaussian Mixture Models (GMM)
  - GMSDB (Gaussian Mixture with Sparse Dirichlet prior)
  - Agglomerative Clustering
  - BIRCH

- **Advanced Evaluation Metrics**:
  - Silhouette Score
  - Davies-Bouldin Index
  - Calinski-Harabasz Index
  - Negentropy
  - Minimum cluster size ratio
  - Outlier ratio

- **UMAP Stability Analysis**: Tests UMAP transformations with different random states to ensure stable clustering results

- **Visualization**: Provides 2D UMAP visualization of the best clustering model for easy interpretation

## Requirements

- Python 3.8+
- Required packages:
  - pandas
  - numpy
  - scikit-learn
  - matplotlib
  - seaborn
  - umap-learn
  - hdbscan
  - scipy

## Installation

```bash
pip install pandas numpy scikit-learn matplotlib seaborn umap-learn hdbscan scipy
```

## Usage

1. Ensure your dataset is in CSV format with features and without a target variable
2. Place your dataset in the same directory as the notebook
3. Update the dataset path in the notebook if necessary
4. Run the notebook cells sequentially

## Pipeline Structure

1. **Data Loading and Preprocessing**:
   - Load dataset
   - Handle missing values
   - Scale features

2. **VIF Analysis**:
   - Calculate Variance Inflation Factor for features
   - Create VIF-filtered dataset

3. **Dimensionality Reduction**:
   - PCA transformation
   - UMAP transformation with stability analysis

4. **Clustering Algorithm Evaluation**:
   - Apply multiple clustering algorithms
   - Calculate evaluation metrics
   - Store results in a comprehensive summary table

5. **Best Model Selection**:
   - Identify the best clustering model based on multiple metrics
   - Analyze cluster characteristics

6. **Visualization**:
   - Create 2D UMAP visualization of clusters
   - Generate cluster distribution plots

## Results Interpretation

The notebook generates a comprehensive summary table that allows for easy comparison of clustering algorithms across different dataset variants. The best model is selected based on a combination of metrics, with special attention to:

- Silhouette Score (higher is better)
- Davies-Bouldin Index (lower is better)
- Calinski-Harabasz Index (higher is better)
- Negentropy (higher indicates better cluster separation)
- Minimum cluster size ratio (balanced clusters preferred)

## Customization

The notebook can be customized in several ways:

- Adjust the VIF threshold to control feature filtering
- Modify UMAP parameters for different dimensionality reduction results
- Change the number of clusters for applicable algorithms
- Add or remove clustering algorithms
- Customize evaluation metrics

## License

This project is available for academic and research purposes.

## Acknowledgments

This clustering pipeline was developed using state-of-the-art techniques from the data science community, with inspiration from various research papers on clustering evaluation and stability analysis.
