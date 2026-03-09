# 📊 Retail Customer Segmentation & Churn Prediction

End-to-end **Data Analytics & Machine Learning project** that analyzes retail transaction data to identify **customer segments** and predict **customer churn risk**.

This project demonstrates a complete pipeline from **data cleaning → feature engineering → customer segmentation → churn prediction → business insights**.

---

# 🚀 Project Objectives

Retail businesses must understand customer behavior to improve retention and marketing efficiency.

This project aims to:

- Identify **high-value customers**
- Detect **customers at risk of churn**
- Segment customers based on purchasing behavior
- Provide **data-driven marketing strategies**

---

# 📁 Dataset

**Online Retail II Dataset**

Transactional dataset containing retail purchase records.

### Key Features

- `Invoice` – Invoice number
- `StockCode` – Product code
- `Quantity` – Quantity purchased
- `InvoiceDate` – Transaction date
- `Price` – Unit price
- `Customer ID` – Unique customer identifier
- `Country` – Customer location

Each row represents a **single transaction line item**.

---

# ⚙️ Project Pipeline

## 1️⃣ Data Cleaning

Steps performed:

- Removed missing **Customer IDs**
- Removed **duplicate transactions**
- Removed **cancelled invoices**
- Removed **invalid price and quantity values**
- Removed **non-product stock codes**
- Fixed incorrect **data types**

This ensures the dataset is reliable for analysis.

---

## 2️⃣ Feature Engineering (RFM Analysis)

Customer behavior was summarized using **RFM metrics**:

| Feature       | Description              |
| ------------- | ------------------------ |
| **Recency**   | Days since last purchase |
| **Frequency** | Number of purchases      |
| **Monetary**  | Total spending           |

Additional preprocessing:

- Log transformation to reduce skew
- Standard scaling for clustering algorithms

---

# 🔍 Customer Segmentation

Customer segmentation was performed using **unsupervised machine learning**.

### Algorithms Tested

- K-Means Clustering
- Hierarchical Clustering (validation)

### Optimal Clusters

Using:

- **Elbow Method**
- **Silhouette Score**

The optimal number of clusters was:

**K = 4**

---

## 📊 Customer Segments

| Segment                         | Description                                |
| ------------------------------- | ------------------------------------------ |
| 🏆 **VIP Customers**            | High spending and loyal customers          |
| 🔵 **Active Regular Customers** | Frequent buyers with moderate spending     |
| 🟠 **At-Risk Customers**        | Previously active but declining engagement |
| 🔴 **Lost Customers**           | Inactive customers with high churn risk    |

These segments allow businesses to create **targeted marketing strategies**.

---

# 🤖 Churn Prediction

Customer churn was defined as:

> No purchase within the last **180 days**

A binary churn label was created for supervised modeling.

---

## Models Evaluated

- Logistic Regression
- Random Forest
- XGBoost

### Model Performance

| Model               | ROC-AUC | Recall (Churn) | F1 Score |
| ------------------- | ------- | -------------- | -------- |
| Logistic Regression | 0.78    | 0.65           | 0.65     |
| Random Forest       | 0.69    | 0.58           | 0.57     |
| XGBoost             | 0.75    | 0.64           | 0.63     |

### Final Model

✅ **Logistic Regression**

Reasons:

- Highest ROC-AUC
- Highest Recall
- Interpretable model
- Lower risk of overfitting

---

# 📈 Key Business Insights

| Segment        | Avg Spend | Churn Risk | Strategy                     |
| -------------- | --------- | ---------- | ---------------------------- |
| VIP Customers  | Very High | Very Low   | Loyalty rewards & upselling  |
| Active Regular | Medium    | Moderate   | Engagement campaigns         |
| At-Risk        | High      | Moderate   | Targeted retention campaigns |
| Lost           | Low       | High       | Low-cost reactivation        |

---

## 🔥 High-Value Customers at Risk

Customers with:

- **High Monetary value**
- **High churn probability**

These customers represent the **highest priority for retention strategies**.

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn
- Jupyter Notebook

---

# 📂 Project Structure

```
.
├── Customer_Segmentation_and_Churn_Prediction.ipynb
├── online_retail_II.csv
├── README.md
```

---

# ▶️ How to Run

### 1️⃣ Clone the repository

```
git clone https://github.com/nikhildhole/retail-crunch-segmentation.git
```

### 2️⃣ Install dependencies

```
pip install -r requirements.txt
```

### 3️⃣ Open the notebook

Run:

```
Customer_Segmentation_and_Churn_Prediction.ipynb
```

---

# 📚 Learning Highlights

This project demonstrates:

- End-to-end **machine learning workflow**
- **RFM-based customer segmentation**
- **Unsupervised learning (K-Means)**
- **Churn prediction modeling**
- **Data leakage detection & prevention**
- **Business-focused data science insights**

---

# 🔮 Future Improvements

Possible extensions:

- Cross-validation for model robustness
- Hyperparameter tuning
- SHAP model interpretability
- Interactive dashboards (Power BI / Streamlit)
- Real-time churn prediction API

---

# 📌 Conclusion

This project demonstrates how machine learning can help businesses:

- Understand customer behavior
- Predict churn risk
- Improve customer retention
- Optimize marketing strategies

By combining **customer segmentation with churn prediction**, businesses can make **data-driven decisions to maximize customer lifetime value (CLV)**.
