```markdown
# Online Retail Customer Segmentation using K-Means Clustering

![Project Banner](images/3d_scatter_plot.png)  
*3D visualization of customer segments based on Recency, Frequency, and Monetary (RFM) value.*

---

## Project Overview

This project performs **customer segmentation** on the [Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail) using **K-Means clustering**. The goal is to group customers into meaningful segments based on their purchasing behavior, enabling targeted marketing strategies.

We follow a complete **data science pipeline**:
1. Data Cleaning
2. Feature Engineering (RFM)
3. Outlier Removal
4. Standardization
5. K-Means Clustering
6. Visualization (2D & 3D)

---

## Dataset

- **Source**: [UCI Machine Learning Repository – Online Retail](https://archive.ics.uci.edu/dataset/352/online+retail)
- **File**: `data/Online Retail Dataset.xlsx`
- **Description**: Transnational dataset containing transactions from 01/12/2010 to 09/12/2011 for a UK-based online retailer.

> **Note**: The dataset is included in the `data/` folder (under 50MB). For larger versions or updates, refer to the UCI link.

---

## Project Structure

```
├── data/
│   └── Online Retail Dataset.xlsx
├── src/
│   └── main.ipynb                  # Complete analysis (Jupyter Notebook)
├── images/
│   ├── 3d_scatter_plot.png
│   ├── elbow_plot.png
│   └── cluster_distribution.png
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Key Steps Explained

| Step | Purpose |
|------|--------|
| **Data Cleaning** | Remove canceled orders (`Invoice` starting with 'C'), invalid quantities/prices, and missing `Customer ID` |
| **RFM Calculation** |  
- **Recency**: Days since last purchase  
- **Frequency**: Number of transactions  
- **Monetary**: Total spend (`Quantity × UnitPrice`) |
| **Outlier Removal** | Using IQR method to reduce distortion in K-Means |
| **Standardization** | `StandardScaler` → all features on same scale |
| **Elbow Method** | Determine optimal K (number of clusters) |
| **K-Means** | Cluster customers into K groups |
| **Visualization** | 3D scatter plot + 2D pair plots |

---

## Results

- **Optimal Clusters (K=4)** based on Elbow Method
- **Segments Identified**:
  1. **High-Value Recent Buyers** (VIPs)
  2. **Loyal but Inactive** (At-Risk)
  3. **Low-Value Frequent** (Budget Shoppers)
  4. **New or One-Time** (Prospects)

> See `images/` for visualizations.

---

## How to Run

1. **Clone the repo**:
   ```bash
   git clone https://github.com/yourusername/Online-Retail-Clustering.git
   cd Online-Retail-Clustering
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the notebook**:
   ```bash
   jupyter notebook src/main.ipynb
   ```

---

## Requirements

See [`requirements.txt`](requirements.txt):
```txt
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter
```

---

## Learning Source

This project is based on the excellent tutorial by **Keith Galli**:

[Watch on YouTube: Customer Segmentation with K-Means (Python)](https://www.youtube.com/watch?v=afPJeQuVeuY)

**Highly recommended** for understanding RFM, clustering, and visualization!

---

## Author

- **Your Name**
- GitHub: [github.com/yourusername](https://github.com/yourusername)

---

## License

MIT License – feel free to use, modify, and share.

---

*“Turning raw transaction data into actionable customer insights — one cluster at a time.”*
```
