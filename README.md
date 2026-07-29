# 🛍️ Mall Customer Segmentation using K-Means Clustering

**Name:** Athira V  
**MUID:** athirav-3@mulearn

---

## 📌 Project Overview

This project is part of **Epochs '26 - Assignment 7** and focuses on customer segmentation using **Unsupervised Machine Learning**.

The **Mall Customer Segmentation Dataset** is used to group customers with similar characteristics using the **K-Means Clustering** algorithm.

The analysis considers customer information such as:

- Gender
- Age
- Annual Income
- Spending Score

After clustering the customers, I analyzed the characteristics of each group and assigned meaningful business names to the segments.

I also used **Principal Component Analysis (PCA)** to reduce the data to two dimensions and visualize the customer segments.

The main goal is to understand different types of customers and suggest suitable business strategies for each group.

---

## 🎯 Objectives

The main objectives of this project are:

- Understand and explore the Mall Customer dataset.
- Check for missing values and duplicate records.
- Encode the categorical `Gender` feature.
- Scale the features before applying K-Means.
- Use the Elbow Method to select the number of clusters.
- Apply K-Means Clustering.
- Profile the resulting customer segments.
- Assign meaningful business names to the clusters.
- Use PCA to visualize the clusters in two dimensions.
- Analyze the customer groups and identify business opportunities.
- Recommend suitable strategies for each customer segment.

---

## 📂 Dataset

The dataset used in this project is the **Mall Customer Segmentation Dataset**.

### Dataset Source

Kaggle:  
https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python

### Features

| Feature | Description |
|---|---|
| `CustomerID` | Unique ID of each customer |
| `Gender` | Gender of the customer |
| `Age` | Age of the customer |
| `Annual Income (k$)` | Annual income in thousands of dollars |
| `Spending Score (1-100)` | Spending score assigned to the customer |

---

## 🛠️ Tools and Technologies

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- GitHub

### Machine Learning Techniques

- Data Preprocessing
- Feature Encoding
- StandardScaler
- K-Means Clustering
- Elbow Method
- Principal Component Analysis (PCA)

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Exploration
   ↓
Missing Value Check
   ↓
Duplicate Check
   ↓
Exploratory Data Analysis
   ↓
Categorical Feature Encoding
   ↓
Feature Scaling
   ↓
Elbow Method
   ↓
K-Means Clustering
   ↓
Cluster Assignment
   ↓
Cluster Profiling
   ↓
Business Segment Naming
   ↓
PCA
   ↓
Cluster Visualization
   ↓
Business Insights
   ↓
Recommendations
```

---

# 1️⃣ Data Exploration and Preprocessing

I first loaded the Mall Customer dataset using Pandas and explored its structure.

The dataset was checked for:

- Number of rows and columns
- Column names
- Data types
- Missing values
- Duplicate records

I also performed basic exploratory data analysis to understand:

- Customer distribution by gender
- Age distribution
- Annual income distribution
- Spending score distribution

These steps helped me understand the data before applying clustering.

---

# 2️⃣ Encoding Categorical Features

The `Gender` column contains categorical values, so it was converted into numerical form before applying the clustering algorithm.

The encoded feature was then included in the preprocessing pipeline.

---

# 3️⃣ Feature Scaling

I used **StandardScaler** to scale the features before applying K-Means.

The features have different numerical ranges. Since K-Means uses distance calculations to assign customers to clusters, features with larger numerical values could otherwise have more influence on the results.

StandardScaler transforms the features to a comparable scale, with a mean close to 0 and a standard deviation close to 1.

This allows the selected features to contribute more fairly during clustering.

---

# 4️⃣ Elbow Method

To determine a suitable number of clusters, I used the **Elbow Method**.

I calculated the K-Means inertia for values of K from 1 to 10 and plotted the results.

The Elbow Method helps identify the point where adding more clusters no longer provides a large improvement in reducing within-cluster variation.

Based on the Elbow Method plot, I selected:

**K = 5**

The final K-Means model was therefore trained using five clusters.

---

# 5️⃣ K-Means Clustering

I trained the K-Means model using:

- Number of clusters: 5
- Random state: 42
- Number of initializations: 10

Each customer was assigned to one of the five clusters.

The cluster labels were then added to the original dataset for further analysis.

---

# 6️⃣ Cluster Profiling

After assigning customers to clusters, I analyzed each cluster using:

- Number of customers
- Average age
- Average annual income
- Average spending score

The cluster profiles were used to understand the characteristics of each customer group.

The final segment names were assigned based on the actual characteristics of the clusters.

## Customer Segment Interpretation

| Segment | Customer Characteristics | Business Interpretation |
|---|---|---|
| Premium High-Value Customers | High income and high spending | Valuable customers who should be retained through premium experiences and loyalty programs |
| Budget-Conscious Customers | Lower income and lower spending | Customers who may respond well to discounts and affordable offers |
| Enthusiastic Shoppers | Lower or moderate income with high spending | Active customers who can be encouraged through targeted promotions and loyalty rewards |
| Careful High-Income Customers | High income but relatively low spending | Potential customers who may require personalized engagement |
| Regular Moderate Spenders | Moderate income and spending | Stable customers who can be encouraged through loyalty and cross-selling strategies |

The segment names and interpretations should be understood from the cluster profile generated by the K-Means model.

---

# 7️⃣ PCA Dimensionality Reduction

I applied **Principal Component Analysis (PCA)** to reduce the scaled feature space to two dimensions.

The two principal components were used to visualize the customer clusters.

This makes it easier to observe how the customer groups are distributed in a two-dimensional space.

## 📈 PCA Explained Variance

The first two principal components explained the following amount of variance:

```text
PC1 Explained Variance: 33.69%
PC2 Explained Variance: 26.23%

Total Explained Variance: 59.92%
```

Therefore, the first two principal components together retain approximately **59.92%** of the total variance in the data.

The PCA visualization provides a simplified view of the customer segments while retaining a significant amount of information from the original feature space.

---

# 📊 Visualizations

The project includes visualizations for:

- Gender distribution
- Age distribution
- Annual income distribution
- Spending score distribution
- Elbow Method
- Customer clusters
- PCA-based customer segment visualization

These visualizations were used to understand both the original dataset and the final clustering results.

---

# 💡 Business Insights

### 1. High-Value Customers Should Be Retained

Customers with high income and high spending behavior represent an important segment.

Businesses can focus on:

- VIP loyalty programs
- Premium products
- Exclusive offers
- Personalized recommendations

### 2. Budget-Conscious Customers Need Value-Based Offers

Customers with lower income and lower spending behavior may respond better to:

- Discounts
- Seasonal offers
- Affordable product bundles
- Value-for-money promotions

### 3. High-Spending Customers Can Be Encouraged to Stay Engaged

Customers who spend frequently can be targeted using:

- Loyalty rewards
- Personalized promotions
- Limited-time offers
- Repeat-purchase campaigns

### 4. High-Income but Low-Spending Customers Represent an Opportunity

Customers with high income but lower spending may have strong purchasing potential but low engagement.

Businesses can try:

- Personalized marketing
- Premium product recommendations
- Exclusive shopping experiences
- Customer feedback campaigns

### 5. Moderate Customers Can Be Encouraged to Increase Spending

Customers with moderate income and spending behavior can be targeted using:

- Loyalty points
- Cross-selling
- Upselling
- Personalized product recommendations

---

# 🚀 Recommended Business Strategies

| Customer Segment | Recommended Strategy |
|---|---|
| Premium High-Value Customers | VIP programs, premium products, exclusive offers |
| Budget-Conscious Customers | Discounts, affordable bundles, seasonal promotions |
| Enthusiastic Shoppers | Loyalty rewards, targeted promotions, personalized offers |
| Careful High-Income Customers | Personalized marketing and premium experiences |
| Regular Moderate Spenders | Loyalty points, cross-selling, and upselling |

---

# 📌 Important Observations

From this analysis, I observed that:

- Customers have different spending behaviors even when their income levels are similar.
- Income alone is not enough to understand customer value.
- Spending Score provides useful information for identifying customer behavior.
- K-Means can help group customers with similar characteristics.
- Feature scaling is important because K-Means relies on distance calculations.
- The Elbow Method provides a practical way to select a suitable number of clusters.
- PCA helps visualize the customer segments in a reduced two-dimensional space.
- Different customer groups require different marketing strategies.

---

# 🏆 Conclusion

In this project, I used K-Means Clustering to segment mall customers into five groups based on their demographic and behavioral characteristics.

I first explored and prepared the dataset, encoded the categorical feature, and applied feature scaling. The Elbow Method was then used to select five clusters for the final K-Means model.

After clustering, I analyzed the characteristics of each group and interpreted them as meaningful customer segments. These segments can help businesses understand customer behavior and design more targeted marketing strategies.

Finally, I applied PCA to reduce the data to two dimensions and visualize the customer clusters. The first two principal components explained approximately **59.92%** of the variance in the dataset.

Overall, this project demonstrates how K-Means clustering can be used to discover customer segments and convert those patterns into practical business strategies.

---

# 📁 Project Structure

```text
day_7_epoch_task/
│
├── customer_segmentation.ipynb
│
└── README.md
```

---

# 👩‍💻 Author

**Athira V**

**MUID:** athirav-3@mulearn
