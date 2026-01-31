# 🍽️ Food Delivery Data Analysis

This project is a **Food Delivery Data Analysis** task completed as part of the  
**Innomatics Research Labs – Advanced GenAI Internship Entrance Test**.

The project demonstrates end-to-end data handling by integrating **CSV, JSON, and SQL** data sources and performing meaningful analysis using **Python, Pandas, and SQL concepts**.

---

## 🎯 Project Objective

The key objectives of this project are to:

- Load data from **multiple file formats** (CSV, JSON, SQL)
- Merge datasets into a **single, clean analytical dataset**
- Perform analysis to understand:
  - 📊 Revenue trends
  - 👤 User behavior
  - 🌍 City-wise performance
  - 🍕 Cuisine-wise insights
  - ⭐ Membership impact (Gold vs Regular)

---

## 🗂️ Project Structure

food-delivery-data-analysis/
│
├── datasets/
│ ├── orders.csv # Order transaction data
│ ├── users.json # User details
│ └── restaurants.sql # Restaurant & cuisine data
│
├── food_delivery_data_analysis.ipynb # Complete analysis notebook
├── final_food_delivery_dataset.csv # Final merged dataset
└── README.md # Project documentation

## 📊 Data Sources

### 🟢 orders.csv  
Contains transactional order information including:
- `order_id`
- `user_id`
- `restaurant_id`
- `order_date`
- `total_amount`

### 🟢 users.json  
Stores user-level data such as:
- User name
- City
- Membership type (Gold / Regular)

### 🟢 restaurants.sql  
Contains restaurant master data including:
- Restaurant name
- Cuisine type
- Restaurant rating

---

## 🔗 Data Merging Logic

- `orders.csv` is merged with `users.json` using **user_id**
- The result is merged with `restaurants.sql` using **restaurant_id**
- A **LEFT JOIN** strategy is applied to ensure **all orders are retained**

---

## 📅 Date Handling

Order dates appear in mixed formats and are handled using:

```python
pd.to_datetime(
    final_df["order_date"],
    dayfirst=True,
    format="mixed",
    errors="coerce"
)

🛠️ Tools & Technologies Used

🐍 Python 3

📘 Pandas

🗄️ SQLite

🧮 SQL

☁️ Google Colab

Note:
Although MySQL was mentioned in the instructions, SQLite is used to execute the provided .sql file locally for simplicity and portability.

📁 Key Project Files

food_delivery_data_analysis.ipynb
→ Complete notebook containing data loading, merging, and analytical insights

final_food_delivery_dataset.csv
→ Final merged dataset used as the single source of truth for all analysis

▶️ How to Use

Clone the repository

Open the notebook in Google Colab or Jupyter Notebook

Run the cells sequentially to reproduce the analysis

👤 Author

Kumar Gaurav
Advanced GenAI Internship Entrance Test Submission
Innomatics Research Labs

📧 Email: kumartuntun123789@gmail.com

---

✨ **This project reflects practical experience in real-world data integration and exploratory data analysis.**
