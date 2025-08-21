# Python Topics with Real-World Examples

## 1. Variables and Data Types
```python
# 1. Store product price
price = 299.99

# 2. Store quantity
quantity = 5

# 3. Store product name
product_name = "Smartphone"

# 4. Boolean for user login status
is_logged_in = False

# 5. List for multiple phone numbers
phone_numbers = ["1234567890", "9876543210"]

# 6. Dictionary for user profile
user_profile = {"name": "Bob", "age": 28, "email": "bob@example.com"}

# 7. Tuple for coordinates
location = (40.7128, -74.0060)

# 8. Set for unique tags
tags = {"python", "coding", "tutorial"}

# 9. None for missing data
middle_name = None

# 10. Print all variables
print(price, quantity, product_name, is_logged_in, phone_numbers, user_profile, location, tags, middle_name)

# Store employee age and name
employee_name = "Alice"
employee_age = 30
salary = 55000.50
is_manager = True
print(employee_name, employee_age, salary, is_manager)
```

## 2. Input and Output
```python
# Get user input for a banking application
name = input("Enter your name: ")
print("Welcome,", name)

# Input product quantity for billing
quantity = int(input("Enter quantity: "))
print("Quantity entered:", quantity)

```

## 3. Conditional Statements
```python
# Check loan eligibility
income = 40000
if income > 30000:
    print("Eligible for loan")
else:
    print("Not eligible for loan")

# Professional Conditional Logic Examples

# 1. Multiple conditions with elif (e.g., grading system)
score = 85
if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
else:
    print("Grade: D")

# 2. Compound conditions using and/or (e.g., access control)
is_admin = True
is_active = False
if is_admin and is_active:
    print("Access granted")
else:
    print("Access denied")

# 3. Checking membership (e.g., user roles)
role = "editor"
if role in ["admin", "editor"]:
    print("Can edit content")

# 4. Nested conditions (e.g., payment processing)
payment_method = "credit_card"
amount = 500
if payment_method == "credit_card":
    if amount > 1000:
        print("Requires manager approval")
    else:
        print("Payment processed")
else:
    print("Unsupported payment method")

# 5. Ternary conditional (e.g., status message)
status = "active"
message = "User is online" if status == "active" else "User is offline"
print(message)

# 6. Checking for empty values (e.g., form validation)
email = ""
if not email:
    print("Email is required")

# 7. Using all/any for batch checks (e.g., data validation)
fields = ["name", "email", "age"]
data = {"name": "Alice", "email": "alice@example.com", "age": 30}
if all(field in data and data[field] for field in fields):
    print("All fields present")
else:
    print("Missing fields")

# 8. Switch-like logic using dictionaries (e.g., command routing)
def handle_command(cmd):
    actions = {
        "start": lambda: print("Starting..."),
        "stop": lambda: print("Stopping..."),
        "pause": lambda: print("Pausing...")
    }
    action = actions.get(cmd, lambda: print("Unknown command"))
    action()

handle_command("start")
handle_command("exit")
```

## 4. Loops
```python
# Print all items in a shopping cart
cart = ["apple", "banana", "milk"]
for item in cart:
    print(item)

    # Print item prices in a shopping cart
    prices = [30, 20, 50]
    for price in prices:
        print("Price:", price)

    # Use while loop to process items until cart is empty
    cart = ["apple", "banana", "milk"]
    while cart:
        item = cart.pop()
        print("Removed:", item)

    # Loop with enumerate to get index and value
    for idx, item in enumerate(["apple", "banana", "milk"]):
        print(f"Item {idx}: {item}")

    # Loop with range for fixed number of iterations
    for i in range(3):
        print("Iteration:", i)

    # Nested loops for a grid (e.g., seating chart)
    rows = 2
    cols = 3
    for r in range(rows):
        for c in range(cols):
            print(f"Seat ({r}, {c})")

    # Using break and continue in loops
    for item in ["apple", "banana", "milk"]:
        if item == "banana":
            continue  # Skip banana
        print("Selected:", item)
        if item == "milk":
            break  # Stop after milk

    # List comprehension inside a loop for advanced filtering
    numbers = [1, 2, 3, 4, 5]
    evens = [n for n in numbers if n % 2 == 0]
    print("Even numbers:", evens)

    # Loop with else clause
    for item in ["apple", "banana"]:
        if item == "orange":
            print("Found orange!")
            break
    else:
        print("Orange not found in cart.")
```

## 5. Functions
```python
# Calculate area of a rectangle for a construction app
def area(length, width):
    return length * width

print(area(5, 3))

# Sum all numbers in a list
def sum_list(numbers):
    return sum(numbers)
print("Sum:", sum_list([1, 2, 3, 4, 5]))

# Find all even numbers in a list
def find_evens(numbers):
    return [x for x in numbers if x % 2 == 0]
print("Even numbers:", find_evens([1, 2, 3, 4, 5, 6]))

# Count vowels in a string
def count_vowels(s):
    return sum(1 for char in s.lower() if char in "aeiou")
print("Vowels in 'Python':", count_vowels("Python"))

```

## 6. Lists
```python
# Store student marks
marks = [85, 90, 78]
marks.append(88)
print(marks)

# List operations examples

# Access elements
print("First mark:", marks[0])

# Slicing
print("First two marks:", marks[:2])

# Length of list
print("Total marks:", len(marks))

# Insert at specific position
marks.insert(1, 92)
print("After insert:", marks)

# Remove by value
marks.remove(78)
print("After remove:", marks)

# Pop last element
last = marks.pop()
print("Popped:", last, "Remaining:", marks)

# Sort marks
marks.sort()
print("Sorted marks:", marks)

# Reverse marks
marks.reverse()
print("Reversed marks:", marks)

# Check existence
print(90 in marks)

# Iterate over list
for m in marks:
    print("Mark:", m)

# Find index of a value
print("Index of 85:", marks.index(85))

# Count occurrences
print("Count of 90:", marks.count(90))
```

## 7. Tuples
```python
# Store coordinates for a mapping app
location = (28.7041, 77.1025)

# Tuple operations examples

# Access elements
print("Longitude:", location[1])

# Slicing
coords = (1, 2, 3, 4, 5)
print("First three:", coords[:3])

# Length of tuple
print("Total coordinates:", len(coords))

# Concatenation
extra = (6, 7)
combined = coords + extra
print("Combined:", combined)

# Repetition
repeated = coords * 2
print("Repeated:", repeated)

# Check existence
print(2 in coords)

# Iterate over tuple
for value in coords:
    print("Value:", value)

# Find index of an element
print("Index of 3:", coords.index(3))

# Count occurrences
print("Count of 2:", coords.count(2))
```

## 8. Dictionaries
```python

# Store product details in an e-commerce app
product = {"id": 101, "name": "Laptop", "price": 45000}
print(product["name"], product["price"])

# Dictionary operations examples

# Add a new key-value pair
product["stock"] = 25
print(product)

# Update a value
product["price"] = 43000
print(product)

# Remove a key-value pair
del product["stock"]
print(product)

# Get all keys
print(product.keys())

# Get all values
print(product.values())

# Get all items
print(product.items())

# Check if a key exists
print("name" in product)

# Safely get a value with default
print(product.get("discount", "No discount"))

# Iterate over dictionary
for key, value in product.items():
    print(key, ":", value)

```

## 9. Sets
```python
# Remove duplicate emails in a mailing list
emails = {"alice@example.com", "bob@example.com", "alice@example.com"}
print(emails)

# Set operations examples

# Add a new email
emails.add("carol@example.com")

# Remove an email
emails.discard("bob@example.com")

# Check if an email exists
print("alice@example.com" in emails)

# Union of two sets
other_emails = {"dave@example.com", "carol@example.com"}
all_emails = emails.union(other_emails)
print(all_emails)

# Intersection of two sets
common_emails = emails.intersection(other_emails)
print(common_emails)

# Difference between sets
unique_emails = emails.difference(other_emails)
print(unique_emails)

```

## 10. Exception Handling

```python

# 1. Basic try-except
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero!")

# 2. Catching multiple exceptions
try:
    value = int("abc")
except (ValueError, TypeError):
    print("Invalid conversion!")

# 3. Handle invalid user input in a billing system
try:
    amount = float(input("Enter amount: "))
except ValueError:
    print("Invalid amount entered!")

# 3. Using else with try-except
try:
    num = int(input("Enter a number: "))
except ValueError:
    print("Not a number!")
else:
    print("You entered:", num)

# 4. Using finally to always execute code
try:
    f = open("data.txt")
    data = f.read()
except FileNotFoundError:
    print("File not found!")
finally:
    print("Closing file (if open).")

# 5. Raising exceptions manually
def withdraw(balance, amount):
    if amount > balance:
        raise Exception("Insufficient funds!")
    return balance - amount

try:
    withdraw(100, 200)
except Exception as e:
    print(e)

# 6. Custom exception classes
class MyError(Exception):
    pass

try:
    raise MyError("Something went wrong!")
except MyError as err:
    print(err)
```

## 11. File Handling
```python
# Save user feedback to a file
with open("feedback.txt", "w") as f:
    f.write("Great service!")

# File Operations Examples

# 1. Write to a file (overwrite)
with open("example.txt", "w") as f:
    f.write("Hello World!")

# 2. Append to a file
with open("example.txt", "a") as f:
    f.write("\nAppended line.")

# 3. Read entire file
with open("example.txt", "r") as f:
    content = f.read()
    print(content)

# 4. Read file line by line
with open("example.txt", "r") as f:
    for line in f:
        print(line.strip())

# 5. Read all lines into a list
with open("example.txt", "r") as f:
    lines = f.readlines()
    print(lines)

# 6. Write multiple lines
lines = ["First line\n", "Second line\n"]
with open("example.txt", "w") as f:
    f.writelines(lines)

# 7. Open file in binary mode
with open("image.png", "rb") as f:
    data = f.read()

# 8. Write binary data
with open("output.bin", "wb") as f:
    f.write(b'\x00\xFF')

# 9. Check if file exists before reading
import os
if os.path.exists("example.txt"):
    with open("example.txt") as f:
        print(f.read())
else:
    print("File does not exist.")

# 10. Using try-except for safe file operations
try:
    with open("missing.txt") as f:
        print(f.read())
except FileNotFoundError:
    print("File not found.")

# 11. Rename and delete files
    os.rename("example.txt", "renamed.txt")
    os.remove("renamed.txt")

## 12. Serialization and Deserialization

    # JSON
    ```python
    import json

    user_data = {"name": "Alice", "age": 30, "email": "alice@example.com"}
    with open("user.json", "w") as f:
        json.dump(user_data, f)

    # Deserialize user data from the file
    with open("user.json", "r") as f:
        loaded_data = json.load(f)
        print(loaded_data)
    ```

    # Pickle is a Python module for serializing and deserializing Python objects (saving and loading objects to/from files).
    ```python
    import pickle

    # Write (serialize) Python object to a pickle file
    data = {"name": "Bob", "age": 25}
    with open("data.pkl", "wb") as f:
        pickle.dump(data, f)

    # Read (deserialize) Python object from a pickle file
    with open("data.pkl", "rb") as f:
        loaded = pickle.load(f)
        print(loaded)
    ```

    ### YAML (PyYAML)
    ```python
    import yaml

    # Serialize Python object to YAML
    data = {"name": "Alice", "age": 30}
    with open("data.yaml", "w") as f:
        yaml.dump(data, f)

    # Deserialize YAML to Python object
    with open("data.yaml", "r") as f:
        loaded = yaml.safe_load(f)
        print(loaded)
    ```

    ### MessagePack
    ```python
    import msgpack

    # Serialize Python object to MessagePack
    data = {"name": "Bob", "age": 25}
    with open("data.msgpack", "wb") as f:
        f.write(msgpack.packb(data))

    # Deserialize MessagePack to Python object
    with open("data.msgpack", "rb") as f:
        loaded = msgpack.unpackb(f.read())
        print(loaded)
    ```

    ### TOML
    ```python
    import toml

    # Serialize Python object to TOML
    data = {"name": "Carol", "age": 22}
    with open("data.toml", "w") as f:
        toml.dump(data, f)

    # Deserialize TOML to Python object
    with open("data.toml", "r") as f:
        loaded = toml.load(f)
        print(loaded)
    ```

    ### XML (xml.etree.ElementTree)
    ```python
    import xml.etree.ElementTree as ET

    # Serialize Python object to XML
    person = ET.Element("person")
    name = ET.SubElement(person, "name")
    name.text = "Dave"
    age = ET.SubElement(person, "age")
    age.text = "40"
    tree = ET.ElementTree(person)
    tree.write("person.xml")

    # Deserialize XML to Python object
    tree = ET.parse("person.xml")
    root = tree.getroot()
    print(root.find("name").text, root.find("age").text)
    ```

    ### CSV (csv module)
    ```python
    import csv

    # Serialize Python object to CSV
    data = [["name", "age"], ["Eve", 28]]
    with open("data.csv", "w", newline="") as f:
        writer = csv.writer(f)
        writer.writerows(data)

    # Deserialize CSV to Python object
    with open("data.csv", "r") as f:
        reader = csv.reader(f)
        for row in reader:
            print(row)
    ```

    ### Parquet (pyarrow or fastparquet)
    ```python
    import pandas as pd

    # Serialize DataFrame to Parquet
    df = pd.DataFrame({"name": ["Alice", "Bob"], "age": [30, 25]})
    df.to_parquet("data.parquet")

    # Deserialize Parquet to DataFrame
    df_loaded = pd.read_parquet("data.parquet")
    print(df_loaded)
    ```

    ### Excel (openpyxl or pandas)
    ```python
    import pandas as pd

    # Serialize DataFrame to Excel
    df = pd.DataFrame({"name": ["Carol", "Dave"], "age": [22, 40]})
    df.to_excel("data.xlsx", index=False)

    # Deserialize Excel to DataFrame
    df_loaded = pd.read_excel("data.xlsx")
    print(df_loaded)
    ```
```


## 12. Classes and Objects
```python
    # Model a car for a rental service
    class Car:
        def __init__(self, brand, price):
            self.brand = brand
            self.price = price

    car1 = Car("Toyota", 800000)
    print(car1.brand, car1.price)
    ```
    # Object-Oriented Programming Concepts

    ## 1. Abstraction
    ```python
    # Abstract class for a payment method
    from abc import ABC, abstractmethod

    class PaymentMethod(ABC):
        @abstractmethod
        def pay(self, amount):
            pass

    class CreditCard(PaymentMethod):
        def pay(self, amount):
            print(f"Paid {amount} using credit card.")

    payment = CreditCard()
    payment.pay(1000)
    ```

    ## 2. Polymorphism
    ```python
    # Different payment methods with the same interface
    class PayPal(PaymentMethod):
        def pay(self, amount):
            print(f"Paid {amount} using PayPal.")

    methods = [CreditCard(), PayPal()]
    for method in methods:
        method.pay(500)
    ```

    ## 3. Inheritance
    ```python
    # Base class Vehicle and derived class Car
    class Vehicle:
        def __init__(self, brand):
            self.brand = brand

        def drive(self):
            print(f"{self.brand} is driving.")

    class Car(Vehicle):
        def drive(self):
            print(f"{self.brand} car is driving smoothly.")

    my_car = Car("Honda")
    my_car.drive()
    ```

    ## 4. Encapsulation
    ```python
    # Encapsulate account balance with getter and setter
    class BankAccount:
        def __init__(self):
            self.__balance = 0  # Private variable

        def deposit(self, amount):
            self.__balance += amount

        def get_balance(self):
            return self.__balance

    account = BankAccount()
    account.deposit(500)
    print("Balance:", account.get_balance())
    ```

    ## 12.1. Scope of Member Variables and Methods

    ## Python does not have explicit access modifiers like `public`, `private`, or `protected` as in some other languages, but you can control access using naming conventions:

    ## - **Public**: Accessible from anywhere. No underscore prefix.
    ## - **Protected (default)**: Intended for internal use. Single underscore prefix (`_`).
    ## - **Private**: Name mangling to restrict access. Double underscore prefix (`__`).

    ```python
    class Example:
        public_var = "I am public"           # Public variable
        _protected_var = "I am protected"    # Protected (default) variable
        __private_var = "I am private"       # Private variable

        def public_method(self):
            print("Public method")

        def _protected_method(self):
            print("Protected method")

        def __private_method(self):
            print("Private method")

    obj = Example()
    print(obj.public_var)           # Accessible
    print(obj._protected_var)       # Accessible, but intended as protected
    # print(obj.__private_var)      # Not directly accessible

    obj.public_method()             # Accessible
    obj._protected_method()         # Accessible, but intended as protected
    # obj.__private_method()        # Not directly accessible

    # Accessing private members using name mangling
    print(obj._Example__private_var)
    obj._Example__private_method()
    ```
```

## 13. Modules and Packages
```python
# Use math module for scientific calculations
import math
print(math.sqrt(49))
```

## 14. List Comprehension
```python
# 1. Basic list comprehension: squares of numbers
squares = [x**2 for x in range(1, 6)]
print(squares)

# 2. Filtering: even numbers
evens = [x for x in range(10) if x % 2 == 0]
print(evens)

# 3. Nested loops: pairs (i, j)
pairs = [(i, j) for i in range(3) for j in range(2)]
print(pairs)

# 4. Conditional expression: label even/odd
labels = ["even" if x % 2 == 0 else "odd" for x in range(5)]
print(labels)

# 5. List comprehension with function call
def double(x): return x * 2
doubled = [double(x) for x in range(5)]
print(doubled)

# 6. Flatten a 2D list
matrix = [[1, 2], [3, 4]]
flat = [item for row in matrix for item in row]
print(flat)

# 7. Remove vowels from a string
s = "hello world"
no_vowels = [c for c in s if c not in "aeiou"]
print("".join(no_vowels))

# 8. List of tuples with condition
filtered_pairs = [(x, y) for x in range(3) for y in range(3) if x != y]
print(filtered_pairs)

# 9. Dictionary keys to uppercase
d = {"a": 1, "b": 2}
upper_keys = [k.upper() for k in d.keys()]
print(upper_keys)

# 10. List comprehension with enumerate
indexed = [(i, v) for i, v in enumerate(["a", "b", "c"])]
print(indexed)

# 11. List comprehension with zip
names = ["Alice", "Bob"]
ages = [25, 30]
combined = [f"{n} is {a}" for n, a in zip(names, ages)]
print(combined)

# 12. List comprehension with set
unique = [x for x in {1, 2, 3, 2, 1}]
print(unique)

# 13. List comprehension with string methods
words = ["hello", "world"]
upper_words = [w.upper() for w in words]
print(upper_words)

# 14. List comprehension with range and step
multiples_of_3 = [x for x in range(0, 20, 3)]
print(multiples_of_3)

# 15. List comprehension for flattening and filtering
matrix = [[1, 2, 3], [4, 5, 6]]
flat_evens = [x for row in matrix for x in row if x % 2 == 0]
print(flat_evens)

# 16. List comprehension with try-except (using helper function)
def safe_int(s):
    try:
        return int(s)
    except ValueError:
        return None
values = ["1", "a", "3"]
ints = [safe_int(v) for v in values]
print(ints)
```

## 15. Lambda Functions
```python
    # Sort employees by salary
    employees = [("Alice", 50000), ("Bob", 60000)]
    employees.sort(key=lambda x: x[1])
    print(employees)

    # Professional Lambda Function Examples

    ```python
    # 1. Lambda for sorting by multiple keys (e.g., sort employees by department then salary)
    employees = [
        {"name": "Alice", "dept": "HR", "salary": 50000},
        {"name": "Bob", "dept": "IT", "salary": 60000},
        {"name": "Carol", "dept": "HR", "salary": 55000}
    ]
    employees.sort(key=lambda x: (x["dept"], -x["salary"]))
    print(employees)

    # 2. Lambda for custom filtering (e.g., filter active users)
    users = [
        {"name": "Alice", "active": True},
        {"name": "Bob", "active": False}
    ]
    active_users = list(filter(lambda u: u["active"], users))
    print(active_users)

    # 3. Lambda for mapping transformations (e.g., anonymize emails)
    emails = ["alice@example.com", "bob@example.com"]
    masked = list(map(lambda e: e.split("@")[0] + "@***", emails))
    print(masked)

    # 4. Lambda in DataFrame operations (e.g., add computed column)
    import pandas as pd
    df = pd.DataFrame({"price": [100, 200], "tax": [0.1, 0.2]})
    df["total"] = df.apply(lambda row: row["price"] * (1 + row["tax"]), axis=1)
    print(df)

    # 5. Lambda for reducing (e.g., total invoice amount)
    from functools import reduce
    invoices = [120, 80, 150]
    total = reduce(lambda a, b: a + b, invoices)
    print(total)

    # 6. Lambda for event handling (e.g., GUI callbacks)
    def on_click(callback):
        callback("Button clicked!")

    on_click(lambda msg: print(msg))

    # 7. Lambda for key extraction (e.g., max by score)
    students = [{"name": "Alice", "score": 85}, {"name": "Bob", "score": 92}]
    top_student = max(students, key=lambda s: s["score"])
    print(top_student)

    # 8. Lambda for conditional logic (e.g., label transactions)
    transactions = [120, -50, 200, -30]
    labels = list(map(lambda x: "credit" if x > 0 else "debit", transactions))
    print(labels)

    # 9. Lambda for inline arithmetic (e.g., currency conversion)
    usd = [10, 20, 30]
    eur = list(map(lambda x: x * 0.92, usd))
    print(eur)

    # 10. Lambda for sorting complex objects (e.g., sort files by extension)
    files = ["report.pdf", "data.csv", "image.png"]
    files.sort(key=lambda f: f.split(".")[-1])
    print(files)

    # 11. Lambda for dictionary value transformation (e.g., increase prices)
    products = {"A": 100, "B": 200}
    updated = {k: (lambda v: v * 1.1)(v) for k, v in products.items()}
    print(updated)

    # 12. Lambda for chaining functions (e.g., preprocess text)
    texts = ["  Hello ", "World!  "]
    cleaned = list(map(lambda s: s.strip().lower(), texts))
    print(cleaned)

    # 13. Lambda for grouping (e.g., group by first letter)
    names = ["Alice", "Bob", "Anna"]
    from collections import defaultdict
    groups = defaultdict(list)
    for name in names:
        groups[(lambda n: n[0])(name)].append(name)
    print(dict(groups))

    # 14. Lambda for exception-safe conversion (e.g., parse numbers)
    values = ["10", "x", "20"]
    parsed = list(map(lambda v: int(v) if v.isdigit() else None, values))
    print(parsed)

    # 15. Lambda for functional composition (e.g., apply multiple transformations)
    def compose(*funcs):
        return lambda x: reduce(lambda v, f: f(v), funcs, x)

    double = lambda x: x * 2
    increment = lambda x: x + 1
    pipeline = compose(double, increment)
    print(pipeline(3))  # Output: 7
    ```
```

## 16. Map, Filter, Reduce
```python
# Apply discount to all prices in a store
prices = [100, 200, 300]
discounted = list(map(lambda x: x * 0.9, prices))
print(discounted)
```

## 17. Working with JSON
```python
# Parse API response in a web app
import json
data = '{"name": "Alice", "age": 30}'
parsed = json.loads(data)
print(parsed["name"])
```

## 18. Date and Time
```python
# Print current date for a report
from datetime import datetime
print(datetime.now())
```

## 19. Regular Expressions
```python
# Validate email format in a signup form
import re
email = "test@example.com"
if re.match(r"[^@]+@[^@]+\.[^@]+", email):
    print("Valid email")
```

## 20. Virtual Environment
```python
# Create isolated environment for a project (run in terminal)
# python -m venv myenv
```

## 21. Web Scraping
```python
# Scrape headlines from a news website
import requests
from bs4 import BeautifulSoup
response = requests.get("https://news.ycombinator.com/")
soup = BeautifulSoup(response.text, "html.parser")
for headline in soup.find_all("a", class_="storylink"):
    print(headline.text)
```

## 22. Working with CSV
```python
# Read sales data from a CSV file
import csv
with open("sales.csv") as f:
    reader = csv.reader(f)
    for row in reader:
        print(row)
```

## 23. Numpy Basics
```python
# Calculate average temperature from sensor data
import numpy as np
temps = np.array([22.5, 23.0, 21.8])
print(temps.mean())
```

## 24. Pandas Basics
```python
# Analyze sales data
import pandas as pd
df = pd.DataFrame({"sales": [100, 200, 150]})
print(df["sales"].sum())
```

## 25. Matplotlib Basics
```python
# Plot monthly sales
import matplotlib.pyplot as plt
sales = [100, 200, 150]
plt.plot(sales)
plt.show()
```

## 26. Creating and Publishing Python Modules

### 1. Create Your Own Module

A Python module is simply a `.py` file containing functions, classes, or variables.

**Example: `mymath.py`**
```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b
```

**Usage:**
```python
import mymath

print(mymath.add(2, 3))
```

### 2. Organize as a Package

A package is a directory with an `__init__.py` file.

**Example:**
```
my_package/
    __init__.py
    math_utils.py
    string_utils.py
```

### 3. Add Metadata for Distribution

Create a `pyproject.toml` or `setup.py` file in your project root.

**Example: `pyproject.toml` (recommended)**
```toml
[project]
name = "my_package"
version = "0.1.0"
description = "A sample Python package"
authors = [{name = "Your Name", email = "your@email.com"}]
dependencies = []
```

### 4. Build and Publish to PyPI

Install build tools:
```bash
pip install build twine
```

Build your package:
```bash
python -m build
```

Upload to PyPI:
```bash
twine upload dist/*
```

### 5. Use as a Dependency

Others can install your package:
```bash
pip install my_package
```

And use it in their code:
```python
from my_package import math_utils
```

**Tip:** For more info, see [Packaging Python Projects](https://packaging.python.org/tutorials/packaging-projects/).


## 27. Python Decorators

Decorators allow you to modify the behavior of functions or classes.

```python
def log(func):
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__}")
        return func(*args, **kwargs)
    return wrapper

@log
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")
```

---

## 28. Generators and Iterators

Generators produce items one at a time and are memory efficient.

```python
def countdown(n):
    while n > 0:
        yield n
        n -= 1

for num in countdown(5):
    print(num)
```

---

## 29. Context Managers (`with` Statement)

Context managers handle setup and cleanup actions.

```python
with open("example.txt", "w") as f:
    f.write("Hello World!")
# File is automatically closed after the block
```

---

## 30. Multithreading and Multiprocessing

Parallel execution for performance.

```python
import threading

def worker():
    print("Worker running")

t = threading.Thread(target=worker)
t.start()
t.join()
```

---

## 31. Type Hinting and Static Analysis

Type hints improve code readability and help with static analysis.

```python
def add(a: int, b: int) -> int:
    return a + b
```

---

## 32. Unit Testing

Automated tests for code reliability.

```python
import unittest

class TestMath(unittest.TestCase):
    def test_add(self):
        self.assertEqual(2 + 3, 5)

unittest.main()
```

---

## 33. Logging

Track events and errors in your application.

```python
import logging

logging.basicConfig(level=logging.INFO)
logging.info("App started")
```

---

## 34. Argument Parsing (`argparse`)

Build command-line interfaces.

```python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument("--name")
args = parser.parse_args()
print(f"Hello, {args.name}")
```

---

## 35. Working with Databases (`sqlite3`)

Store and retrieve data using SQL.

```python
import sqlite3

conn = sqlite3.connect("test.db")
c = conn.cursor()
c.execute("CREATE TABLE IF NOT EXISTS users (name TEXT, age INTEGER)")
c.execute("INSERT INTO users VALUES (?, ?)", ("Alice", 30))
conn.commit()
conn.close()
```

---

## 36. Web Development (Flask Example)

Build web applications.

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello, World!"

# Run with: flask run
```

---

## 37. Asynchronous Programming (`asyncio`)

Handle concurrent tasks efficiently.

```python
import asyncio

async def main():
    print("Hello")
    await asyncio.sleep(1)
    print("World")

asyncio.run(main())
```