# Online Retail Customer Segmentation using K-Means Clustering

3D visualization of customer segments based on Recency, Frequency, and Monetary (RFM) value.

---

## Project Overview

This project performs customer segmentation on the Online Retail Dataset using K-Means clustering. The goal is to group customers into meaningful segments based on their purchasing behavior, enabling targeted marketing strategies.

We follow a complete data science pipeline:
1. Data Cleaning
2. Feature Engineering (RFM)
3. Outlier Removal
4. Standardization
5. K-Means Clustering
6. Visualization (2D & 3D)

---

## Dataset

- Source: UCI Machine Learning Repository – Online Retail
- File: data/Online Retail Dataset.xlsx
- Description: Transnational dataset containing transactions from 01/12/2010 to 09/12/2011 for a UK-based online retailer.

> Note: The dataset is included in the data/ folder. For larger versions or updates, refer to the UCI link.

---

## Key Steps Explained

Data Cleaning: Remove canceled orders (Invoice starting with 'C'), invalid quantities/prices, and missing Customer ID

RFM Calculation:
- Recency: Days since last purchase
- Frequency: Number of transactions
- Monetary: Total spend (Quantity × UnitPrice)

Outlier Removal: Using IQR method to reduce distortion in K-Means
Standardization: StandardScaler → all features on same scale
Elbow Method: Determine optimal K (number of clusters)
K-Means: Cluster customers into K groups
Visualization: 3D scatter plot + 2D pair plots

---

## Results

- Optimal Clusters (K=4) based on Elbow Method
- Segments Identified:
  1. High-Value Recent Buyers (VIPs)
  2. Loyal but Inactive (At-Risk)
  3. Low-Value Frequent (Budget Shoppers)
  4. New or One-Time (Prospects)

> See images/ for visualizations.
