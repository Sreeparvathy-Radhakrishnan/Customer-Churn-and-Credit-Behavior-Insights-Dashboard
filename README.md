# 🏦 Customer Churn and Credit Behavior Insights Dashboard

## 📘 Project Overview  
This Tableau project analyzes customer churn patterns and credit behavior using the BankChurners dataset.The goal is to uncover insights into customer demographics, financial activity, and behavioral trends that influence churn.Through key metrics and interactive visualizations, this dashboard enables data-driven decision-making for **customer retention and credit management strategies**.  


## 💻 Tech Stack  
- Tool : Tableau Desktop / Tableau Public  
- Data Processing : Microsoft Excel  
- Language : Calculated Fields in Tableau (for KPI logic)  
- Visualization Type : Single-page interactive dashboard  


## 🗂 Data Source  
- Dataset Name : `BankChurners.csv`  
- Source : Kaggle – Bank Customer Churn Prediction Dataset  
- Rows : 10,127  
- Columns : 23  
- Key Fields :**  
  - `Attrition_Flag`, `Customer_Age`, `Gender`, `Education_Level`, `Income_Category`,  
    `Card_Category`, `Credit_Limit`, `Total_Trans_Amt`, `Total_Trans_Ct`,  
    `Months_Inactive_12_mon`, `Avg_Utilization_Ratio`  


## 🧹 Data Cleaning and Transformation  
Performed using **Excel** and **Tableau Data Pane**:  
1. Removed irrelevant columns like `Naive_Bayes_Classifier_*` fields.  
2. Renamed columns for better readability.  
3. Checked for missing values and standardized categories.  
4. Created calculated fields in Tableau for KPIs such as:  
   - **Churn Rate (%)**  
   - **Average Transaction Amount**  
   - **Total Customer** 


## 💡 Business Problem (Key Questions)  
1. What percentage of customers are leaving the bank (churn rate)?  
2. Which customer demographics show higher churn?  
3. How does spending behavior relate to churn and credit utilization?  
4. What income and education groups hold the highest credit limits?  
5. Which card categories are most preferred by customers?  
6. What factors influence customer inactivity and retention risk?  


## 🎯 Goal of the Dashboard  
To provide a **comprehensive view** of customer churn behavior and financial activity, enabling stakeholders to:  
- Identify at-risk customer segments  
- Understand behavioral trends by demographics and income  
- Develop targeted marketing and retention strategies  


## 📊 Dashboard Overview  
The **Customer Churn and Credit Behavior Insights Dashboard** is a single-page Tableau dashboard consisting of:  
- **5 Interactive Visuals**  
- **3 Key KPIs**  
- **5 Filters** for detailed exploration  <br><br>
[!Dashboard Image](https://github.com/Sreeparvathy-Radhakrishnan/Customer-Churn-and-Credit-Behavior-Insights-Dashboard/blob/main/Dashboard%20Image.png)
---

## 🧭 Walkthrough of Key Visuals  

### 🔹 1. Average Credit Limit by Education Level  
**Rows:** `Education_Level`  
**Columns:** `AVG(Credit_Limit)`  
**Aggregation:** Average  
**Insight:** Customers with higher education levels tend to have higher credit limits, suggesting a correlation between education and financial trustworthiness.  
**Business Value:** Helps design personalized credit limit offers based on education segment.  


### 🔹 2. Total  Transactions vs Transaction Amount  
**Rows:** `AVG(Total_Trans_Ct)`  
**Columns:** `AVG(Total_Trans_Amt)`  
**Aggregation:** Average  
**Insight:** Shows how frequently customers transact relative to their total spending. High-frequency, high-amount customers represent high-value users.  
**Business Value:** Identifies potential premium customers and usage intensity.  


### 🔹 3. Churn by Income Category  
**Rows:** `Income_Category`  
**Columns:** `COUNT(Customer_Age)`  
**Aggregation:** Count  
**Insight:** Majority of customers belong to the **Less than $40K** and **$40K–$60K** income brackets.  
**Business Value:** Helps target mid-income customers with suitable financial products.  


### 🔹 4. Age Distribution by Churn Status  
**Rows:** `Customer_Age`  
**Columns:** `COUNT(Customer_Age)`  
**Color:** `Attrition_Flag`  
**Aggregation:** Count  
**Insight:** Churn is higher among **middle-aged groups (40–55 years)**, indicating possible dissatisfaction or better alternatives.  
**Business Value:** Enables targeted retention strategies for at-risk age groups.  


### 🔹 5. Churn by Card Category  
**Rows:** `Card_Category`  
**Columns:** `COUNT(Customer_Age)`  
**Aggregation:** Count  
**Insight:** The **Blue** card is the most common, followed by **Silver**. Premium cards (Gold, Platinum) have fewer customers but higher credit limits.  
**Business Value:** Supports marketing focus on promoting premium cards to loyal customers.  


## ⚙️ KPIs Used (Top Section)  

| KPI Name | Formula | Business Meaning |
|-----------|----------|------------------|
| **Total Customers** | `COUNT(ClientNum)` | Total number of customers in the dataset |
| **Churn Rate (%)** | `(COUNTIF(Attrition_Flag = 'Attrited Customer') / COUNT(ClientNum)) * 100` | Percentage of customers lost |
| **Average Transaction Amount** | `AVG(Total_Trans_Amt)` | Average total spending |


## 🎛 Filters Used  

| Filter Name | Field | Purpose |
|--------------|--------|----------|
| **Education Level** | `Education_Level` | Segment customers by education background |
| **Income Category** | `Income_Category` | Filter by financial group |
| **Card Category** | `Card_Category` | Analyze performance across card tiers |
| **Attrition Flag** | `Attrition_Flag` | Analyze performance of Attrited and Existing Customers |
| **Gender** | `Gender` | Analyze gender wise performance  |


## 🚀 Future Enhancements  
- Integrate **predictive modeling** (using Python or Tableau extensions) to forecast future churn.  
- Include **trend analysis over time** using historical transaction data.  
- Build **drill-through pages** for individual customer segments.  
- Add **RFM (Recency, Frequency, Monetary)** segmentation analysis.  


## 🏁 Conclusion  
This Tableau dashboard successfully uncovers key factors influencing customer churn and financial behavior. It helps business users visualize customer patterns, identify churn risks, and design targeted engagement strategies. The visual simplicity and KPI integration make it a **valuable analytical tool for customer retention and business growth**.  


## 🎥 Demo  
> Tableau Public Link:  [View Dashboard on Tableau Public](https://github.com/Sreeparvathy-Radhakrishnan/Customer-Churn-and-Credit-Behavior-Insights-Dashboard/blob/main/Customer%20Churn%20and%20Credit%20Behavior%20Insights%20Dashboard.twbx)


