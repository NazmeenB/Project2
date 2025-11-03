# Global Development Measurement Clustering Project

## Overview
This project uses unsupervised machine learning to cluster countries based on diverse development indicators. By leveraging **PCA, K-Means Clustering, and an interactive Streamlit app**, the project enables users to explore country profiles, compare global trends, and predict development status (Developed, Developing, Under Developed) using real-world data.

## Dataset
- **File:** World_development_mesurement.csv
- **Description:** Contains country-level features: birth rate, CO2 emissions, GDP, health expenditures, mortality rates, internet and mobile usage, population breakdowns, and tourism stats.
- **Purpose:** Analyze global development patterns and group countries with similar profiles.

## Tools and Technologies
- **Python** (Pandas, NumPy, Matplotlib, Seaborn)
- **Scikit-learn** (PCA, KMeans, MinMaxScaler, KNNImputer)
- **Streamlit** (for interactive deployment)
- **Jupyter Notebook** (for prototyping and analysis)

## Steps

1. **Data Loading and Cleaning**
   - Read the global development CSV file.
   - Handled missing values using KNN and mean/mode imputation.
   - Converted columns to appropriate numeric types; cleaned string-based and currency columns.
   - Dropped columns with excessive missing data (Business Tax Rate, Ease of Business, etc.).

2. **Feature Engineering**
   - Identified and handled outliers using IQR, capping, and winsorization.
   - Performed scaling with MinMaxScaler.
   - Encoded categorical variables (countries).

3. **Dimensionality Reduction**
   - Applied **Principal Component Analysis (PCA)** to reduce feature space and enable intuitive visualization.

4. **Clustering**
   - Ran **K-Means clustering** to group countries into development clusters.
   - Evaluated clustering results using metrics: Silhouette Score, Calinski-Harabasz Index, Davies-Bouldin Index.

5. **Model Serialization**
   - Saved pipelines (scaler, PCA, and clustering model) for deployment.

6. **Interactive Streamlit Application**
   - Built a **Streamlit UI** where users input country indicators and receive a prediction for their development cluster.
   - Provided sidebar controls for country selection and custom values; immediate display of cluster result (Developed, Developing, Under Developed).
   - Presented global averages and visual comparisons for key metrics (GDP, tourism, population).

7. **Presentation**
   - Project can be summarized in a PPT (create as needed) illustrating workflow, EDA findings, clustering logic, and real-world implications.

## Results

- The app successfully clusters countries—and provides human-readable cluster labels—based on combined social, economic, and demographic factors.
- Key insights include:
  - Which indicators most drive cluster assignment.
  - How individual countries compare to global averages on key development metrics.
  - Offers a live, interactive tool for non-technical decision-makers.
