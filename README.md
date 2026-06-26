# 📱 PhonePe Transaction Analytics Dashboard — Power BI Project

A complete **Business Intelligence and Data Analytics project** that analyzes digital payment transactions using **SQL, Excel, and Microsoft Power BI**.

This project focuses on understanding **transaction performance, customer spending behavior, payment trends, and transaction failure patterns** using an interactive Power BI dashboard.

The analysis is performed on a real-world inspired **PhonePe transaction dataset containing 500 users and 2000 transactions** to generate meaningful business insights and support data-driven decision-making.

---

# 🎯 Business Problem

Digital payment platforms handle thousands of transactions every day. However, businesses need clear insights into:

* Customer payment behavior
* Transaction growth patterns
* Popular payment methods
* High-performing categories and locations
* Reasons behind failed transactions

The objective of this project is to answer:

### 📌 Key Business Questions

✔ How is PhonePe performing overall?

✔ Which payment methods are most preferred by customers?

✔ Which categories contribute the highest transaction value?

✔ Which cities and states generate maximum transactions?

✔ What are the major reasons behind payment failures?

✔ How can transaction success rates be improved?

---

# 🗂️ Project Files

| File                                | Description                                                  |
| ----------------------------------- | ------------------------------------------------------------ |
| 📊 PhonePe_Dataset.xlsx             | Raw transaction dataset containing users and payment records |
| 📈 PhonePe_Analytics_Dashboard.pbix | Complete Power BI dashboard file                             |
| 📘 README.md                        | Project documentation                                        |
| 🖼️ Dashboard Screenshots           | Dashboard previews                                           |

---

# 🛠️ Tools & Technologies Used

| Tool                  | Purpose                                                  |
| --------------------- | -------------------------------------------------------- |
| 🟦 Microsoft Power BI | Dashboard creation, visualization, and business insights |
| 🟨 SQL                | Data extraction, transformation, and analytical queries  |
| 📊 Excel              | Dataset preparation and initial exploration              |
| 📐 DAX                | Calculated measures and KPI creation                     |
| 📊 Data Visualization | Interactive charts and reporting                         |

---

# 📊 Dashboard Pages

The dashboard contains **3 interactive pages**:

---

# 📌 HOME PAGE  - PHONEPE 

<img width="482" height="272" alt="Home Page" src="https://github.com/user-attachments/assets/ad365c67-6a58-4ac3-8fc8-513640d5655b" />


---

# 📌 PAGE 1 — Executive Payment Overview

<img width="480" height="271" alt="Executive Payment overview" src="https://github.com/user-attachments/assets/bcc97634-6a1c-42d5-871c-50282b8eda6e" />

### Objective:

Provide an overall view of PhonePe transaction performance.

### KPIs:

* Total Users
* Total Transactions
* Total Transaction Value
* Success Rate

### Visual Analysis:

📌 Payment Method Analysis

* Distribution of transactions across payment channels

📌 Category Analysis

* Transaction value comparison across categories

📌 Transaction Trend

* Monthly transaction performance

📌 State Performance

* Identify high-performing regions

---

# 📌 PAGE 2 — Customer & Spending Insights

<img width="480" height="270" alt="Customer   Merchnat Insights" src="https://github.com/user-attachments/assets/166208e4-b711-489a-af67-2f3a9da754fe" />


### Objective:

Analyze customer behavior and spending patterns.

### KPIs:

* Average Transaction Value
* Premium Users
* Active Cities

### Visual Analysis:

📌 User Type Distribution

* Premium, Regular, and Business customer analysis

📌 Age Group Analysis

* Customer distribution by age categories

📌 Category Transactions

* Identify popular spending categories

📌 Top Cities

* Find cities generating maximum transactions

---

# 📌 PAGE 3 — Transaction Failure & Risk Analysis

<img width="600" height="400" alt="Transaction Failure   Risk" src="https://github.com/user-attachments/assets/40b6bc21-407c-4c59-97b1-bb851f581b3a" />



### Objective:

Understand payment failures and improve transaction reliability.

### KPIs:

* Total Transactions
* Failed Transactions
* Failure Rate

### Visual Analysis:

📌 Success vs Failed Transactions

📌 Failure Reason Analysis

📌 Payment Method Failure Analysis

📌 Risk Identification

---

# 📐 DAX Measures Created

## Total Users

```DAX
Total Users =
DISTINCTCOUNT(Dim_User[User_ID])
```

---

## Total Transactions

```DAX
Total Transactions =
COUNT(Fact_Transactions[Transaction_ID])
```

---

## Total Transaction Value

```DAX
Total Transaction Value =
SUM(Fact_Transactions[Amount])
```

---

## Success Rate

```DAX
Success Rate =
DIVIDE(
    CALCULATE(
        COUNT(Fact_Transactions[Transaction_ID]),
        Fact_Transactions[Status]="Success"
    ),
    [Total Transactions]
)
```

---

## Average Transaction Value

```DAX
Average Transaction =
AVERAGE(Fact_Transactions[Amount])
```

---

## Premium Users

```DAX
Premium Users =
CALCULATE(
    DISTINCTCOUNT(Dim_User[User_ID]),
    Dim_User[User_Type]="Premium"
)
```

---

## Failed Transactions

```DAX
Failed Transactions =
CALCULATE(
    COUNT(Fact_Transactions[Transaction_ID]),
    Fact_Transactions[Status]="Failed"
)
```

---

## Failure Rate

```DAX
Failure Rate =
DIVIDE(
    [Failed Transactions],
    [Total Transactions]
)
```

---

# 📈 Dashboard Insights

* ✔ Analyzed **500 users and 2000 transactions**

* ✔ Achieved an overall transaction success rate of **88.85%**

* ✔ Identified major transaction failure reasons affecting payment success

* ✔ Compared customer preferences across different payment methods

* ✔ Analyzed spending behavior across multiple categories

* ✔ Identified high-performing cities and states

* ✔ Evaluated customer segments based on user type and age groups

---

# 🔍 Key Business Findings

### Payment Performance

* Majority of transactions were completed successfully.
* Failed transactions represented a smaller but important portion requiring improvement.

### Customer Behavior

* Premium users contributed significantly to transaction activity.
* Different age groups showed different transaction patterns.

### Regional Insights

* Certain cities generated higher transaction volumes compared to others.

### Payment Risk

* Failure reason analysis helped identify areas where payment reliability can be improved.

---

# 🎯 Final Conclusion

The **PhonePe Transaction Analytics Dashboard** demonstrates how raw payment data can be transformed into meaningful business intelligence.

Using **SQL, Power BI, and DAX**, the project analyzed transaction performance, customer behavior, regional trends, and payment risks.

The dashboard provides actionable insights that can help digital payment platforms:

✅ Improve payment success rates
✅ Understand customer preferences
✅ Optimize transaction experience
✅ Make data-driven business decisions

---

# 🚀 How To Run The Project

### Step 1:

Install required tools:

* Microsoft Power BI Desktop
* SQL Database
* Microsoft Excel

### Step 2:

Load the dataset into SQL/Power BI.

### Step 3:

Open:

```
PhonePe_Analytics_Dashboard.pbix
```

### Step 4:

Refresh the dataset and explore interactive dashboards.

---

# ✅ Project Checklist

* ✔ Dataset Preparation
* ✔ SQL Analysis
* ✔ Data Modeling
* ✔ DAX Measures
* ✔ KPI Development
* ✔ Interactive Dashboard
* ✔ Customer Analytics
* ✔ Transaction Analysis
* ✔ Failure Analysis
* ✔ Business Insights

---

# 👨‍💻 Author

**Shruti Bhawsar**

📍 Ahmedabad, Gujarat, India

---

⭐ If you found this project useful, consider giving it a star and sharing feedback.

📊 **Data Analytics | Business Intelligence | Data-Driven Decisions**
