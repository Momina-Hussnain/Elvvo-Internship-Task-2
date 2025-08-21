# Elvvo-Internship-Task-2
This project applies Recency, Frequency, and Monetary (RFM) analysis on an online sales dataset to segment customers into groups such as Champions, Loyal, At Risk, and Lost. Includes data cleaning, scoring, visualization, and marketing insights.
# 🛒 Customer Segmentation using RFM Analysis

This project applies **RFM (Recency, Frequency, Monetary) Analysis** to an online sales dataset.  
It segments customers into groups like *Champions*, *Loyal*, *Potential Loyalists*, *At Risk*, and *Lost*, enabling data-driven marketing strategies.

---

## 📌 What is RFM?

- **Recency (R):** How recently a customer made a purchase (lower = better).  
- **Frequency (F):** How often they purchase (higher = better).  
- **Monetary (M):** How much money they spend (higher = better).  

RFM is widely used in marketing analytics for customer segmentation.

---

## 📂 Dataset

The dataset used: **online_sales_dataset (1).csv**

Key fields:
- `CustomerID` → unique customer identifier  
- `InvoiceNo` → order/invoice number  
- `InvoiceDate` → date of transaction  
- `Quantity` → items purchased  
- `UnitPrice` → price per item  
- `TotalAmount` → computed as *Quantity × UnitPrice*  

---

## ⚙️ Steps in the Project

1. **Data Cleaning**
   - Removed missing IDs and invalid dates  
   - Removed cancellations (`InvoiceNo` starting with "C")  
   - Kept only positive transactions  

2. **Feature Engineering**
   - Added `TotalAmount` per transaction  
   - Defined snapshot date (max purchase + 1 day)  

3. **RFM Calculation**
   - Recency = days since last purchase  
   - Frequency = number of unique invoices  
   - Monetary = total amount spent  

4. **Scoring**
   - Divided each R, F, M into quintiles (1–5)  
   - Combined into RFM Score (e.g., 555 = best)  

5. **Segmentation**
   - Champions  
   - Loyal  
   - Potential Loyalists  
   - At Risk  
   - Lost  
   - Others  

6. **Visualization**
   - Bar chart of customer counts per segment  

---

## 📊 Example Output

- Cleaned transactions → `online_sales_clean.csv`  
- RFM table (with scores + segments) → `RFM_table_newdata.csv`  
- Segment chart → `rfm_segments_newdata.png`  


## 💡 Business Insights

- **Champions** → VIP rewards, exclusive offers, referral programs  
- **Loyal** → loyalty points, subscription models  
- **Potential Loyalists** → onboarding campaigns, upselling opportunities  
- **At Risk** → win-back discounts, limited-time offers  
- **Lost** → re-engagement campaigns, surveys to collect feedback  

---

## 🛠️ Tools & Libraries

- Python 3  
- Pandas  
- Matplotlib  

---

## ✨ Author
Internship Project — Customer Segmentation using RFM  
