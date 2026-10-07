# Product Clustering for Retail and Warehouse Sales

K-Means segmentation of products by sales behaviour across retail and warehouse channels. Built as part of a data science On Job Training program, using a public dataset.

**Shubham Adate** | [LinkedIn](https://www.linkedin.com/in/adate-shubham) | [GitHub](https://github.com/shubhamadatework-git)

## Problem
Distributors manage thousands of products with very different demand patterns. Grouping similar products helps identify fast movers, slow movers, warehouse-dominant items and transfer-heavy items.

## Data
- Monthly sales and movement records by item: year, month, supplier, item code, item type, retail sales, retail transfers and warehouse sales
- Source: [Warehouse and Retail Sales (Montgomery County, MD open data)](https://data.montgomerycountymd.gov/d/v76h-r7br). See `data/README.md`.

## Approach
1. Cleaning and feature engineering
2. Aggregated the data to product level and selected features
3. Scaled features and chose the number of clusters with the elbow method and silhouette analysis
4. Trained the final K-Means model and visualised it with PCA
5. Profiled each cluster and compared clusters against product categories

## Results
| Cluster quality metric | Value |
|---|---|
| Silhouette score | 0.764 |
| Davies-Bouldin index | 0.713 (lower is better) |
| Calinski-Harabasz score | 18,548 |

The clusters separate products with distinct demand patterns, which supports inventory management, demand forecasting and distribution decisions.

## Limitations and future work
- Seasonality, promotions and holidays were not considered
- Pricing and profit margins were not analysed
- Future work: seasonal demand analysis, time-series demand forecasting and an automated inventory optimisation model

## Run it
```bash
pip install -r requirements.txt
jupyter notebook product-clustering-retail-warehouse-sales.ipynb
```

**Tech:** Python, pandas, NumPy, scikit-learn, kneed, seaborn, matplotlib
