## Prequisites

    1. Python installation


### Python Modules installation:

    pip install numpy
    pip install pandas
    pip install matplotlib


### Step for jupyter notebook installation:

    pip install notebook


### Step for Run jupyter notebook:

    jupyter notebook


### NumPy Topics

    1. Introduction to NumPy
    2. NumPy Array Creation
    3. Array Indexing and Slicing
    4. Array Shape and Reshape
    5. Array Data Types
    6. Array Operations (Arithmetic, Comparison)
    7. Universal Functions (ufuncs)
    8. Aggregation Functions (sum, mean, std, etc.)
    9. Broadcasting
    10. Random Module in NumPy
    11. Sorting and Searching
    12. Copy vs View
    13. Structured Arrays
    14. Saving and Loading Arrays
    15. Linear Algebra in NumPy
    16. Masking and Filtering
    17. Handling Missing Data
    18. Performance Tips
    19. Integration with Other Libraries

### 1. Introduction to NumPy

```python
import numpy as np
print(np.__version__)
```

### 2. NumPy Array Creation

```python
a = np.array([1, 2, 3])
b = np.zeros((2, 3))
c = np.ones(5)
d = np.arange(0, 10, 2)
e = np.linspace(0, 1, 5)
```

### 3. Array Indexing and Slicing

```python
arr = np.array([10, 20, 30, 40, 50])
print(arr[1])
print(arr[1:4])
arr2d = np.array([[1, 2], [3, 4]])
print(arr2d[0, 1])
```

### 4. Array Shape and Reshape

```python
arr = np.arange(6)
print(arr.shape)
arr2d = arr.reshape((2, 3))
print(arr2d)
```

### 5. Array Data Types

```python
arr = np.array([1, 2, 3], dtype=np.float32)
print(arr.dtype)
```

### 6. Array Operations (Arithmetic, Comparison)

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
print(a + b)
print(a * b)
print(a > 2)
```

### 7. Universal Functions (ufuncs)

```python
arr = np.array([1, 4, 9])
print(np.sqrt(arr))
print(np.exp(arr))
```

### 8. Aggregation Functions (sum, mean, std, etc.)

```python
arr = np.array([1, 2, 3, 4])
print(arr.sum())
print(arr.mean())
print(arr.std())
```

### 9. Broadcasting

```python
a = np.array([1, 2, 3])
b = np.array([[10], [20], [30]])
print(a + b)
```

### 10. Random Module in NumPy

```python
rand_arr = np.random.rand(2, 3)
rand_int = np.random.randint(0, 10, size=(3, 3))
```

### 11. Sorting and Searching

```python
arr = np.array([3, 1, 2])
print(np.sort(arr))
print(np.where(arr == 2))
```

### 12. Copy vs View

```python
arr = np.array([1, 2, 3])
view = arr.view()
copy = arr.copy()
arr[0] = 99
print(view)
print(copy)
```

### 13. Structured Arrays

```python
dt = np.dtype([('name', 'S10'), ('age', 'i4')])
arr = np.array([('Alice', 25), ('Bob', 30)], dtype=dt)
print(arr['name'])
```

### 14. Saving and Loading Arrays

```python
arr = np.array([1, 2, 3])
np.save('my_array.npy', arr)
loaded = np.load('my_array.npy')
print(loaded)
```

### 15. Linear Algebra in NumPy

```python
a = np.array([[1, 2], [3, 4]])
b = np.array([[5, 6], [7, 8]])
print(np.dot(a, b))
print(np.linalg.inv(a))
```

### 16. Masking and Filtering

```python
arr = np.array([1, 2, 3, 4, 5])
mask = arr > 2
print(arr[mask])
```

### 17. Handling Missing Data

```python
arr = np.array([1, np.nan, 3])
print(np.isnan(arr))
print(np.nanmean(arr))
```

### 18. Performance Tips

```python
arr = np.arange(1e6)
%timeit arr + 1  # Jupyter magic for timing
```

### 19. Integration with Other Libraries

```python
import pandas as pd
df = pd.DataFrame(np.random.rand(3, 3), columns=['A', 'B', 'C'])
print(df)
```