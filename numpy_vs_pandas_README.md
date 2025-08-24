# 📊 NumPy vs Pandas

Understanding the difference between **NumPy** and **Pandas** helps you decide which tool to use for data-related tasks in Python.

---

## 🔹 NumPy

- **What it is:**  
  Fundamental **scientific computing library** for Python. Provides efficient operations on large, multi-dimensional arrays and matrices.

- **Key Features:**
  - `ndarray` (N-dimensional array) – much faster than Python lists.
  - Optimized for **numerical computations** (linear algebra, Fourier transforms, random numbers).
  - Backbone of many Python data libraries (Pandas, Scikit-learn, TensorFlow, etc.).
  - **Vectorized operations** → faster than Python loops.

✅ **Use NumPy when:**
- You need **fast mathematical operations** on large datasets.
- You’re working with **raw numerical data** (e.g., sensor data, image arrays, matrices).
- You need **linear algebra, statistics, broadcasting** computations.
- You don’t need row/column **labels** – just numbers.

---

## 🔹 Pandas

- **What it is:**  
  Built **on top of NumPy**, designed for **structured/tabular data** with labeled rows and columns.

- **Key Features:**
  - **Series** (1D labeled array) and **DataFrame** (2D labeled table like Excel/SQL).
  - Great for **data cleaning, transformation, and analysis**.
  - Supports multiple **data types** (numbers, strings, dates, categorical data).
  - Rich **I/O support** (CSV, Excel, SQL, JSON, Parquet, etc.).
  - Built-in functions for **grouping, merging, joining, filtering, reshaping**.

✅ **Use Pandas when:**
- You’re working with **structured/tabular data**.
- You need **labels** (column names, row indexes).
- You’re performing **data cleaning, wrangling, or EDA (exploratory data analysis)**.
- You want SQL/Excel-like operations in Python.

---

## 🔹 Quick Comparison

| Feature                | **NumPy**                          | **Pandas**                          |
|-------------------------|------------------------------------|--------------------------------------|
| Data Structure          | `ndarray` (N-dimensional array)   | `Series` (1D), `DataFrame` (2D)     |
| Best For                | Numerical & scientific computing  | Tabular, structured data             |
| Speed                   | Very fast for numeric operations  | Slightly slower (built on NumPy)     |
| Labels (row/col names)  | ❌ Not supported                  | ✅ Supported                        |
| Data Types              | Homogeneous (all same type)       | Heterogeneous (mixed types allowed)  |
| Typical Use Cases       | Math, ML preprocessing, image ops | Data analysis, cleaning, wrangling   |

---

## 🔹 Rule of Thumb

- **Use NumPy** for **pure math, matrices, arrays** (ML, stats, scientific computing).  
- **Use Pandas** for **structured datasets** (CSV, SQL, Excel, JSON) and **data analysis/cleaning**.  

👉 In practice, you often **use both together**:
- Load & clean data with **Pandas**.
- Convert to **NumPy arrays** for numerical modeling/ML.

---

## 🔹 Example Workflow

```python
import pandas as pd
import numpy as np

# Load tabular data with Pandas
df = pd.read_csv("sales.csv")
print(df.head())

# Clean & transform
df["total_price"] = df["quantity"] * df["unit_price"]

# Convert to NumPy for numerical computation
arr = df[["quantity", "unit_price", "total_price"]].to_numpy()
print(type(arr))  # <class 'numpy.ndarray'>

# Use NumPy for fast numerical operations
mean_price = np.mean(arr[:, 2])
print("Average total price:", mean_price)
```

## 📌 Summary:

    NumPy → Fast math with arrays.
    Pandas → Data analysis with tables.