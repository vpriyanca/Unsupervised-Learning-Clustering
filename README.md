# ADL Clustering Project

## Overview
ADL Clustering is an unsupervised machine learning project aimed at recognizing Activities of Daily Living (ADLs) using binary sensor data. This project leverages clustering techniques (K-Means and K-Modes) along with data preprocessing, feature engineering, and visualization tools to identify hidden activity patterns without using labeled data during training.

## Features
- Data cleaning and preprocessing of binary sensor data from two users (OrdonezA and OrdonezB).
- Feature transformation and encoding of categorical fields (Location, Place, Type, Start/End Time).
- Clustering using both K-Means and K-Modes techniques.
- Dimensionality reduction using Principal Component Analysis (PCA) for visualization.
- Cluster evaluation using:
  - Homogeneity
	- Completeness
	- V-Measure
	- Silhouette Coefficient
	- Confusion Matrix
- Visual cluster plots using matplotlib and seaborn.
- Comparison of clustering performance using Label Encoding and One-Hot Encoding.

## Installation
To run the ADL Clustering project, ensure that Python is installed on your system. Using a virtual environment is recommended.
````
# Clone the repository
git clone https://github.com/yourusername/ADL-Clustering.git
cd ADL-Clustering

# (Optional) Set up a virtual environment
python -m venv adl-env
source adl-env/bin/activate  # On Windows, use `adl-env\Scripts\activate`

# Install the required packages
pip install -r requirements.txt
````

## Usage

This project is designed to analyze binary sensor data and apply unsupervised learning techniques to cluster and evaluate ADL patterns

## Data Preparation

Ensure the sensor datasets are stored in the appropriate data/ directory. The project uses:
- OrdonezA.csv: Sensor events from User A.
- OrdonezB.csv: Sensor events from User B.

The files should be cleaned, merged, and preprocessed before applying clustering techniques. Missing values should be handled carefully to avoid bias in clustering outcomes.

## Running the Code
Open the project in a Jupyter environment or your preferred Python IDE. Run the scripts or notebook (e.g., ADL_Clustering.ipynb) in sequence to:
	1.	Clean and preprocess data.
	2.	Apply feature transformation.
	3.	Train K-Means and K-Modes models.
	4.	Visualize clusters using PCA.
	5.	Evaluate performance using clustering metrics.

## Models
The project implements two clustering algorithms:
## KMeans Clustering : Applied to scaled data with PCA for visualization.
- Number of Clusters: 11
- Encoding Method: Label Encoding
- StandardScaler used for normalization
- PCA used for 2D visualization

## K-Modes: Applied to categorical data using kmodes library.
- Number of Clusters: 11
- Categorical encoding using kmodes package
- Evaluation via confusion matrix and cluster centroids

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
The following plots help in interpreting model output:
- # PCA Scatter Plots: Visual representation of clusters in reduced dimensions.
- # Confusion Matrix: To analyze how predicted clusters align with actual activity labels.
- # Cluster Centroids: To understand cluster centers in K-Modes.

## Custom Functions
Custom utility functions are included to streamline:
- Data cleaning and transformation.
- Encoding of categorical features.
- Evaluation of clustering results.
 
## Key Learnings
- Handling missing values is crucial to avoid bias and misclustering.
- Unsupervised learning requires deep understanding of data structure since no labels are available during training.
- Though supervised models may yield better accuracy when labels are present, unsupervised clustering reveals hidden patterns in unlabeled datasets.

## Contributing
Contributions to the ADL Clustering project are welcome. To contribute:
1.Fork the repository.
2.Create a new branch (git checkout -b feature-name).
3.Commit your changes.
4.Open a pull request.

For significant changes, please open an issue to discuss the proposed modification.

## Contact
- Project Owner: Priyanka Vyas
- Email: pvyas2@kent.edu

## Acknowledgments
This project is made possible with the support of the following tools and libraries:
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- kmodes
- Jupyter Notebook

A big thanks to the academic community and open-source contributors for their inspiration and resources.
