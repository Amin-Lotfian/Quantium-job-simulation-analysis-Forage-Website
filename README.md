# Quantium Virtual Internship – Retail Strategy and Analytics

This repository contains my work from the **Quantium Virtual Internship**, focused on real-world data analysis in the retail sector. The project is split into two key tasks involving customer behavior analysis and experimentation design to assess a marketing campaign’s effectiveness.

---

## 📊 Task 1: Data Preparation and Customer Analytics

**Objective**: Clean and analyze chip sales data to understand customer purchasing behavior.

**Key Activities**:
- Loaded and cleaned transaction and customer data using **Pandas**.
- Filtered out irrelevant products (non-chip items) and removed anomalies (e.g., bulk purchases).
- Engineered features such as:
  - `PACK_SIZE` from product names
  - `BRAND` categorization from text fields
- Merged customer and transaction data for full customer profiles.
- Segmented users by `LIFESTAGE` and `PREMIUM_CUSTOMER` classification.
- Performed exploratory data analysis (EDA) to reveal:
  - Segment-wise sales contributions
  - Average chip quantity per customer
  - Average unit price per customer type

**Insights**:
- Highest chip sales came from **Budget–Older Families** and **Mainstream–Young Singles/Couples**.
- Families generally purchased more chips per customer.
- **Premium** customers paid higher unit prices on average.

---

## 🧪 Task 2: Experimentation and Uplift Testing

**Objective**: Evaluate a marketing campaign trial run in three stores using control groups and uplift analysis.

**Approach**:
- Identified matching control stores based on similarity in:
  - Total monthly sales
  - Monthly customer count
- Used **correlation** and **magnitude distance** metrics to score similarity.
- Scaled control store metrics to match baseline differences.
- Performed **uplift analysis** using:
  - Visual time-series comparisons
  - Percentage difference calculations
  - T-tests and confidence intervals

**Findings**:
- **Store 77**: Statistically significant uplift in both sales and customers.
- **Store 86**: Significant increase in customer count, but not sales — possibly due to promotions/discounting.
- **Store 88**: Similar trends observed using consistent methodology.

---

## 🛠 Tools & Technologies

- **Language**: Python
- **Libraries**: `pandas`, `matplotlib`, `seaborn`, `scipy`, `numpy`, `datetime`
- **Techniques**: Data cleaning, feature engineering, segmentation, uplift modeling, t-tests

---

## 📁 Repository Structure

- `Task 1.pdf`: Customer analytics and feature engineering
- `Task 2.pdf`: Experiment design and impact evaluation

---

## 📌 Highlights

- Built end-to-end analytics workflows in Python
- Converted business questions into data-driven decisions
- Delivered statistically backed insights to support marketing strategy
