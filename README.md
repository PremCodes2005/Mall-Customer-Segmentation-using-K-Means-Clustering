# Mall Customer Segmentation (K-Means)

This project segments mall customers into meaningful groups using K-Means clustering on Age, Annual Income (k$), and Spending Score (1–100). The goal is to enable targeted marketing (e.g., premium/high-spend vs. affluent/low-spend) with a simple, interpretable unsupervised workflow. 

## Dataset
- Source: Mall_Customers.csv (200 rows, 5 columns). Typical fields: CustomerID, Gender, Age, Annual Income (k$), Spending Score (1–100). Include the CSV or reference the Kaggle page in your repo notes. 

## Methods
- Standardize numeric features, sweep k=2..8, and select k using elbow (inertia) and silhouette; fit final K-Means and assign clusters. 
- Profile clusters via mean Age/Income/Spending, visualize in 2D using PCA, and export cluster-labeled CSVs. 
## Results
- Produced N clusters (often 4–6) with distinct profiles (e.g., premium/high-spend, affluent/low-spend, value-seeking). Inspect `mall_cluster_profiles.csv` and PCA scatter plot for separation. 

## Repository Structure
- notebooks/
  - mall_segmentation_kmeans.ipynb — end-to-end Colab notebook. 
- data/
  - Mall_Customers.csv (or instructions to obtain it). 
- outputs/
  - mall_customer_clusters.csv — original rows + cluster + optional segment tag. 
  - mall_cluster_profiles.csv — per-cluster means and counts. 
- README.md

## How to Run (Colab)
1. Open the notebook in Google Colab.  
2. Upload `Mall_Customers.csv` (or point PATH to your file location).  
3. Run cells in order: EDA → scaling → elbow/silhouette → K-Means → PCA plot → export CSVs.

## Notes
- This is an unsupervised project: no train/test split; quality is assessed with internal metrics (elbow, silhouette) and business interpretability. [attached_file:49]
- You can override k (e.g., k=4) for cleaner personas if business needs demand fewer segments. 

## License
MIT (update if you use a different license).
