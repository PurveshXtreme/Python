# Table of Contents

- [Python String Functions (Most Important)](#python-string-functions-most-important)
- [Python Arithmetic Operators](#python-arithmetic-operators)
- [Python Logical Operators](#python-logical-operators)
- [IF–ELSE Ladder in Python](#ifelse-ladder-in-python)
- [Python `range()` Function](#python-range-function)
- [Loops in Python](#loops-in-python)
- [Python Lists](#python-lists)
- [Python Tuples](#python-tuples)
- [Python Sets](#python-sets)
- [Python Dictionary](#python-dictionary)
- [Functions in Python](#functions-in-python)
- [File Handling in Python](#-file-handling-in-python)
- [Errors & Exception Handling](#-errors--exception-handling-in-python)
- [Object-Oriented Programming (OOP) in Python](#-object-oriented-programming-oop-in-python)


# Python String Functions (Most Important)

## Basic String Properties
- Strings are immutable
- Access using indexing: `s[0]`, `s[-1]`
- Slicing: `s[start:end]`, `s[::-1]` (reverse)

---

## Case Conversion
- `s.upper()` → Converts to uppercase  
- `s.lower()` → Converts to lowercase  
- `s.capitalize()` → First letter capital  
- `s.title()` → First letter of each word capital  
- `s.swapcase()` → Upper ↔ Lower case

---

## Searching
- `s.find(sub)` → Returns index of substring (or -1)  
- `s.rfind(sub)` → Last occurrence  
- `s.index(sub)` → Like find but throws error if not found  
- `s.count(sub)` → Count occurrences

---

## Modifying / Replacing
- `s.replace(old, new)` → Replace substring  
- `s.strip()` → Remove spaces (left & right)  
- `s.lstrip()` → Left trim  
- `s.rstrip()` → Right trim  

---

## Splitting / Joining
- `s.split()` → Split by whitespace → returns list  
- `s.split(',')` → Split by specific delimiter  
- `" ".join(list)` → Join list into string with separator  

---

## Checking String Type (Boolean functions)
- `s.isalpha()` → Only alphabets  
- `s.isdigit()` → Only digits  
- `s.isalnum()` → Alphanumeric  
- `s.islower()` → All lowercase  
- `s.isupper()` → All uppercase  
- `s.isspace()` → Only whitespace  
- `s.startswith('x')` → Checks prefix  
- `s.endswith('x')` → Checks suffix  

---

## Formatting
- `s.format()` → Placeholder formatting  
- `f"{var}"` → f-string formatting (modern & preferred)  

Example:
```python
name = "Purvesh"
age = 21
msg = f"My name is {name} and I am {age} years old."
```

---

## Useful String Operations
- `len(s)` → Length of string  
- `min(s)`, `max(s)` → Smallest/largest character  
- `sorted(s)` → Sort characters in string  
- `s[::-1]` → Reverse string (slicing)  

---

## Summary (Most Asked in Interviews)
1. `split()`  
2. `join()`  
3. `replace()`  
4. `strip()`  
5. `find()`  
6. Slicing `[::-1]`  
7. Case conversions: `upper()`, `lower()`


---


# Python Arithmetic Operators

## 1. Addition
**Operator:** `+`  
**Usage:** Adds two numbers  
```python
a + b
```

---

## 2. Subtraction
**Operator:** `-`  
**Usage:** Subtracts second number from first  
```python
a - b
```

---

## 3. Multiplication
**Operator:** `*`  
**Usage:** Multiplies numbers  
```python
a * b
```

---

## 4. Division
**Operator:** `/`  
**Usage:** Returns float division  
```python
a / b   # result is always float
```

---

## 5. Floor Division
**Operator:** `//`  
**Usage:** Returns integer division (floors result)  
```python
a // b
```

Example:  
`7 // 2 → 3`

---

## 6. Modulus
**Operator:** `%`  
**Usage:** Returns remainder  
```python
a % b
```

Example:  
`7 % 3 → 1`

---

## 7. Exponentiation
**Operator:** `**`  
**Usage:** Power of a number  
```python
a ** b
```

Example:  
`2 ** 3 → 8`

---

# Summary Table

| Operator | Meaning | Example | Result |
|---------|---------|---------|--------|
| `+` | Addition | `5 + 2` | `7` |
| `-` | Subtraction | `5 - 2` | `3` |
| `*` | Multiplication | `5 * 2` | `10` |
| `/` | Division (float) | `5 / 2` | `2.5` |
| `//` | Floor Division | `5 // 2` | `2` |
| `%` | Modulus | `5 % 2` | `1` |
| `**` | Exponent | `5 ** 2` | `25` |

---
---

# Python Logical Operators

Logical operators are used to combine conditional statements.  
Python has **three** logical operators:

---

## 1. `and`
Returns **True** only if **both** conditions are true.

```python
x = 5
x > 2 and x < 10   # True
```

Truth table:

| A | B | A and B |
|---|---|---------|
| True | True | True |
| True | False | False |
| False | True | False |
| False | False | False |

---

## 2. `or`
Returns **True** if **at least one** condition is true.

```python
x = 5
x > 10 or x == 5   # True
```

Truth table:

| A | B | A or B |
|---|---|--------|
| True | True | True |
| True | False | True |
| False | True | True |
| False | False | False |

---

## 3. `not`
Reverses the boolean value.

```python
x = True
not x      # False
```

Truth table:

| A | not A |
|----|-------|
| True | False |
| False | True |

---

# Combined Example

```python
age = 20
is_student = True

if age > 18 and is_student:
    print("Eligible")
```

```python
if age < 18 or is_student:
    print("Discount applies")
```

```python
if not is_student:
    print("Full price")
```

---

# Important Notes
- `and` has higher precedence than `or`
- Use parentheses `()` to control evaluation order  
  Example:  
  ```python
  True or False and False   # → True
  (True or False) and False # → False
  ```

---
---

# IF–ELSE Ladder in Python

IF–ELSE ladder is used when we have **multiple conditions** to check, one after another.

---

## Basic Syntax

```python
if condition1:
    # code block 1
elif condition2:
    # code block 2
elif condition3:
    # code block 3
else:
    # default block (executes if none above are true)
```

---
---

# Python `range()` Function

`range()` is used to generate a sequence of numbers.  
It is commonly used in loops.

---

## Syntax

```python
range(stop)
range(start, stop)
range(start, stop, step)
```

---

# 1. `range(stop)`
Generates numbers from `0` to `stop-1`.

Example:

```python
for i in range(5):
    print(i)
```

Output:
```
0 1 2 3 4
```

---

# 2. `range(start, stop)`
Generates numbers from `start` to `stop-1`.

```python
for i in range(2, 7):
    print(i)
```

Output:
```
2 3 4 5 6
```

---

# 3. `range(start, stop, step)`
`step` defines the increment or decrement.

### Example: Counting by steps
```python
for i in range(1, 10, 2):
    print(i)
```

Output:
```
1 3 5 7 9
```

### Example: Reverse range
```python
for i in range(10, 0, -1):
    print(i)
```

Output:
```
10 9 8 7 6 5 4 3 2 1
```

---

# Properties of `range()`
- It does **not** store all numbers in memory → memory-efficient  
- It returns a **range object**  
- Commonly used in `for` loops  

---

# Convert range to list (if needed)

```python
list(range(5))
```

Output:
```
[0, 1, 2, 3, 4]
```

---

# Summary Table

| Usage | Meaning | Example | Output |
|-------|---------|---------|--------|
| `range(n)` | 0 → n-1 | `range(4)` | `0 1 2 3` |
| `range(a, b)` | a → b-1 | `range(3, 7)` | `3 4 5 6` |
| `range(a, b, c)` | a → step c | `range(2, 10, 3)` | `2 5 8` |
| Reverse | Count backward | `range(5, 0, -1)` | `5 4 3 2 1` |

---
---


# Loops in Python

Python has **two main loops**:
1. `for` loop  
2. `while` loop  

Both are used to repeat a block of code multiple times.

---

# 1. FOR LOOP

Used to iterate over:
- lists
- strings
- tuples
- dictionaries
- range()

## Basic Syntax
```python
for variable in sequence:
    # code block
```

---

## Example 1: Loop through a list
```python
nums = [10, 20, 30]
for n in nums:
    print(n)
```

---

## Example 2: Loop through string
```python
for ch in "info":
    print(ch)
```

---

## Example 3: Loop with range()
```python
for i in range(5):
    print(i)
```
Output:
```
0 1 2 3 4
```

---

## Example 4: Reverse loop
```python
for i in range(10, 0, -1):
    print(i)
```

---

# 2. WHILE LOOP

Executes **as long as** the condition is True.

## Syntax
```python
while condition:
    # code block
```

---

## Example 1: Simple counter
```python
i = 1
while i <= 5:
    print(i)
    i += 1
```

---

## Example 2: Loop until user stops (logical)
```python
choice = "y"
while choice == "y":
    print("Running...")
    choice = input("Continue? (y/n): ")
```

---

# 3. BREAK and CONTINUE (Very Important)

## break → stops the loop completely
```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

---

## continue → skips current iteration
```python
for i in range(6):
    if i == 3:
        continue
    print(i)
```

---

# 4. Nested Loops
Loop inside another loop.

```python
for i in range(3):
    for j in range(2):
        print(i, j)
```

---

# 5. else with loops (Python special feature)

`else` executes **only if loop completes normally** (not broken).

```python
for i in range(5):
    print(i)
else:
    print("Loop completed!")
```

---

# When to Use Which Loop?

| Loop Type | Use Case |
|----------|----------|
| `for` loop | When iterating through known elements (list, string, range) |
| `while` loop | When repetition depends on a condition, not a sequence |

---

# Quick Summary

- `for` → fixed number of iterations  
- `while` → repeat until condition becomes false  
- `break` → stop loop  
- `continue` → skip iteration  
- `else` after loop → runs when loop ends normally  

---
---


# Python Lists

A **list** is a collection in Python that:
- is **ordered**
- is **mutable** (can be changed)
- allows **duplicates**
- can contain **mixed data types**

Example:
```python
my_list = [10, 20, 30, "hello", 3.14]
```

---

# Creating a List

```python
nums = [1, 2, 3, 4]
mixed = [10, "abc", 4.5, True]
empty = []
```

---

# Accessing Elements

```python
nums = [10, 20, 30, 40]
print(nums[0])   # 10
print(nums[-1])  # 40 (last element)
```

---

# List Slicing

```python
nums = [10, 20, 30, 40, 50]

nums[1:4]    # [20, 30, 40]
nums[:3]     # [10, 20, 30]
nums[2:]     # [30, 40, 50]
nums[::-1]   # Reverse list → [50, 40, 30, 20, 10]
```

---

# Common List Methods (IMPORTANT)

## 1. append() – Add element at end
```python
nums.append(99)
```

## 2. insert() – Insert at index
```python
nums.insert(1, 50)   # insert 50 at index 1
```

## 3. remove() – Remove first occurrence
```python
nums.remove(20)
```

## 4. pop() – Remove and return element
```python
nums.pop()     # removes last
nums.pop(2)    # removes index 2
```

## 5. sort() – Sort list (ascending)
```python
nums.sort()
```

## 6. reverse() – Reverse list
```python
nums.reverse()
```

## 7. count() – Count occurrences
```python
nums.count(10)
```

## 8. index() – Get index of element
```python
nums.index(30)
```

---

# Looping Through List

```python
for item in nums:
    print(item)
```

Using index:
```python
for i in range(len(nums)):
    print(nums[i])
```

---

# Check Membership

```python
if 20 in nums:
    print("Found")
```

---

# List Comprehension (Quick Way to Create Lists)

```python
squares = [x*x for x in range(5)]
```
Output:
```
[0, 1, 4, 9, 16]
```

---

# Adding Two Lists

```python
a = [1,2,3]
b = [4,5]
c = a + b        # [1,2,3,4,5]
```

---

# List Functions Summary Table

| Method | Meaning |
|--------|---------|
| append() | Add element at end |
| insert() | Add element at index |
| remove() | Remove by value |
| pop() | Remove by index |
| sort() | Sort list |
| reverse() | Reverse list |
| count() | Count occurrences |
| index() | Find index of element |
| extend() | Add elements of another list |

---

# Important Interview Notes

- Lists are **mutable**  
- Indexing starts from **0**  
- Negative indexing allowed: `list[-1]`  
- Slicing does **not** modify original list  
- `append()` adds **one** element; `extend()` adds a **list**  

---
---

# Python Tuples

A **tuple** in Python is:
- **Ordered**
- **Immutable** (cannot be changed)
- Allows **duplicate values**
- Can store **mixed data types**

Example:
```python
my_tuple = (10, 20, 30, "hello", 3.14)
```

---

# Creating Tuples

## 1. Normal tuple
```python
t = (1, 2, 3)
```

## 2. Mixed types
```python
t = (10, "abc", 4.5, True)
```

## 3. Empty tuple
```python
t = ()
```

## 4. Single-element tuple (IMPORTANT)
Must include a **comma**:
```python
t = (5,)      # tuple
t = (5)       # NOT a tuple, just an integer
```

---

# Accessing Elements

```python
t = (10, 20, 30)

t[0]       # 10
t[-1]      # 30
```

---

# Tuple Slicing

```python
t = (10, 20, 30, 40, 50)

t[1:4]     # (20, 30, 40)
t[::-1]    # Reverse → (50, 40, 30, 20, 10)
```

---

# Why Tuples?

## ✔ Immutable → cannot be changed  
This makes tuples:
- Safe for storing fixed data  
- Faster than lists  
- Usable as dictionary keys  

---

# Tuple Methods (Only 2)

## 1. count()
```python
t.count(10)
```

## 2. index()
```python
t.index(30)
```

These are the **only two methods** because tuples are immutable.

---

# Looping Through Tuple

```python
for x in t:
    print(x)
```

---

# Tuple Packing and Unpacking

## Packing
```python
t = 1, 2, 3
```

## Unpacking
```python
a, b, c = t
```

---

# Tuple vs List (Important Interview Question)

| Feature | List | Tuple |
|--------|------|--------|
| Mutability | Mutable | Immutable |
| Speed | Slower | Faster |
| Methods | Many | Only 2 |
| Use Case | Dynamic data | Fixed data |
| Syntax | `[ ]` | `( )` |

---

# When to Use Tuples?

- When data should **not change**  
- When using as **keys in dictionaries**  
- When performance matters  
- When returning **multiple values** from a function

---

# Example: Function Returns Tuple
```python
def calc(a, b):
    return a + b, a * b

result = calc(4, 5)
print(result)   # (9, 20)
```

---
---

# Python Sets

A **set** in Python is:
- **Unordered** (no index)
- **Mutable** (can add/remove items)
- Contains **unique elements only**
- Cannot contain **lists or dictionaries** (because they are mutable)

Example:
```python
s = {1, 2, 3, 4}
```

---

# Creating a Set

```python
s = {10, 20, 30}
```

## Empty set (IMPORTANT)
```python
s = set()   # correct
s = {}      # this creates a dictionary, NOT a set
```

---

# Properties of Sets

- No duplicate values  
  ```python
  s = {1, 2, 2, 3}   # {1, 2, 3}
  ```
- No indexing: `s[0]` → ❌ error  
- Order is **not guaranteed**

---

# Adding and Removing Elements

## add()
```python
s.add(50)
```

## remove()
Throws error if item not found.
```python
s.remove(20)
```

## discard()
Does NOT throw error.
```python
s.discard(20)
```

## pop()
Removes a random element.
```python
s.pop()
```

## clear()
```python
s.clear()
```

---

# Set Operations (IMPORTANT FOR INTERVIEWS)

## 1. Union → combines both sets
```python
a = {1, 2, 3}
b = {3, 4, 5}

a.union(b)     # {1, 2, 3, 4, 5}
a | b
```

---

## 2. Intersection → common elements
```python
a.intersection(b)   # {3}
a & b
```

---

## 3. Difference → elements only in A
```python
a.difference(b)     # {1, 2}
a - b
```

---

## 4. Symmetric Difference → elements NOT common
```python
a.symmetric_difference(b)  # {1, 2, 4, 5}
a ^ b
```

---

# Looping Through a Set

```python
for x in s:
    print(x)
```
(Order will be random)

---

# Check Membership

```python
if 10 in s:
    print("Found")
```

---

# Converting Lists to Sets (remove duplicates)

```python
nums = [1,2,2,3,3,4]
unique_nums = set(nums)
```

---

# Summary Table

| Feature | Set |
|--------|------|
| Ordered? | No |
| Mutable? | Yes |
| Allows duplicates? | No |
| Indexing? | No |
| Methods? | add, remove, discard, pop, union, intersection, difference |

---

# When to Use Sets?

- When you need **unique values**
- When you need **fast membership checking** → `x in set`
- When performing **mathematical operations** like union/intersection

---

# Example: Remove duplicates
```python
data = [1,2,2,3,4,4,5]
unique = list(set(data))
```

---
---

# Python Dictionary

A **dictionary** in Python is:
- A collection of **key-value pairs**
- **Unordered** (in Python 3.7+, preserves insertion order)
- **Mutable** (can be changed)
- Keys must be **unique** and **immutable** (str, int, tuple)

Example:
```python
student = {
    "name": "Purvesh",
    "age": 21,
    "city": "Pune"
}
```

---

# Creating a Dictionary

```python
d = {"a": 1, "b": 2, "c": 3}
```

Empty dictionary:
```python
d = {}
```

---

# Accessing Values

```python
student["name"]     # Purvesh
```

Use `.get()` to avoid errors:
```python
student.get("age")          # 21
student.get("address")      # None (no error)
```

---

# Adding / Updating Values

```python
student["age"] = 22        # update
student["college"] = "DY Patil"   # add new key
```

---

# Removing Items

## pop()
Removes a key and returns its value.
```python
student.pop("age")
```

## popitem()
Removes the last inserted item.
```python
student.popitem()
```

## del
```python
del student["city"]
```

## clear()
```python
student.clear()
```

---

# Important Dictionary Methods

## keys()
```python
student.keys()     # dict_keys(['name', 'age'])
```

## values()
```python
student.values()
```

## items()
Returns key-value pairs.
```python
for k, v in student.items():
    print(k, v)
```

## update()
```python
student.update({"age": 23, "city": "Mumbai"})
```

---

# Looping Through Dictionary

### Loop through keys:
```python
for key in student:
    print(key)
```

### Loop through values:
```python
for val in student.values():
    print(val)
```

### Loop through key-value pairs:
```python
for key, val in student.items():
    print(key, val)
```

---

# Check if Key Exists

```python
if "age" in student:
    print("Present")
```

---

# Dictionary Comprehension

```python
squares = {x: x*x for x in range(5)}
```

Output:
```
{0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

---

# Nested Dictionary

```python
info = {
    "student1": {"name": "Raj", "age": 21},
    "student2": {"name": "Purvesh", "age": 22}
}
```

---

# Summary Table

| Feature | Dictionary |
|--------|-------------|
| Type | Key-value pair |
| Mutable | Yes |
| Allows duplicate keys | No |
| Allows duplicate values | Yes |
| Indexing | No (use keys) |
| Methods | keys(), values(), items(), update(), pop(), popitem() |

---

# When to Use Dictionaries?

- When you need **mapping** between keys & values  
- When fast lookup is needed (`O(1)` average time)  
- For JSON-like data  
- For storing structured data  

---
---

# Functions in Python

A **function** is a block of reusable code that performs a specific task.

---

# Why use Functions?
- Avoid repeating code
- Organize code into logical blocks
- Increase readability
- Make code reusable and maintainable

---

# Defining a Function

```python
def function_name(parameters):
    # code block
    return value
```

---

# 1. Simple Function (No Parameters)

```python
def greet():
    print("Hello, World!")

greet()
```

---

# 2. Function With Parameters

```python
def add(a, b):
    return a + b

print(add(5, 3))   # 8
```

---

# 3. Function With Default Parameters

```python
def greet(name="User"):
    print("Hello", name)

greet()           # Hello User
greet("Purvesh")  # Hello Purvesh
```

---

# 4. Function Returning Multiple Values (Tuple)

```python
def calc(a, b):
    return a + b, a * b

x, y = calc(4, 5)
print(x, y)   # 9 20
```

---

# 5. Keyword Arguments

```python
def user(name, age):
    print(name, age)

user(age=21, name="Purvesh")
```

---

# 6. Arbitrary Arguments (`*args`)
Used when number of arguments is unknown.

```python
def total(*nums):
    print(sum(nums))

total(1, 2, 3, 4)   # 10
```

`*args` is a **tuple**.

---

# 7. Arbitrary Keyword Arguments (`**kwargs`)
Used for unknown keyword args.

```python
def show_details(**info):
    print(info)

show_details(name="Purvesh", age=21)
```

`**kwargs` is a **dictionary**.

---

# 8. Nested Functions

```python
def outer():
    def inner():
        print("Inside inner")
    inner()

outer()
```

---

# 9. Lambda Functions (Anonymous Functions)

```python
square = lambda x: x * x
print(square(5))   # 25
```

Used for short one-line functions.

---

# 10. Docstring (Function Documentation)

```python
def add(a, b):
    """This function adds two numbers."""
    return a + b

print(add.__doc__)
```

---

# Important Notes

- A function stops executing when it hits a `return` statement.
- If no return value is given → returns `None` by default.
- Parameters = variables inside function definition  
- Arguments = values passed during function call  

---

# Summary Table

| Concept | Description |
|--------|-------------|
| `def` | Used to define a function |
| parameters | Inputs inside `def` |
| arguments | Values passed to function |
| `return` | Sends value back |
| `*args` | Variable-length positional args |
| `**kwargs` | Variable-length keyword args |
| Lambda | One-line function |

---
---

# 📌 File Handling in Python

Python provides built-in functions to read and write files.

---

# 1. Opening a File

Syntax:
```python
f = open("filename.txt", "mode")
```

Common modes:

| Mode | Meaning |
|------|---------|
| `"r"` | Read (default), error if file not found |
| `"w"` | Write, creates new file or overwrites existing |
| `"a"` | Append, adds content to end |
| `"x"` | Create file, error if exists |
| `"r+"` | Read + Write |
| `"b"` | Binary mode (e.g., "rb") |

Example:
```python
f = open("test.txt", "r")
```

---

# 2. Reading a File

```python
f = open("test.txt", "r")
data = f.read()        # read entire file
print(data)
f.close()
```

Read line by line:
```python
f = open("test.txt", "r")
for line in f:
    print(line)
f.close()
```

Read first line:
```python
f.readline()
```

Read all lines into list:
```python
f.readlines()
```

---

# 3. Writing to a File

```python
f = open("data.txt", "w")
f.write("Hello World")
f.close()
```

Append mode:
```python
f = open("data.txt", "a")
f.write("\nNew Line Added")
f.close()
```

---

# 4. Using `with` Statement (Recommended)

Automatically closes the file.

```python
with open("test.txt", "r") as f:
    print(f.read())
```

---

# 📌 Errors & Exception Handling in Python

Errors stop program execution unless handled.

---

# 1. Try–Except Block

```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
```

---

# 2. Catching Multiple Exceptions

```python
try:
    a = int("abc")
except (ValueError, TypeError):
    print("Error occurred")
```

---

# 3. Finally Block

Always executes.

```python
try:
    f = open("abc.txt")
except FileNotFoundError:
    print("File not found")
finally:
    print("Execution completed")
```

---

# 4. Else Block

Runs only if no exception occurs.

```python
try:
    x = 5 + 5
except:
    print("Error")
else:
    print("No error")
```

---

# 5. Raise Your Own Exception

```python
def check_age(age):
    if age < 18:
        raise Exception("Age below 18 not allowed")

check_age(16)
```

---

# 📌 Object-Oriented Programming (OOP) in Python

OOP helps organize code into classes and objects.

Core concepts:
- **Class**
- **Object**
- **Constructor**
- **Methods**
- **Inheritance**
- **Encapsulation**
- **Polymorphism**

---

# 1. Creating a Class & Object

```python
class Student:
    def __init__(self, name, age):   # constructor
        self.name = name
        self.age = age

    def display(self):
        print(self.name, self.age)

s1 = Student("Purvesh", 21)
s1.display()
```

---

# 2. Inheritance

```python
class Animal:
    def sound(self):
        print("Animal Sound")

class Dog(Animal):  # Dog inherits Animal
    def sound(self):
        print("Bark")

d = Dog()
d.sound()
```

---

# 3. Encapsulation (Hiding data)

Use `_` or `__`.

```python
class Person:
    def __init__(self):
        self.__salary = 50000   # private variable

    def get_salary(self):
        return self.__salary
```

---

# 4. Polymorphism

Same method name, different behavior.

```python
class Bird:
    def fly(self):
        print("Bird can fly")

class Penguin(Bird):
    def fly(self):
        print("Penguin cannot fly")

b = Bird()
p = Penguin()

b.fly()
p.fly()
```

---

# 5. Method Overloading (Not truly supported in Python)

Use default parameters instead.

```python
def add(a, b, c=0):
    return a + b + c
```

---

# 6. Method Overriding

Child class changes method of parent class.

(Example shown in inheritance section)

---

# Quick Summary Table

| Concept | Meaning |
|--------|---------|
| Class | Blueprint |
| Object | Instance of class |
| Constructor | `__init__()` method |
| Inheritance | Reuse parent class |
| Encapsulation | Hide details |
| Polymorphism | Same interface, different behavior |

---
---
