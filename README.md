# **Mall Customers Segmentation using K-Means Clustering**

## **Project Overview**
This project applies **K-Means clustering** to segment mall customers based on their **annual income** and **spending behavior**.  
The objective is to identify distinct, behavior-driven customer groups and determine the optimal number of clusters using **Elbow Method** and **Silhouette Analysis**, enabling interpretable and actionable insights for business decision-making.

---

## **Dataset Description**
- **Dataset:** Mall Customers
- **Records:** 200 customers
- **Features:**
  - CustomerID
  - Gender
  - Age
  - Annual Income (k$)
  - Spending Score (1–100)

The dataset contains **no missing values and no duplicate records**, making it suitable for unsupervised learning without additional data cleaning.

---

## **Exploratory Data Analysis (EDA)**
Key findings from EDA include:
- `CustomerID` was removed as it has no analytical value for clustering.
- `Gender` was excluded to avoid artificial numerical relationships in distance-based clustering.
- `Age` was analyzed but found not to contribute meaningful separation compared to behavioral variables.
- **Annual Income** and **Spending Score** showed clear variability and natural grouping.

Bivariate analysis of income vs spending revealed **distinct, well-separated groups**, justifying the use of K-Means clustering.

---

## **Methodology**
1. **Feature Selection**
   - Annual Income (k$)
   - Spending Score (1–100)

2. **Feature Scaling**
   - StandardScaler applied to ensure fair distance computation.

3. **Optimal Cluster Selection**
   - **Elbow Method:** Clear inflection point at `k = 5`
   - **Silhouette Analysis:** Highest score at `k = 5` (≈ 0.55)

4. **Model Training**
   - K-Means with `k = 5`
   - `k-means++` initialization
   - Fixed random state for reproducibility

---

## **Results & Customer Segments**

| Cluster | Description | Insight |
|-------|------------|---------|
| Cluster 0 | Average Customers | Moderate income and spending |
| Cluster 1 | High-Value Customers (VIPs) | High income, high spending |
| Cluster 2 | Impulsive Low-Income Spenders | Low income, high spending |
| Cluster 3 | Careful High-Income Customers | High income, low spending |
| Cluster 4 | Low-Value Customers | Low income, low spending |

These segments demonstrate that **income alone does not determine spending behavior**, highlighting the importance of behavioral-based segmentation.

---

## **Business Value**
- Enables **targeted marketing strategies** instead of one-size-fits-all campaigns
- Helps identify **high-value and underperforming customer groups**
- Improves **resource allocation** by focusing on segments with higher ROI
- Provides insights that are **easy to communicate to non-technical stakeholders**

---

## **Limitations**
- Small dataset size (200 customers) limits generalization
- Only two behavioral features were used for clustering
- K-Means assumes spherical clusters and equal variance
- No temporal or transactional data available

---

## **Future Improvements**
- Incorporate additional features such as age, gender, or purchase frequency
- Experiment with alternative clustering algorithms (DBSCAN, Hierarchical Clustering)
- Validate cluster stability across multiple random initializations
- Apply the approach to a larger, real-world retail dataset

---

## **Final Takeaway**
> *By focusing on behavioral variables and validating cluster quality using both Elbow and Silhouette methods, this project demonstrates how K-Means can uncover meaningful and actionable customer segments that support data-driven business decisions.*

---

## **Repository Structure**

```
├── Mall_Customers.csv
├── Mall_Customers_K_means.ipynb
├── Mall_Customers_K_means.pdf
├── README.md
```

---

## **Tech Stack**
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## **Running the Project**

1. Clone this repository:
```bash
git clone https://github.com/PranayDomal/Mall_Customers-KMeans.git
```
2. Navigate to the project directory.
```bash
cd Mall_Customers-KMeans
```
3. Open and run the Jupyter Notebook:
```bash
jupyter notebook Mall_Customers_K_means.ipynb
```

---

## **Author**

https://www.linkedin.com/in/pranay-domal-a641bb368/
