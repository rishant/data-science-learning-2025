## Prequisites

    1. Python installation

## install Pandas

    pip install pandas


🎯 Must-Have Checklist (for every Pandas learner)

 Understand Series vs DataFrame

 Read/Write CSV & Excel

 Indexing & Filtering (loc, iloc)

 Handle Missing Values (fillna, dropna)

 Handle Duplicates

 Sorting & Ranking

 GroupBy & Aggregation

 Merge & Join datasets

 Pivot tables & Crosstabs

 Time Series basics (to_datetime, resample)

 Data Visualization (plot())

 Optimize memory for large datasets


# 📘 Pandas Learning Examples

## 1. **Introduction & Basics**
```python
import pandas as pd

# Series
s = pd.Series([10, 20, 30], index=['a', 'b', 'c'])
print(s)

# DataFrame from dict
df = pd.DataFrame({
    "Name": ["Alice", "Bob", "Charlie"],
    "Age": [25, 30, 35]
})
print(df)
```

---

## 2. **Data Input/Output**
```python
df = pd.read_csv("data.csv")
df.to_csv("output.csv", index=False)

df_excel = pd.read_excel("data.xlsx")
df_json = pd.read_json("data.json")
```

---

## 3. **Exploring Data**
```python
print(df.head())       
print(df.tail(3))      
print(df.info())       
print(df.describe())   
print(df.shape)        
```

---

## 4. **Indexing & Selection**
```python
print(df["Name"])                
print(df[["Name", "Age"]])       
print(df.loc[0, "Name"])         
print(df.iloc[0, 1])             
print(df[df["Age"] > 28])        
```

---

## 5. **Adding & Modifying Columns**
```python
df["Salary"] = [50000, 60000, 70000]   
df["AgePlus10"] = df["Age"] + 10       
df.rename(columns={"Age": "Years"}, inplace=True)
```

---

## 6. **Dropping Rows/Columns**
```python
df.drop("Salary", axis=1, inplace=True)  
df.drop(1, axis=0, inplace=True)         
```

---

## 7. **Sorting**
```python
print(df.sort_values("Age"))
print(df.sort_values(["Age", "Name"], ascending=[True, False]))
```

---

## 8. **Handling Missing Data**
```python
df["Age"].fillna(df["Age"].mean(), inplace=True)  
df.dropna(inplace=True)                           
```

---

## 9. **Aggregation & GroupBy**
```python
print(df["Age"].mean())
print(df.groupby("Name")["Age"].mean())
print(df.groupby("Name").agg({"Age": "max"}))
```

---

## 10. **Merging & Joining**
```python
df1 = pd.DataFrame({"ID": [1,2], "Name": ["A", "B"]})
df2 = pd.DataFrame({"ID": [1,2], "Salary": [100, 200]})

merged = pd.merge(df1, df2, on="ID")
print(merged)
```

---

## 11. **Concatenation & Append**
```python
df1 = pd.DataFrame({"A": [1,2]})
df2 = pd.DataFrame({"A": [3,4]})
print(pd.concat([df1, df2]))
```

---

## 12. **Pivot Tables & Crosstab**
```python
df = pd.DataFrame({
    "Name": ["A", "A", "B", "B"],
    "Subject": ["Math", "Eng", "Math", "Eng"],
    "Marks": [90, 80, 70, 60]
})

pivot = df.pivot_table(values="Marks", index="Name", columns="Subject")
print(pivot)
```

---

## 13. **Apply & Lambda**
```python
df["AgeSquared"] = df["Age"].apply(lambda x: x**2)
```

---

## 14. **String Operations**
```python
df["NameUpper"] = df["Name"].str.upper()
print(df[df["Name"].str.contains("A")])
```

---

## 15. **Datetime Handling**
```python
df["JoiningDate"] = pd.to_datetime(["2021-01-01", "2021-06-15", "2022-03-10"])
print(df["JoiningDate"].dt.year)
```

---

## 16. **Window Functions**
```python
df["RollingAvg"] = df["Age"].rolling(window=2).mean()
```

---

## 17. **Categorical Data**
```python
df["Dept"] = pd.Categorical(["HR", "IT", "HR"])
print(df["Dept"].cat.codes)  
```

---

## 18. **MultiIndex (Hierarchical Indexing)**
```python
arrays = [
    ["A", "A", "B", "B"],
    [1, 2, 1, 2]
]
mi = pd.MultiIndex.from_arrays(arrays, names=("Letter", "Number"))
df = pd.DataFrame({"Value": [10,20,30,40]}, index=mi)
print(df)
```

---

## 19. **Advanced Joins (Merge with conditions)**
```python
pd.merge(df1, df2, on="ID", how="outer")   
```

---

## 20. **Exporting Data**
```python
df.to_csv("final.csv", index=False)
df.to_excel("final.xlsx", index=False)
df.to_json("final.json", orient="records")
```
