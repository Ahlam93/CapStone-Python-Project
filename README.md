#  Customer Segmentation Capstone Project  
### **RFM Analysis & K-Means Clustering**

A data-driven project focused on understanding and segmenting customers based on purchasing behavior, using **RFM (Recency, Frequency, Monetary)** analysis and **K-Means clustering** to uncover actionable insights that improve marketing strategies, customer retention, and business growth.

---

##  Executive Summary

This capstone project explores how businesses can leverage data analytics to understand customer purchasing patterns and enhance marketing effectiveness.  
By analyzing demographic and transactional data, the project identifies distinct customer segments to enable **targeted campaigns**, **personalized offers**, and **strategic decision-making**.

### **Key Objectives**
- Understand factors influencing customer purchasing behavior.  
- Segment customers based on RFM metrics and behavioral attributes.  
- Identify actionable insights to improve campaign targeting and retention.  
- Develop predictive clustering models to guide marketing strategies.

### **Key Findings**
- Customers with higher income spend significantly more.  
- Loyalty and engagement vary by segment.  
- Campaign acceptance rates differ, requiring personalized approaches.  
- Data-driven segmentation enhances marketing ROI and customer satisfaction.

---

##  Methodology

### **1. RFM Analysis**
RFM segmentation evaluates customers based on:
- **Recency:** How recently a customer made a purchase.  
- **Frequency:** How often the customer makes purchases.  
- **Monetary:** How much the customer spends.  

#### **Why RFM?**
- Provides interpretable, actionable customer segments.  
- Helps prioritize marketing efforts.  
- Improves personalization and retention strategies.

---

### **2. K-Means Clustering**

K-Means is an unsupervised learning algorithm used to group customers into clusters based on demographic and behavioral attributes.

**Steps Involved:**
1. Data cleaning and feature engineering.  
2. Feature selection (age, income, marital status, number of kids, total expenses, accepted campaigns, etc.).  
3. Determining the optimal number of clusters using the **Elbow Method**.  
4. Training and evaluating the clustering model.  
5. Analyzing cluster characteristics for marketing insights.

**Resulting Clusters:**
| Cluster | Description |
|----------|--------------|
| **Cluster 1** | Married customers with modest income, more children, and lower spending. |
| **Cluster 2** | Single or fewer children, higher income, higher total expenses, strong engagement. |

**Interpretation:**
Businesses can target **Cluster 2** with premium offers and loyalty programs, while **Cluster 1** may respond better to value-based promotions.

---

##  Data Preparation

### **Data Cleaning Process**
- Removed redundant columns (`Z_CostContact`, `Z_Revenue`).  
- Handled missing values by imputation.  
- Calculated new features:
  - `Age` from `Year_Birth`  
  - `Total_Expenses` from product-related columns  
  - `Total_Kids_Number` combining kids and teens at home  
  - `Total_Purchases_Number` and `Total_Accepted_Campaigns`  
- Encoded categorical variables:
  - `Education` → Postgraduate / Undergraduate  
  - `Marital_Status` → Single / Relationship  
- Capped outliers in `Income` and `Age`.

### **Feature Groups**
| Category | Variables |
|-----------|------------|
| **Customers** | ID, Age, Education, Marital Status, Income |
| **Products** | MntWines, MntFruits, MntMeatProducts, MntFishProducts, MntSweetProducts, MntGoldProds |
| **Promotions** | NumDealsPurchases, AcceptedCmp1–5, Response |
| **Places** | NumWebPurchases, NumCatalogPurchases, NumStorePurchases, NumWebVisitsMonth |

---

##  Analysis & Insights

### **Correlation Insights**
Features most correlated with **Total Expenses**:
1. Income  
2. Total Purchases Number  
3. Total Accepted Campaigns  

Low or minimal impact features:
- Marital Status  
- Number of Kids  
- Age  

### **Behavioral Insights**
- High-income customers exhibit higher spending patterns.  
- Customers with fewer children tend to spend more.  
- Tailored campaigns yield higher acceptance rates.  
- Customer loyalty and engagement increase with personalized incentives.

---

##  RFM vs K-Means Comparison

| Aspect | RFM Analysis | K-Means Clustering |
|--------|---------------|--------------------|
| **Approach** | Rule-based segmentation | Unsupervised ML segmentation |
| **Focus** | Recency, Frequency, Monetary values | Multiple behavioral and demographic features |
| **Interpretability** | Simple, intuitive | Requires analysis and domain knowledge |
| **Advantages** | Easy to implement, clear insights | Captures complex relationships |
| **Limitations** | Limited dimensions | Sensitive to K and initialization |

**Conclusion:**  
RFM provides quick, interpretable insights on loyalty and recency, while K-Means offers deeper, multidimensional segmentation.  
Together, they create a comprehensive view of customer behavior.

---

##  Tools & Technologies

| Category | Tools Used |
|-----------|------------|
| Language | Python |
| Libraries | pandas, numpy, matplotlib, seaborn, scikit-learn |
| Models | RFM Segmentation, K-Means Clustering |
| Visualization | Matplotlib, Seaborn |
| Environment | Jupyter Notebook |

---

##  Results Summary

- **RFM Analysis:** Classified customers into loyalty segments for better targeting.  
- **K-Means Clustering:** Identified two primary clusters with distinct demographic and behavioral profiles.  
- **Actionable Insights:** Provided strategies for campaign optimization, loyalty building, and customer retention.  



