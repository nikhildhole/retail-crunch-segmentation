# 📊 Customer Segmentation & Churn Prediction

## 🔹 Project Overview

This project performs **customer segmentation** and **churn prediction** using the **Online Retail II dataset**.

The goal is to:

- Segment customers based on purchasing behavior using **RFM analysis**
- Predict customer churn using supervised machine learning
- Generate actionable business insights for retention strategies

---

## 🔹 Business Problem

Retail businesses need to:

- Identify high-value customers
- Detect customers at risk of churning
- Allocate marketing resources efficiently
- Improve customer lifetime value (CLV)

This project provides a complete data-driven pipeline to address these challenges.

---

## 🔹 Dataset

**Online Retail II Dataset**

Contains transactional data including:

- Invoice
- StockCode
- Quantity
- InvoiceDate
- Price
- Customer ID
- Country

Each row represents a transaction line item.

---

## 🔹 Project Workflow

### 1️⃣ Data Cleaning

- Removed missing `Customer ID`
- Removed duplicates using business keys
- Removed cancellations and invalid transactions
- Removed non-product stock codes (POST, D, M)
- Converted data types correctly
- Prevented data leakage

---

### 2️⃣ Feature Engineering (RFM)

Created customer-level features:

- **Recency** – Days since last purchase
- **Frequency** – Number of unique invoices
- **Monetary** – Total spend

Applied:

- Log transformation
- Standard scaling

---

### 3️⃣ Customer Segmentation (Unsupervised Learning)

Algorithms tested:

- K-Means (Primary)
- Hierarchical Clustering (Validation)

#### Optimal Clusters:

K = 4 (based on Elbow Method & Silhouette Score)

#### Final Segments:

- 🏆 VIP Customers
- 🔵 Active Regular Customers
- 🟠 At-Risk Customers
- 🔴 Lost Customers

---

### 4️⃣ Churn Prediction (Supervised Learning)

Churn defined as:

> No purchase in the last 180 days

Models tested:

- Logistic Regression
- Random Forest
- XGBoost

⚠ Data leakage was identified and corrected by removing Recency from predictive features.

#### Model Comparison

| Model               | ROC-AUC | Recall (Churn) | F1-Score |
| ------------------- | ------- | -------------- | -------- |
| Logistic Regression | 0.78    | 0.65           | 0.65     |
| Random Forest       | 0.69    | 0.58           | 0.57     |
| XGBoost             | 0.75    | 0.64           | 0.63     |

✅ Final Model: **Logistic Regression**

Reason:

- Best ROC-AUC
- Highest recall
- Most interpretable

---

## 🔹 Key Insights

| Segment        | Avg Monetary | Avg Churn Probability | Strategy              |
| -------------- | ------------ | --------------------- | --------------------- |
| VIP Customers  | Very High    | Very Low              | Retain & Upsell       |
| Active Regular | Medium       | Moderate              | Engagement Campaigns  |
| At-Risk        | High         | Moderate              | Immediate Retention   |
| Lost           | Low          | High                  | Low-Cost Reactivation |

### 🔥 High-Value Customers at Risk

Customers with:

- High Monetary value
- High churn probability

These represent the most important retention targets.

---

## 🔹 Business Recommendations

- Focus retention campaigns on **At-Risk Customers**
- Use loyalty programs for **VIP Customers**
- Use automated reactivation for **Lost Customers**
- Optimize marketing spend using churn probability ranking

---

## 🔹 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib / Seaborn

---

## 🔹 How to Run

1. Clone the repository
2. Open folder in vs code
3. Open Customer_Segmentation_and_Churn_Prediction.ipynb in run all.

## 🔹 Project Structure

```
.
├── Customer_Segmentation_and_Churn_Prediction.ipynb
├── online_retail_II.csv
├── README.md
```

---

## 🔹 Learning Highlights

- End-to-end ML pipeline
- RFM-based segmentation
- Clustering validation
- Data leakage detection & correction
- Model comparison framework
- Business-driven ML interpretation

---

## 🔹 Future Improvements

- Cross-validation
- Threshold optimization
- Hyperparameter tuning
- SHAP interpretability
- Deployment as a dashboard

---

# 📌 Conclusion

This project demonstrates a complete machine learning workflow:

From raw transactional data → customer segmentation → churn prediction → business strategy.

It combines technical rigor with business applicability.
