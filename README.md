# 🛒 E-Commerce Customer Segmentation & RFM Analytics Dashboard

> An end-to-end data analysis and business intelligence project focused on grouping e-commerce customers using the **RFM (Recency, Frequency, Monetary)** framework to optimize marketing strategies and customer retention.

---

## 🔗 Live Interactive Dashboard
You can explore the interactive Google Looker Studio dashboard here:
👉 **[View Live Dashboard](https://datastudio.google.com/reporting/de8eba21-f6e1-4dd0-9bf1-77e56642b97a)**

---

## 📊 Project Overview
Understanding customer behavior is crucial for modern e-commerce businesses. This project processes transactional data to classify customers into 10 distinct behavioral segments (such as *Champion*, *Loyal Customers*, *At Risk*, and *Hibernating*). By leveraging Python for data preprocessing/RFM scoring and Google Looker Studio for data visualization, this project bridges raw data engineering with actionable business insights.

### **Project Objectives & Benefits:**
* **Customer Value Identification:** Maps the entire user base into 10 strategic behavioral segments based on their shopping activity (*Recency*, *Frequency*, *Monetary*).
* **Data-Driven Strategy:** Empowers management and business teams to formulate specific, actionable initiatives—such as VIP loyalty programs for the *Champion* segment and targeted win-back campaigns to re-engage customers in the *At Risk* group.
* **Comprehensive Visualization:** Delivers a real-time summary of business performance—ranging from total unique customers and total revenue to average frequency and recency per segment, enhanced with interactive filters.

---

## 🛠️ Tech Stack & Tools
* **Python (Google Colab):** Data cleaning, aggregation, feature engineering, and RFM scoring using `pandas`, `numpy`, and `matplotlib`.
* **Google Drive:** Data storage and pipeline management.
* **Google Looker Studio:** Business intelligence dashboarding, custom metric transformation, and interactive filtering.

---

## ⚙ Methodology & RFM Scoring Process
1. **Data Preprocessing:** Cleaned the raw online retail dataset, handled missing values, filtered out invalid transactions (quantity/price $\le 0$), and converted date formats.
2. **RFM Metric Extraction:** Aggregated transactional records per `customer_id`:
   * **Recency:** Days elapsed since the customer's last purchase.
   * **Frequency:** Total number of unique orders placed.
   * **Monetary:** Total spending value (`quantity * price`).
3. **Scoring & Binning:** Assigned scores from 1 to 5 using dynamic quantile ranking (`pd.qcut`) to handle data skewness.
4. **Segment Mapping:** Classified customers into 10 tactical segments based on their Recency and Frequency scores.

---

## 📂 Repository Structure
```text
├── Project_User_Segmentation/
│   ├── rfm_customer_segments.csv       # Processed dataset ready for BI
│   ├── customer_segmentation.ipynb     # Jupyter/Colab notebook with Python code
│   └── README.md                       # Project documentation
```

---

## 🚀 How to Run the Code
1. Open the **Google Colab** notebook (`customer_segmentation.ipynb`).
2. Ensure your dataset is placed in your Google Drive under:  
   `My Drive/Project User Segmentation/Salinan Online Retail Data.csv`
3. Run the cells sequentially to perform data cleansing, RFM aggregation, and generate the exported CSV file.

---

## 💡 Key Business Insights
* **Hibernating (Largest Segment):** Comprises a major portion of the customer base, requiring aggressive re-engagement campaigns.
* **Champion & Loyal Customers:** High-value segments that drive sustainable revenue, best targeted with exclusive VIP perks and early access.
* **At Risk:** High historical value customers who haven't purchased recently, requiring immediate win-back strategies.

---
*Created by Elieser Pasaribu — Aspiring Data Analyst / Data Scientist / Machine Learning*
