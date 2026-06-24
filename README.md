# 📊 Customer Segmentation using RFM Analysis & K-Means Clustering

## 📌 Project Overview

Customer segmentation is a critical business strategy that helps organizations understand customer behavior and deliver personalized experiences. In this project, customers were segmented based on their purchasing behavior using **RFM (Recency, Frequency, Monetary) Analysis** and **K-Means Clustering**.

The objective was to identify distinct customer groups and generate actionable business insights that can support customer retention, targeted marketing campaigns, and revenue optimization.

---

## 🎯 Objectives

* Analyze customer purchasing behavior.
* Perform customer segmentation using machine learning techniques.
* Identify high-value, regular, and at-risk customers.
* Generate business insights for marketing and retention strategies.
* Build a data-driven framework for customer analytics.

---

## 📂 Dataset Information

### Dataset

Online Retail Dataset

### Source

Kaggle – Online Retail Dataset

### Dataset Description

The dataset contains transactional records from a UK-based online retail company between December 2010 and December 2011.

### Features Used

| Column      | Description                   |
| ----------- | ----------------------------- |
| InvoiceNo   | Unique transaction identifier |
| StockCode   | Product identifier            |
| Description | Product description           |
| Quantity    | Number of units purchased     |
| InvoiceDate | Transaction date and time     |
| UnitPrice   | Price per unit                |
| CustomerID  | Unique customer identifier    |
| Country     | Customer location             |

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Jupyter Notebook / VS Code

---

## 📋 Project Workflow

### 1. Data Cleaning

The raw dataset contained missing values, cancelled orders, and invalid transactions.

The following cleaning steps were performed:

* Removed records with missing Customer IDs
* Removed cancelled transactions
* Removed negative quantities
* Removed transactions with zero or negative prices
* Created a Revenue column

Revenue Calculation:

```python
Revenue = Quantity × UnitPrice
```

---

### 2. Exploratory Data Analysis (EDA)

Initial exploration was performed to understand:

* Customer distribution
* Revenue contribution
* Country-wise transactions
* Missing values
* Duplicate records

Key Findings:

* United Kingdom generated the majority of transactions.
* The dataset contained more than 500,000 transaction records.
* Revenue exceeded £8.9 million after cleaning.

---

### 3. RFM Analysis

RFM analysis is a widely used customer segmentation technique based on customer purchase behavior.

### Recency (R)

How recently a customer made a purchase.

### Frequency (F)

How often a customer makes purchases.

### Monetary (M)

How much money a customer spends.

The RFM table was created at the customer level to summarize customer behavior.

---

### 4. Outlier Treatment

Extreme values in Recency, Frequency, and Monetary variables can negatively impact clustering performance.

To improve model quality:

* Interquartile Range (IQR) method was used
* Outliers were removed from all three RFM metrics

---

### 5. Feature Scaling

Since RFM metrics exist on different scales, StandardScaler was used to normalize the data before clustering.

```python
from sklearn.preprocessing import StandardScaler
```

---

### 6. K-Means Clustering

K-Means clustering was applied to group customers based on purchasing behavior.

The optimal number of clusters was determined using the Elbow Method.

### Elbow Method

The Elbow Curve indicated that **3 clusters** provided the best balance between model complexity and cluster separation.

---

## 📈 Customer Segments Identified

### ⭐ High Value Customers

Characteristics:

* Recent purchases
* High purchase frequency
* Highest spending levels

Average Metrics:

* Recency: 37 days
* Frequency: 5.68
* Monetary Value: £1847

Business Strategy:

* Loyalty programs
* Exclusive offers
* VIP customer engagement

---

### 👍 Regular Customers

Characteristics:

* Moderate purchase frequency
* Moderate spending levels
* Consistent customer activity

Average Metrics:

* Recency: 50 days
* Frequency: 2.03
* Monetary Value: £559

Business Strategy:

* Cross-selling opportunities
* Personalized recommendations
* Membership incentives

---

### ⚠️ At-Risk Customers

Characteristics:

* Long period since last purchase
* Low purchase frequency
* Lowest spending levels

Average Metrics:

* Recency: 228 days
* Frequency: 1.49
* Monetary Value: £405

Business Strategy:

* Re-engagement campaigns
* Discount offers
* Customer win-back programs

---

## 📊 Results

The clustering model successfully categorized customers into meaningful business segments.

Key observations:

* High Value Customers generated significantly higher revenue than other segments.
* At-Risk Customers showed low engagement and purchase activity.
* Customer retention strategies can be tailored according to segment behavior.
* Data-driven segmentation enables more efficient marketing resource allocation.

---

## 💡 Business Recommendations

### For High Value Customers

* Reward loyalty through exclusive benefits.
* Provide early access to promotions.
* Focus on long-term retention.

### For Regular Customers

* Encourage repeat purchases.
* Introduce personalized product recommendations.
* Promote loyalty memberships.

### For At-Risk Customers

* Launch targeted retention campaigns.
* Offer time-sensitive discounts.
* Conduct customer feedback initiatives.

---

## 📁 Project Structure

```text
Customer-Segmentation/
│
├── customer_segmentation.ipynb
├── OnlineRetail.csv
├── customer_segments.csv
├── README.md


## 🚀 Future Improvements

* RFM Scoring and Customer Lifetime Value (CLV) Analysis
* Advanced clustering techniques (DBSCAN, Hierarchical Clustering)
* Interactive Power BI Dashboard
* Real-time customer segmentation pipeline
* Marketing campaign effectiveness analysis

---

## 👨‍💻 Author

**Akshat Porwal**

B.Tech Information Technology | Data Analytics Enthusiast

Skills:

* Python
* SQL
* Power BI
* Excel
* Machine Learning
* Data Visualization
* Business Analytics

---

### ⭐ If you found this project useful, consider giving the repository a star.
