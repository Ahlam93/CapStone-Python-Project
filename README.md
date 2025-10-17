#  Customer Segmentation 
### **RFM & K-Means Clustering Analysis**

A Data Science project that explores customer purchasing behavior using **RFM (Recency, Frequency, Monetary)** analysis and **K-Means clustering**.  
The goal is to identify key customer groups to enhance **marketing strategies, loyalty programs**, and **business profitability**.

---

##  Executive Summary

This project aims to uncover insights from customer transactional data to drive data-driven marketing strategies.  
By applying **RFM analysis** and **K-Means clustering**, customers are segmented into meaningful groups such as **loyal**, **at-risk**, and **hibernating** customers.

**Key outcomes:**
- Identify high-value and at-risk customer segments.
- Improve targeting efficiency through personalized marketing.
- Maximize customer engagement and retention.

---

##  Methods

### **1. RFM Analysis**
Three key behavioral metrics:
- **Recency:** How recently a customer purchased.
- **Frequency:** How often they purchase.
- **Monetary:** How much they spend.

**Customer Segments Identified:**
| Segment | Description |
|----------|--------------|
|  Champions | Frequent and recent buyers |
|  Potential Loyalists | Show strong engagement and promise |
|  Hibernating | Inactive or lost customers |

>  *RFM helps businesses tailor retention and loyalty strategies effectively.*

---

### **2. K-Means Clustering**
An unsupervised ML approach to group customers with similar characteristics.

**Features Used:**
- Age, Income, Education, Marital Status  
- Total Purchases, Total Expenses, Accepted Campaigns, Total Kids Number

**Optimal Clusters (using Elbow Method):**
| Cluster | Description |
|----------|--------------|
| **Cluster 1** | Married, lower income, more kids, lower spending |
| **Cluster 2** | Single or fewer kids, higher income, higher spending |

>  *Cluster 2 customers are high-value and ideal for premium targeting.*

---

##  Data Cleaning & Preparation

**Dataset Source:** [Kaggle – Dr. Omar Romero-Hernandez](https://www.kaggle.com/)  
**Shape:** 2240 rows × 29 columns

**Key Data Cleaning Steps:**
- Filled missing values in `Income` using median.  
- Created new derived columns:
  - `Total_Expenses` (sum of all product spend columns)
  - `Total_Kids_Number` (`Kidhome + Teenhome`)
  - `Total_Purchases_Number` and `Total_Accepted_Campaigns`
- Encoded categorical columns (`Education`, `Marital_Status`).
- Removed meaningless columns (`Z_CostContact`, `Z_Revenue`).
- Handled outliers in `Age` and `Income`.

---

##  Results & Insights

**Top correlations with Total Expenses:**
1. Income  
2. Total Purchases Number  
3. Total Accepted Campaigns  

**Low correlations:**
- Age  
- Marital Status  
- Total Kids Number  

**Insights:**
- Higher income correlates strongly with higher spending.
- Campaign performance varies across segments.
- Potential Loyalists should be nurtured for conversion to Champions.

---

##  Tools & Technologies

| Category | Tools |
|-----------|--------|
| Language | Python |
| Libraries | pandas, numpy, matplotlib, seaborn, scikit-learn |
| Modeling | RFM Analysis, K-Means Clustering |
| Visualization | matplotlib, seaborn |
| Data Source | Kaggle |

---

##  Recommendations

1. **Focus on High-Value Segments:** Prioritize Cluster 2 with premium campaigns.  
2. **Loyalty Programs:** Retain Champions and Potential Loyalists.  
3. **Personalized Offers:** Design custom offers for at-risk customers.  
4. **Continuous Data Updates:** Refresh models periodically.  
5. **Feedback Loop:** Integrate customer feedback to refine segmentation.



