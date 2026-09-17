## ETL Project + Flask Dashboard

### 📌 Overview

Build an ETL pipeline using Python with three data sources:

* `customers.csv`
* `orders.parquet`
* `products.csv` — retrieved from an API [Link](https://raw.githubusercontent.com/MohammedHameds/test1455/refs/heads/main/products.csv)

Clean, transform, merge the data, load the final Sales table into **SQL Server**, and display it using a **Flask dashboard**.

### 🔄 Transformations

**Customers**

* Remove duplicates
* Standardize city
* Validate age
* Handle missing email
* Create `full_name`

**Orders**

* Remove duplicate `order_id`
* Validate quantity
* Convert `order_date` to datetime
* Validate `customer_id`

**Products**

* Remove duplicates
* Standardize product/category
* Validate `unit_price`
* Convert price to numeric

### 💰 Sales

Merge the three datasets and calculate:

```python
sales["total_amount"] = sales["quantity"] * sales["unit_price"]
```

Final columns:

```text
order_id
customer
product
quantity
unit_price
total_amount
```

### 🗄️ SQL Server

Load the final `Sales` table into SQL Server.

### 🌐 Flask Dashboard

Create a Flask application that:

1. Connects to SQL Server.
2. Retrieves the `Sales` table.
3. Displays the data in an HTML dashboard.
