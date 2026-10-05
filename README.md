# Superstore Sales & Profit Analysis 📊

## 📌 Project Overview

This project analyzes Superstore sales data to understand **sales performance, profitability, discount impact, regional performance, customer segments, shipping modes, and loss-making areas**.

The analysis was performed using Python to clean the data, engineer useful features, perform exploratory data analysis, and generate business-focused visualizations.

The main objective is to identify patterns that can help a business **increase profitability, manage discounts effectively, and identify underperforming areas**.

---

## 🎯 Business Problem

The business wants to understand:

* Which categories and sub-categories generate the most profit?
* Which regions and states perform well?
* Which customer segments contribute the most sales and profit?
* Does higher discounting affect profitability?
* Which shipping modes generate the most sales and profit?
* Which states and products contribute to losses?
* How can the business improve overall profitability?

---

## 🛠️ Tools & Technologies

* **Python**
* **Pandas** — Data cleaning and analysis
* **Matplotlib** — Data visualization
* **Seaborn** — Statistical visualization
* **Jupyter Notebook**
* **GitHub**

---

## 📂 Dataset

The project uses a Superstore sales dataset containing information about:

* Ship Mode
* Segment
* Country
* City
* State
* Postal Code
* Region
* Category
* Sub-Category
* Sales
* Quantity
* Discount
* Profit

The dataset contains approximately **10,000 transaction records**.

---

## 🧹 Data Cleaning

The following data-cleaning activities were performed:

* Checked dataset dimensions and column names
* Checked for duplicate records
* Checked for missing values
* Verified data types
* Examined numerical columns using descriptive statistics
* Validated Sales, Quantity, Discount, and Profit values
* Confirmed that negative Profit values represent loss-making transactions

---

## ⚙️ Feature Engineering

### Profit Margin

A new `profit_margin` column was created:

```python
df["profit_margin"] = (df["Profit"] / df["Sales"]) * 100
```

### Discount Category

Discounts were categorized into:

* No Discount
* Low Discount
* Medium Discount
* High Discount

### Profit Status

Transactions were classified as:

* **Profit**
* **Loss**

```python
df["Profit_Status"] = df["Profit"].apply(
    lambda x: "Profit" if x > 0 else "Loss"
)
```

---

## 📊 Exploratory Data Analysis

The following analyses were performed:

### 1. Overall Business KPIs

Calculated:

* Total Sales
* Total Profit
* Total Quantity
* Average Sales
* Average Profit
* Overall Profit Margin
* Number of Loss-Making Orders

### 2. Category & Sub-Category Analysis

Analyzed:

* Sales by Category
* Profit by Category
* Sales and Profit by Sub-Category
* Top-performing sub-categories
* Loss-making sub-categories

### 3. Discount vs Profit Analysis

Analyzed the relationship between:

**Discount → Profit**

A correlation analysis and scatter plot were used to understand whether higher discounts are associated with lower profitability.

### 4. Regional Analysis

Analyzed:

* Sales by Region
* Profit by Region
* Top-performing states
* Loss-making states

### 5. Customer Segment Analysis

Compared:

* Consumer
* Corporate
* Home Office

using Sales, Profit, Quantity, Average Sales, and Average Profit.

### 6. Ship Mode Analysis

Compared:

* Standard Class
* Second Class
* First Class
* Same Day

using order volume, sales, profit, and profit margin.

### 7. Correlation Analysis

A correlation matrix was created to study relationships between:

* Sales
* Quantity
* Discount
* Profit
* Profit Margin

### 8. Loss-Making Analysis

Identified:

* Loss-making orders
* Loss by category
* Loss by sub-category
* Loss by state
* Top 10 loss-making states

---

## 📈 Visualizations

The project includes the following key visualizations:

### Sales by Category

![Sales by Category](visualizations/sales_by_category.png)

### Profit by Sub-Category

![Profit by Sub-Category](visualizations/profit_by_subcategory.png)

### Discount vs Profit

![Discount vs Profit](visualizations/discount_vs_profit.png)

### Profit by Region

![Profit by Region](visualizations/profit_by_region.png)

### Top 10 Loss-Making States

![Top Loss-Making States](visualizations/top_loss_states.png)

---

## 🔍 Key Insights

The analysis highlights several important business patterns:

* Sales and profit do not always increase together.
* Some sub-categories generate significantly higher profit than others.
* Certain products and states contribute disproportionately to overall losses.
* Higher discount levels are generally associated with lower profitability.
* Customer segments differ in their contribution to sales and profit.
* Shipping modes can be compared not only by sales volume but also by profitability.
* Loss-making transactions should be analyzed alongside discount levels, category, and geography.

> **Note:** The exact numerical findings should be added after reviewing the final outputs from the notebook.

---

## 💡 Business Recommendations

### 1. Optimize Discount Strategy

Avoid applying high discounts broadly.

Use targeted discounts for specific products, customer segments, or business situations while monitoring their effect on profit margins.

### 2. Investigate Loss-Making Products

Review pricing, discounts, and other business costs associated with consistently loss-making sub-categories.

### 3. Focus on Profitable Products

Identify high-profit sub-categories and consider strategies that increase their sales while maintaining healthy margins.

### 4. Monitor Regional Performance

Investigate states and regions with consistently low or negative profitability and identify the underlying business factors.

### 5. Evaluate Shipping Performance

Compare shipping modes based on both sales and profitability rather than using order volume alone.

### 6. Use Data-Driven Pricing Decisions

Discount decisions should consider their impact on profitability instead of focusing only on increasing sales volume.

---

## 📁 Project Structure

```text
Superstore-Sales-Profit-Analysis/
│
├── data/
│   └── Sample - Superstore.csv
│
├── notebooks/
│   └── Superstore_Analysis.ipynb
│
├── visualizations/
│   ├── sales_by_category.png
│   ├── profit_by_subcategory.png
│   ├── discount_vs_profit.png
│   ├── profit_by_region.png
│   └── top_loss_states.png
│
├── README.md
└── requirements.txt
```

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_LINK
```

### 2. Install required libraries

```bash
pip install -r requirements.txt
```

### 3. Open Jupyter Notebook

```bash
jupyter notebook
```

### 4. Open

```text
notebooks/Superstore_Analysis.ipynb
```

### 5. Run the notebook

Run the cells sequentially to reproduce the analysis and visualizations.

---

## 📌 Skills Demonstrated

This project demonstrates practical skills in:

* Data Cleaning
* Data Transformation
* Feature Engineering
* Exploratory Data Analysis
* Pandas
* Matplotlib
* Seaborn
* Statistical Analysis
* Business Insights
* Data Visualization
* Business Recommendations

---

## 👩‍💻 Author

**Shreya**

Computer Engineering Student | Aspiring Data Analyst

### Technical Skills

**Python | SQL | Power BI | Excel | Data Visualization**

---

⭐ If you found this project useful, feel free to explore the repository and the analysis notebook.
