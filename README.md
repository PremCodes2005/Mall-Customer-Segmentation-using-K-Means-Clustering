# Mall Customer Segmentation (K-Means)

This project segments mall customers into meaningful groups using K-Means clustering on Age, Annual Income (k$), and Spending Score (1–100). The goal is to enable targeted marketing (e.g., premium/high-spend vs. affluent/low-spend) with a simple, interpretable unsupervised workflow. [attached_file:49]

## Dataset
- Source: Mall_Customers.csv (200 rows, 5 columns). Typical fields: CustomerID, Gender, Age, Annual Income (k$), Spending Score (1–100). Include the CSV or reference the Kaggle page in your repo notes. [attached_file:49]

## Methods
- Standardize numeric features, sweep k=2..8, and select k using elbow (inertia) and silhouette; fit final K-Means and assign clusters. [attached_file:49]
- Profile clusters via mean Age/Income/Spending, visualize in 2D using PCA, and export cluster-labeled CSVs. [attached_file:49]

## Results
- Produced N clusters (often 4–6) with distinct profiles (e.g., premium/high-spend, affluent/low-spend, value-seeking). Inspect `mall_cluster_profiles.csv` and PCA scatter plot for separation. 

## Repository Structure
- notebooks/
  - mall_segmentation_kmeans.ipynb — end-to-end Colab notebook. [attached_file:49]
- data/
  - Mall_Customers.csv (or instructions to obtain it). [attached_file:49]
- outputs/
  - mall_customer_clusters.csv — original rows + cluster + optional segment tag. [attached_file:49]
  - mall_cluster_profiles.csv — per-cluster means and counts. [attached_file:49]
- README.md

## How to Run (Colab)
1. Open the notebook in Google Colab. [attached_file:49]  
2. Upload `Mall_Customers.csv` (or point PATH to your file location). [attached_file:49]  
3. Run cells in order: EDA → scaling → elbow/silhouette → K-Means → PCA plot → export CSVs. [attached_file:49]

## Notes
- This is an unsupervised project: no train/test split; quality is assessed with internal metrics (elbow, silhouette) and business interpretability. [attached_file:49]
- You can override k (e.g., k=4) for cleaner personas if business needs demand fewer segments. [attached_file:49]

## License
MIT (update if you use a different license).
