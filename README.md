# Retail Customer Clustering

This project uses the UCI Online Retail dataset to group customers into simple segments based on their buying behavior.

The notebook compares two clustering methods:

- **K-Means**: puts every customer into a fixed number of groups
- **DBSCAN**: finds dense groups and leaves unusual customers as noise

## What the notebook does

1. Loads the online retail transaction data
2. Creates a `Total_Bill` value for each purchase line
3. Builds customer-level features such as:
   - total spend
   - first and last purchase date
   - purchase interval
   - most common country
   - most common item code
4. Runs **K-Means** clustering on spend
5. Uses the elbow method to help choose the number of clusters
6. Runs **DBSCAN** on spend and purchase interval
7. Calculates a silhouette score for the DBSCAN result
8. Visualizes and summarizes the clusters

## Files

- [`retail_customer_clustering.ipynb`](./retail_customer_clustering.ipynb) - main notebook

## Requirements

You will need:

- Python 3.10+
- `pandas`
- `scikit-learn`
- `matplotlib`
- `openpyxl` for reading the Excel file from the UCI dataset

## How to run

1. Open the notebook in Jupyter Notebook, JupyterLab, or VS Code.
2. Run the cells from top to bottom.
3. Make sure you have internet access, because the dataset is loaded directly from the UCI website.

If you need to install the libraries, use:

```bash
pip install pandas scikit-learn matplotlib openpyxl
```

## About the data

The notebook uses the UCI Online Retail dataset, which contains transaction records from an online store. Each row is a purchase line, not a customer summary, so the notebook groups rows by `CustomerID` before clustering.

## Results

You should expect:

- one large group of typical customers
- a few smaller groups of higher-spending customers
- some unusual customers marked as noise by DBSCAN

## Notes

- The notebook is designed to be easy to follow and beginner-friendly.
- K-Means is useful, but it can force outliers into clusters.
- DBSCAN is often better for skewed retail spending data because it can ignore unusual points.

# Retail-Customer-Segmentation-using-K-Means-and-DBSCAN
