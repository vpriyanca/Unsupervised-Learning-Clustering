# ADL Clustering Project

## Overview

This project presents an unsupervised learning approach to recognize Activities of Daily Living (ADLs) using binary sensor data. By leveraging clustering techniques such as K-Means and K-Modes, the study aims to detect hidden activity patterns without relying on labeled data during model training. The approach explores the capability of sensor-triggered binary datasets to reveal meaningful clusters representing distinct daily activities.

## Features
- Preprocessing of binary sensor data from two users (OrdonezA and OrdonezB).
- Dataset cleaning, merging, and handling of missing values using pandas.
- Feature engineering and encoding of categorical data (Location, Place, Type, Start/End Time).
- Implementation of K-Means and K-Modes clustering.
- Dimensionality reduction using PCA for visualization.
- Cluster performance evaluation using metrics like:
  -- Homogeneity
  -- Completeness
  -- V-Measure
  -- Silhouette Coefficient
  -- Confusion Matrix
- Comparison of encoded data using both Label Encoding and One-Hot Encoding methods.
- Visual cluster plots for both models using matplotlib and seaborn.
