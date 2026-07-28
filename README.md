# 🛍️ Mall Customer Segmentation using K-Means Clustering

**Name:** Athira V  
**MUID:** athirav-3@mulearn

---

## 📌 Project Overview

This project focuses on **customer segmentation using Unsupervised Machine Learning** techniques.

The **Mall Customer Segmentation Dataset** is analyzed using the **K-Means Clustering** algorithm to identify groups of customers with similar demographic and purchasing behavior.

The project also uses **Principal Component Analysis (PCA)** to reduce the dimensionality of the dataset and visualize the identified customer segments in a two-dimensional space.

The main goal of this project is to discover meaningful customer groups and derive **actionable business insights** that can help businesses improve their marketing strategies, customer engagement, and personalized services.

---

## 🎯 Objectives

The main objectives of this project are:

- Explore and understand the customer dataset.
- Check and handle missing values.
- Check for duplicate records.
- Encode categorical features into numerical form.
- Apply feature scaling before clustering.
- Understand why feature scaling is important for K-Means.
- Use the **Elbow Method** to determine the optimal number of clusters.
- Build a **K-Means Clustering** model.
- Assign each customer to a suitable cluster.
- Profile the identified customer clusters.
- Give meaningful business names to the customer segments.
- Apply **PCA** for dimensionality reduction.
- Visualize customer segments using PCA.
- Calculate and report the variance explained by the principal components.
- Generate actionable business insights.
- Recommend suitable strategies for each customer segment.

---

## 📂 Dataset

The project uses the **Mall Customer Segmentation Dataset**.

### Dataset Source

Kaggle:  
https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python

### Dataset Features

| Feature | Description |
|---|---|
| `CustomerID` | Unique identification number assigned to each customer |
| `Gender` | Gender of the customer |
| `Age` | Age of the customer |
| `Annual Income (k$)` | Annual income of the customer in thousands of dollars |
| `Spending Score (1-100)` | Spending score assigned to the customer based on purchasing behavior |

---

## 🛠️ Technologies and Libraries Used

The project was implemented using **Python** in **Google Colab**.

### Programming Language

- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

### Machine Learning Techniques

- Feature Scaling
- K-Means Clustering
- Elbow Method
- Principal Component Analysis (PCA)

### Development Environment

- Google Colab
- Jupyter Notebook
- GitHub

---

# 🔄 Project Workflow

The project follows the workflow below:

```text
Dataset
   ↓
Data Loading
   ↓
Data Understanding
   ↓
Missing Value Check
   ↓
Duplicate Check
   ↓
Exploratory Data Analysis
   ↓
Categorical Feature Encoding
   ↓
Feature Selection
   ↓
Feature Scaling
   ↓
Elbow Method
   ↓
Optimal K Selection
   ↓
K-Means Clustering
   ↓
Cluster Assignment
   ↓
Cluster Profiling
   ↓
Business Segment Naming
   ↓
PCA Dimensionality Reduction
   ↓
PCA Visualization
   ↓
Business Insights
   ↓
Customer-Specific Strategies
   ↓
Conclusion
```

---

# 1️⃣ Data Loading and Understanding

The dataset was loaded into a Pandas DataFrame and examined to understand its structure.

The following operations were performed:

* Displaying the first few records.
* Checking the shape of the dataset.
* Inspecting column names.
* Checking data types.
* Generating descriptive statistics.

This helped in understanding the characteristics of the dataset before applying machine learning techniques.

---

# 2️⃣ Data Preprocessing

## Missing Value Handling

The dataset was checked for missing values using Pandas.

Missing values can affect the performance of machine learning algorithms. Therefore, the dataset was inspected before proceeding with clustering.

The dataset was found to have no significant missing values requiring imputation.

## Duplicate Check

Duplicate records were also checked to ensure that repeated customer records do not affect the clustering results.

---

# 3️⃣ Exploratory Data Analysis

Exploratory Data Analysis (EDA) was performed to understand customer characteristics and distributions.

The following visualizations were created:

* Customer distribution by gender.
* Age distribution.
* Annual income distribution.
* Spending score distribution.

These visualizations helped identify patterns in the customer population and understand the distribution of important features.

---

# 4️⃣ Categorical Feature Encoding

The `Gender` feature is categorical and cannot be directly processed by K-Means in its original text format.

Therefore, it was converted into numerical form:

```text
Male   → 0
Female → 1
```

This encoded feature was then used during the preprocessing stage.

---

# 5️⃣ Feature Selection

The following features were selected for customer segmentation:

* Age
* Annual Income
* Spending Score
* Encoded Gender

These features represent both demographic and behavioral characteristics of customers.

The selected features allow the clustering algorithm to identify customers with similar characteristics.

---

# 6️⃣ Feature Scaling

Feature scaling was applied using **StandardScaler**.

The features in the dataset have different numerical ranges. For example, age, annual income, spending score, and encoded gender have different scales.

K-Means clustering is based on distance calculations. Therefore, features with larger numerical values could have a greater influence on the clustering process if scaling is not performed.

StandardScaler transforms the features so that they have:

* Mean approximately equal to 0.
* Standard deviation approximately equal to 1.

This allows the features to contribute more fairly to the clustering process.

---

# 7️⃣ Elbow Method

The **Elbow Method** was used to determine a suitable number of clusters for the K-Means algorithm.

The method calculates the **Within-Cluster Sum of Squares**, represented by the inertia, for different values of K.

The inertia generally decreases as the number of clusters increases.

The optimal number of clusters is selected by identifying the point where the decrease in inertia begins to slow down significantly. This point is known as the **elbow point**.

The Elbow Method was used to determine the final value of K used for the K-Means model.

---

# 8️⃣ K-Means Clustering

After determining the appropriate number of clusters, the K-Means clustering algorithm was trained on the standardized dataset.

K-Means works by:

1. Selecting K initial cluster centroids.
2. Assigning each data point to the nearest centroid.
3. Updating the centroid of each cluster.
4. Repeating the process until the clusters converge.

Each customer was assigned to one of the resulting clusters.

The cluster labels were then added to the original dataset for further analysis.

---

# 9️⃣ Cluster Profiling

After assigning customers to clusters, each cluster was analyzed based on its characteristics.

The following metrics were used to profile the clusters:

* Number of customers.
* Average age.
* Average annual income.
* Average spending score.

The cluster profiles were used to understand the behavior and characteristics of each customer group.

Based on these characteristics, meaningful business names were assigned to the clusters.

---

# 👥 Customer Segments

The identified clusters were interpreted based on their income, spending behavior, and demographic characteristics.

The following are the possible business interpretations of the customer segments:

### 💎 Premium High-Value Customers

These customers have relatively high annual income and high spending scores.

They represent an important customer segment because they have both strong purchasing power and high engagement with the mall.

**Recommended Strategies:**

* Provide premium products and services.
* Introduce exclusive loyalty programs.
* Offer VIP memberships.
* Provide personalized recommendations.
* Give early access to new products and special events.

---

### 💰 Budget-Conscious Customers

These customers have relatively lower income and lower spending scores.

Their purchasing behavior may be influenced by affordability and discounts.

**Recommended Strategies:**

* Offer discounts and seasonal promotions.
* Provide affordable product bundles.
* Introduce value-for-money offers.
* Promote budget-friendly products.
* Use special sale events to increase engagement.

---

### 🛍️ Enthusiastic / High-Spending Customers

These customers demonstrate relatively high spending behavior.

They may respond positively to targeted campaigns and personalized promotions.

**Recommended Strategies:**

* Introduce loyalty rewards.
* Offer personalized discounts.
* Promote repeat purchases.
* Use limited-time offers.
* Recommend products based on previous purchasing behavior.

---

### 💼 Careful High-Income Customers

These customers have relatively high income but comparatively lower spending scores.

They have strong purchasing power but may not be highly engaged with the mall.

**Recommended Strategies:**

* Use personalized marketing campaigns.
* Promote premium and exclusive products.
* Understand their preferences through customer feedback.
* Offer personalized shopping experiences.
* Focus on quality and exclusivity instead of heavy discounts.

---

### 📊 Regular Moderate Spenders

These customers have moderate income and moderate spending behavior.

They represent a stable customer group that can potentially be encouraged to increase their spending.

**Recommended Strategies:**

* Introduce loyalty point systems.
* Encourage repeat purchases.
* Use cross-selling and upselling strategies.
* Provide personalized product recommendations.
* Offer moderate discounts and bundle deals.

> **Note:** The exact cluster interpretation and segment names should be aligned with the final cluster profiling results generated by the K-Means model.

---

# 🔬 PCA Dimensionality Reduction

**Principal Component Analysis (PCA)** was used to reduce the dimensionality of the standardized dataset.

The original dataset contains multiple features used for clustering. PCA transforms these features into new dimensions called **Principal Components**.

For visualization, the dataset was reduced to two principal components:

* Principal Component 1 (PC1)
* Principal Component 2 (PC2)

This allows the customer segments to be visualized in a two-dimensional space.

---

# 📈 Explained Variance

The explained variance ratio of each principal component was calculated to understand how much information is retained after dimensionality reduction.

The following values were obtained from the PCA analysis:

```text
PC1 Explained Variance: 33.69 %
PC2 Explained Variance: 26.23%

Total Explained Variance: 59.92%
```

The first two principal components together explain a significant portion of the variance in the standardized dataset, allowing the customer segments to be visually analyzed in a 2D representation.

---

# 📊 Customer Segment Visualization

The customer clusters were visualized using two approaches.

## 1. Income vs Spending Score

A scatter plot was created using:

* Annual Income
* Spending Score

This visualization helps understand the relationship between customer purchasing power and spending behavior.

## 2. PCA Visualization

PCA was used to project the standardized customer data into two dimensions.

The resulting scatter plot shows the distribution of customers across the identified clusters.

Different colors represent different customer segments, making it easier to understand the separation and distribution of the clusters.

---

# 💡 Key Business Insights

The customer segmentation analysis provides several important business insights.

### 1. Customer Behavior is Not Uniform

Customers have different income levels, demographic characteristics, and spending behaviors.

Therefore, applying the same marketing strategy to every customer may not be effective.

Customer segmentation allows businesses to develop strategies based on the characteristics of individual customer groups.

---

### 2. High-Value Customers Should Be Prioritized

Customers with high income and high spending scores are particularly valuable.

Businesses should focus on retaining these customers through:

* Personalized services.
* Premium experiences.
* Loyalty rewards.
* Exclusive offers.

---

### 3. Low-Spending Customers Can Be Encouraged Through Promotions

Customers with lower spending behavior may respond positively to:

* Discounts.
* Seasonal sales.
* Product bundles.
* Affordable offers.

These strategies can encourage increased purchase frequency.

---

### 4. High-Income but Low-Spending Customers Represent an Opportunity

Customers with high purchasing power but low spending scores may represent an untapped opportunity.

Businesses can investigate their preferences and use personalized marketing to increase engagement.

---

### 5. Customer Segmentation Enables Targeted Marketing

Instead of using a single marketing strategy for everyone, businesses can target each segment with a suitable approach.

This can improve:

* Customer satisfaction.
* Marketing effectiveness.
* Customer retention.
* Sales opportunities.
* Resource allocation.

---

# 🚀 Recommendations

Based on the identified customer segments, the following recommendations can be implemented:

| Customer Segment                     | Recommended Strategy                                              |
| ------------------------------------ | ----------------------------------------------------------------- |
| Premium High-Value Customers         | VIP programs, premium products, exclusive offers                  |
| Budget-Conscious Customers           | Discounts, affordable bundles, seasonal sales                     |
| Enthusiastic High-Spending Customers | Loyalty rewards, personalized offers, repeat-purchase campaigns   |
| Careful High-Income Customers        | Personalized marketing, premium experiences, targeted engagement  |
| Regular Moderate Spenders            | Loyalty points, cross-selling, upselling, product recommendations |

These strategies can be adjusted according to the actual cluster profiles generated by the K-Means model.

---

# 📌 Important Observations and Findings

The project demonstrates that:

* Customer segmentation can reveal hidden patterns in customer behavior.
* K-Means clustering can group customers based on similarities in their characteristics.
* Feature scaling is essential for distance-based algorithms such as K-Means.
* The Elbow Method provides a useful approach for selecting the number of clusters.
* PCA helps visualize high-dimensional data in a two-dimensional space.
* Cluster profiling is essential for translating machine learning results into meaningful business insights.
* Different customer segments require different marketing and engagement strategies.
* High-income and high-spending customers can be considered an important target group for customer retention.
* Low-spending customers may require targeted promotions and value-based offers.
* High-income customers with lower spending behavior may represent an opportunity for personalized engagement.

---

# 🏆 Final Conclusion

This project successfully applies **Unsupervised Machine Learning** to segment mall customers into meaningful groups using **K-Means Clustering**.

The project followed a complete machine learning workflow, including data preprocessing, categorical encoding, feature scaling, exploratory data analysis, optimal cluster selection using the Elbow Method, K-Means clustering, cluster profiling, and business interpretation.

PCA was also applied to reduce the dimensionality of the dataset and visualize the customer segments in two dimensions. The explained variance of the principal components was calculated to understand the amount of information retained in the reduced representation.

The resulting customer segments provide valuable insights into customer demographics, income levels, and spending behavior.

Businesses can use these insights to:

* Identify high-value customers.
* Improve customer retention.
* Create personalized marketing campaigns.
* Design targeted promotions.
* Increase customer engagement.
* Optimize marketing resources.
* Develop customer-specific strategies.

Overall, this project demonstrates how **unsupervised learning and customer segmentation can transform raw customer data into actionable business intelligence**.

---

# 📁 Project Structure

```text
customer-segmentation/
│
├── customer_segmentation.ipynb
│
└── README.md
```

### `customer_segmentation.ipynb`

Contains the complete implementation of:

* Data loading
* Data preprocessing
* Exploratory Data Analysis
* Feature encoding
* Feature scaling
* Elbow Method
* K-Means Clustering
* Cluster profiling
* PCA
* Cluster visualization
* Business insights
* Recommendations

### `README.md`

Contains:

* Project overview
* Objectives
* Dataset information
* Methodology
* Technologies used
* Key observations
* Business insights
* Recommendations
* Final conclusion

---

# 👩‍💻 Author

**Athira V**

**MUID:** athirav-3@mulearn

---

⭐ This project was completed as part of **Epochs '26 – Assignment 7** on **Unsupervised Learning and Customer Segmentation**.
