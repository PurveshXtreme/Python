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
