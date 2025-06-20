# ADL Clustering Project

## Overview

This project presents an unsupervised learning approach to recognize Activities of Daily Living (ADLs) using binary sensor data. By leveraging clustering techniques such as K-Means and K-Modes, the study aims to detect hidden activity patterns without relying on labeled data during model training. The approach explores the capability of sensor-triggered binary datasets to reveal meaningful clusters representing distinct daily activities.

## Features

- Preprocessing of binary sensor data from two users (OrdonezA and OrdonezB).
- Dataset cleaning, merging, and handling of missing values using pandas.
- Feature engineering and encoding of categorical data (Location, Place, Type, Start/End Time).
- Implementation of K-Means and K-Modes clustering.
- Dimensionality reduction using PCA for visualization.
- Cluster performance evaluation using metrics:
  - Homogeneity
  - Completeness
  - V-Measure
  - Silhouette Coefficient
  - Confusion Matrix
- Comparison of encoded data using both Label Encoding and One-Hot Encoding methods.
- Visual cluster plots for both models using matplotlib and seaborn.

## Installation

Make sure Python and essential libraries are installed. You can use Anaconda for easy environment management.

````
# Clone the repository
git clone https://github.com/yourusername/ADL-Clustering.git
cd ADL-Clustering

# Create and activate a virtual environment (optional but recommended)
python -m venv adl-env
source adl-env/bin/activate  # On Windows: adl-env\Scripts\activate

# Install the required packages
pip install -r requirements.txt

````

## Usage

## Dataset

The Ordonez dataset consists of two users’ sensor-triggered activity logs spanning 35 days:
	•	OrdonezA.txt
	•	OrdonezB.txt

After pre-processing and merging, the features used for clustering include:
Location, Place, Type, Start Time, End Time.
The Activity label is only used for evaluation, not training.

## Running the Code

You can run the analysis through a Jupyter Notebook or Python script. Steps include:
	1.	Data Cleaning and Preprocessing
	2.	Feature Transformation (encoding, scaling)
	3.	Clustering using KMeans and KModes
	4.	Dimensionality Reduction (PCA)
	5.	Visualization
	6.	Evaluation

```
# Launch Jupyter Notebook
jupyter notebook

# Open and run notebook: ADL_Clustering.ipynb

```
## Models

## KMeans Clustering
	•	Number of Clusters: 11
	•	Encoding Method: Label Encoding
	•	StandardScaler used for normalization
	•	PCA used for 2D visualization

## KModes Clustering
	•	Number of Clusters: 11
	•	Categorical encoding using kmodes package
	•	Evaluation via confusion matrix and cluster centroids

## Evaluation Metrics

| Metric                | Value  |
|-----------------------|--------|
| Homogeneity           | 0.092  |
| Completeness          | 0.051  |
| V-Measure             | 0.066  |
| Accuracy              | 0.015  |
| Silhouette Coefficient| 0.90   |

Although the Silhouette Coefficient suggests clear separation, the homogeneity and completeness metrics indicate poor clustering alignment with the actual activity labels. This reflects the challenges in applying unsupervised techniques on real-world noisy sensor data.

## Visualizations
- Cluster Scatter Plots (PCA-reduced) to view cluster separations.
- Confusion Matrix to compare predicted clusters with actual activity labels.
- Cluster Centroids to understand cluster composition in KModes.

## Experimental Environment
- Platform: MacBook Pro (Apple M1)
- IDE: Jupyter Notebook via Anaconda
- Libraries used:
  - pandas, numpy
	- sklearn, kmodes
  - matplotlib, seaborn

## Key Learnings
- Handling missing values is crucial to avoid bias and misclustering.
- Unsupervised learning requires deep understanding of data structure since no labels are available during training.
- Though supervised models may yield better accuracy when labels are present, unsupervised clustering reveals hidden patterns in unlabeled datasets.
