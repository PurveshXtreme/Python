# PYTHON CODING QUESTIONS — SET 1 (with full solutions)

---

## ✅ 1. Check if a number is even or odd.

```python
num = int(input("Enter a number: "))

if num % 2 == 0:
    print("Even")
else:
    print("Odd")
```

---

## ✅ 2. Find the largest of 3 numbers.

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
c = int(input("Enter third number: "))

if a >= b and a >= c:
    print("Largest:", a)
elif b >= a and b >= c:
    print("Largest:", b)
else:
    print("Largest:", c)
```

---

## ✅ 3. Sum of digits of a number.

```python
num = int(input("Enter number: "))
total = 0

while num > 0:
    digit = num % 10
    total += digit
    num //= 10

print("Sum of digits:", total)
```

---

## ✅ 4. Reverse a string without using slicing.

```python
text = input("Enter string: ")
rev = ""

for ch in text:
    rev = ch + rev

print("Reversed string:", rev)
```

---

## ✅ 5. Count vowels in a string.

```python
text = input("Enter string: ").lower()
vowels = "aeiou"
count = 0

for ch in text:
    if ch in vowels:
        count += 1

print("Vowel count:", count)
```

---

## ✅ 6. Check if a string is palindrome.

```python
text = input("Enter a string: ")

rev = ""
for ch in text:
    rev = ch + rev

if rev == text:
    print("Palindrome")
else:
    print("Not Palindrome")
```

---

## ✅ 7. Print Fibonacci series of N terms.

```python
n = int(input("Enter number of terms: "))

a, b = 0, 1

for i in range(n):
    print(a, end=" ")
    a, b = b, a + b
```

---

## ✅ 8. Find factorial of a number (loop).

```python
num = int(input("Enter number: "))
fact = 1

for i in range(1, num + 1):
    fact *= i

print("Factorial:", fact)
```

---

## ✅ 9. Remove duplicates from a list.

```python
lst = [1, 2, 2, 3, 3, 4]
unique_list = []

for item in lst:
    if item not in unique_list:
        unique_list.append(item)

print(unique_list)
```

---

## ✅ 10. Find second largest number in a list (without sort).

```python
lst = [10, 25, 3, 99, 48]

largest = float('-inf')
second = float('-inf')

for num in lst:
    if num > largest:
        second = largest
        largest = num
    elif num > second and num != largest:
        second = num

print("Second largest:", second)
```

---

## ✅ 11. Count frequency of each element in a list.

```python
lst = [1, 1, 2, 2, 2, 3]
freq = {}

for num in lst:
    if num in freq:
        freq[num] += 1
    else:
        freq[num] = 1

print(freq)
```

---

## ✅ 12. Merge two dictionaries.

```python
d1 = {"a": 1, "b": 2}
d2 = {"c": 3, "d": 4}

merged = {**d1, **d2}

print(merged)
```

---

## ✅ 13. Print all even numbers from 1 to N.

```python
n = int(input("Enter N: "))

for i in range(1, n + 1):
    if i % 2 == 0:
        print(i)
```

---

## ✅ 14. Print multiplication table of a number.

```python
num = int(input("Enter number: "))

for i in range(1, 11):
    print(num, "x", i, "=", num * i)
```

---

## ✅ 15. Reverse a list using loop only.

```python
lst = [10, 20, 30, 40]
rev = []

for item in lst:
    rev.insert(0, item)

print("Reversed list:", rev)
```

---

## ✅ 16. Check if a key exists in a dictionary.

```python
d = {"name": "Purvesh", "age": 21}

key = input("Enter key to check: ")

if key in d:
    print("Key exists")
else:
    print("Key does not exist")
```

---

## ✅ 17. Find common elements between two lists.

```python
a = [1, 2, 3]
b = [2, 3, 4]
common = []

for item in a:
    if item in b:
        common.append(item)

print("Common elements:", common)
```

---

## ✅ 18. Count words in a string.

```python
text = input("Enter text: ")

words = text.split()
print("Number of words:", len(words))
```

---

## ✅ 19. Find max and min without using max(), min().

```python
lst = [5, 9, 1, 4, 2]

maximum = lst[0]
minimum = lst[0]

for num in lst:
    if num > maximum:
        maximum = num
    if num < minimum:
        minimum = num

print("Max:", maximum)
print("Min:", minimum)
```

---

## ✅ 20. Convert two lists into a dictionary.

```python
keys = ["a", "b", "c"]
values = [1, 2, 3]

result = {}

for i in range(len(keys)):
    result[keys[i]] = values[i]

print(result)
```

---

