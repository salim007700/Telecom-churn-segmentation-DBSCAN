# 🚀 Telecom Customer Segmentation & Churn Intelligence (DBSCAN)

> Turning raw customer data into actionable revenue and retention strategy

---

## 📌 Overview

Customer churn is one of the biggest revenue challenges in the telecom industry.
This project applies **unsupervised machine learning (DBSCAN clustering)** to segment customers based on real behavioral patterns and uncover:

* 🔴 High-risk churn segments
* 🟢 Loyal, high-value customers
* 💰 Upsell and cross-sell opportunities

Unlike traditional models, this approach **does not rely on predefined labels**, making it powerful for discovering hidden patterns in customer behavior.

---

## 🎯 Business Problem

Telecom companies often treat all customers the same.

👉 This leads to:

* Inefficient marketing spend
* Missed retention opportunities
* Lost revenue from unnoticed churn signals

---

## 💡 Solution

This project builds a **data-driven segmentation system** that:

* Groups customers into natural behavioral clusters
* Measures churn risk within each segment
* Translates insights into **clear business actions**

---

## 🧠 Key Results

| Metric                     | Insight                |
| -------------------------- | ---------------------- |
| 🔴 High-risk clusters      | ~50% churn rate        |
| 👥 Largest at-risk segment | ~2600 customers        |
| 🟢 Low-risk segments       | <15% churn             |
| ⚠️ Noise (outliers)        | Identified and handled |

---

## 📊 Example Output

### 🔥 Churn Risk by Cluster

* Clear identification of high-risk customer segments
* Prioritization of retention efforts

### 📈 Cluster Behavior Heatmap

* Visual comparison of:

  * Churn rate
  * Monthly charges
  * Tenure

### 👥 Customer Segments

* Distinct behavioral groupings across the customer base

---

## ⚙️ Methodology

### 1. Data Preparation

* Selected key features:

  * Tenure in Months
  * Monthly Charges
  * Total Charges
  * Contract Type
  * Unlimited Data
* Applied **one-hot encoding**
* Standardized data using **StandardScaler**

---

### 2. Clustering (DBSCAN)

Tested multiple distance metrics:

| Metric      | Clusters | Noise |
| ----------- | -------- | ----- |
| Euclidean   | 7        | 65    |
| Manhattan ✅ | 7        | 16    |
| Cosine      | 1        | 0     |

👉 **Final Choice: Manhattan Distance**

* Balanced segmentation
* Minimal noise
* Best real-world representation

---

### 3. Data Cleaning

* Removed noise points (`cluster = -1`)
* Eliminated insignificant clusters (<50 customers)

---

### 4. Business Layer

For each cluster, computed:

* Average monthly charge
* Average tenure
* Total revenue contribution
* Churn rate
* Contract behavior

---

## 💰 Business Impact

### 🔴 Retention Strategy

Target high-risk clusters:

* Discount offers
* Contract upgrades
* Loyalty programs

---

### 🟢 Revenue Growth

Focus on low-risk clusters:

* Upsell premium plans
* Bundle services
* Increase ARPU

---

### ⚠️ Anomaly Detection

Noise points reveal:

* Unusual behavior
* Potential early churn signals

---

## 📈 Visualizations

* Churn Rate by Cluster
* Customer Distribution
* Cluster Behavior Heatmap

> Note: Scatter plots were intentionally minimized due to low interpretability for high-dimensional clustering.

---

## 🧪 Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn (DBSCAN, preprocessing)
* Matplotlib

---

## 🧠 Key Learnings

* DBSCAN can uncover **natural customer segments without labels**
* Distance metric selection significantly affects clustering quality
* Combining clustering with business metrics transforms insights into **real decisions**

---

## 📂 Project Structure

```bash
📁 telecom-churn-clustering/
│
├── 📊 data/
├── 📓 notebook.ipynb
├── 📈 visualizations/
├── 📄 README.md
```

---

## 🚀 How to Run

```bash
pip install -r requirements.txt
jupyter notebook
```

---

## 🔮 Future Improvements

* Add churn prediction model (supervised learning)
* Build interactive dashboard (Power BI / Tableau)
* Deploy segmentation API

---

## 🤝 Let's Connect

If you're working on:

* Customer analytics
* Telecom data
* Machine learning projects

Feel free to connect or collaborate.

---

⭐ If you found this useful, consider giving it a star!
