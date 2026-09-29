# 👥 Customer Data Segmentation Analysis

## 📌 Overview

This project analyzes and segments customer data from a mall using **K-Means clustering** to identify groups of customers with different characteristics.

The analysis explores customer attributes such as **age, annual income, and spending score**, supported by exploratory data analysis (EDA), data preprocessing, feature standardization, and cluster evaluation.

The final analysis produces **5 customer segments** with different combinations of age, annual income, and spending score, providing insights into customer characteristics and potential segmentation patterns.

---

## 🎯 Objectives

- Explore customer demographic and spending data.
- Identify patterns and relationships between customer attributes.
- Prepare the data for clustering through preprocessing and standardization.
- Determine an appropriate number of customer clusters.
- Evaluate clustering results using multiple evaluation methods.
- Analyze the characteristics of each customer segment.

---

## 📂 Dataset

The analysis uses the **Mall Customers** dataset stored in:

`Mall_Customers.csv`

The dataset contains **200 customer records** with the following attributes:

| Feature | Description |
|---|---|
| CustomerID | Unique identifier for each customer |
| Gender | Customer gender |
| Age | Customer age |
| Annual Income (k$) | Customer annual income |
| Spending Score (1–100) | Spending score assigned to each customer |

### Dataset Preparation

The following preprocessing steps were performed:

- Checked for missing values.
- Checked for duplicate records.
- Removed `CustomerID` because it is an identifier and is not useful for clustering.
- Renamed `Annual Income (k$)` to `Annual Income`.
- Renamed `Spending Score (1-100)` to `Spending Score`.
- Encoded `Gender` into numerical values using **LabelEncoder**.
- Applied **Z-score standardization** to the numerical data used in the analysis.

---

## 🔎 Exploratory Data Analysis

Exploratory Data Analysis (EDA) was performed to understand the characteristics and relationships within the customer dataset.

The analysis includes:

- Pairplot to explore relationships between customer attributes.
- Gender distribution.
- Annual income distribution using a histogram.
- Relationship between annual income and spending score.
- Descriptive statistics of the dataset.

The dataset consists of:

- **112 female customers**
- **88 male customers**

---

## ⚙️ K-Means Clustering

### 1. Determining the Number of Clusters

The **Elbow Method** was used to evaluate different values of `K` from 1 to 10 by observing the inertia of the K-Means model.

Additional clustering evaluation was performed using:

- **Silhouette Score**
- **Davies-Bouldin Index**

These evaluation methods were used to examine the quality and separation of different cluster configurations.

### 2. Final Clustering

The final K-Means model was created with:

- **Number of Clusters:** 5
- **Random State:** 42

The resulting clusters were then analyzed based on customer characteristics, including age, annual income, and spending score.

---

## 📊 Customer Segments

The five resulting customer groups show different characteristics.

| Cluster | Age | Annual Income | Spending Score | General Characteristics |
|---|---:|---:|---:|---|
| Category 0 | 55.55 | 48.48 k$ | 41.78 | Older customers with relatively lower income and spending |
| Category 1 | 25.27 | 25.73 k$ | 79.36 | Younger customers with lower income but high spending |
| Category 2 | 41.26 | 88.50 k$ | 16.76 | Customers with higher income but low spending |
| Category 3 | 27.96 | 50.00 k$ | 44.64 | Younger customers with moderate income and spending |
| Category 4 | 32.69 | 86.54 k$ | 82.13 | Customers with higher income and high spending |

> The values above represent the average characteristics of each cluster based on the notebook's clustering results.

---

## 📈 Cluster Visualization

The resulting customer segments were visualized using:

- Pairplots with cluster categories.
- Violin plots for age, annual income, and spending score.
- Annual income distribution.
- Annual income vs. spending score scatter plot.

These visualizations help illustrate the differences between the resulting customer groups.

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **Seaborn**
- **Matplotlib**
- **Scikit-learn**
  - K-Means
  - StandardScaler
  - LabelEncoder
  - Silhouette Score
  - Davies-Bouldin Index
- **Google Colab / Jupyter Notebook**

---

## 🔄 Analysis Workflow

The analysis follows this workflow:

**Mall_Customers.csv**  
↓  
**Data Inspection**  
↓  
**Missing Value & Duplicate Check**  
↓  
**Data Preprocessing**  
↓  
**Label Encoding**  
↓  
**Z-score Standardization**  
↓  
**Exploratory Data Analysis**  
↓  
**Elbow Method**  
↓  
**Silhouette Score & Davies-Bouldin Index**  
↓  
**K-Means Clustering**  
↓  
**5 Customer Segments**  
↓  
**Cluster Analysis & Visualization**

---

## 📂 Repository Contents

- 📓 `Customer-Data-Segmentation-Analysis.ipynb` — Jupyter Notebook containing the complete analysis.
- 📄 `Mall_Customers.csv` — Customer dataset used for the analysis.
- 📄 `README.md` — Project documentation.

---

## 🔍 Key Takeaways

This project demonstrates the application of **unsupervised machine learning** for customer segmentation.

The analysis resulted in five customer segments with different combinations of:

- Age
- Annual income
- Spending score

The segmentation provides a way to understand differences in customer characteristics and can serve as a basis for further customer analysis and segmentation-oriented marketing strategies.

---

## 🏷️ Keywords

`Python` `K-Means` `Customer Segmentation` `Unsupervised Learning` `Clustering` `Data Analysis` `EDA` `Machine Learning` `Scikit-learn` `Pandas` `Seaborn`
