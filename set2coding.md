# PYTHON CODING QUESTIONS — SET 2 (Medium Level)

---

## ✅ 1. Find the number of occurrences of each character in a string.

```python
text = input("Enter string: ")
freq = {}

for ch in text:
    if ch in freq:
        freq[ch] += 1
    else:
        freq[ch] = 1

print(freq)
```

---

## ✅ 2. Remove all vowels from a string.

```python
text = input("Enter text: ")
vowels = "aeiouAEIOU"
result = ""

for ch in text:
    if ch not in vowels:
        result += ch

print("After removing vowels:", result)
```

---

## ✅ 3. Find all pairs in a list whose sum equals a target.

```python
lst = [1, 2, 3, 4, 5, 6]
target = int(input("Enter target sum: "))

for i in range(len(lst)):
    for j in range(i + 1, len(lst)):
        if lst[i] + lst[j] == target:
            print(lst[i], lst[j])
```

---

## ✅ 4. Check if two strings are anagrams.

```python
s1 = input("Enter first string: ")
s2 = input("Enter second string: ")

if sorted(s1) == sorted(s2):
    print("Anagram")
else:
    print("Not Anagram")
```

---

## ✅ 5. Find the longest word in a sentence.

```python
text = input("Enter sentence: ")

words = text.split()
longest = words[0]

for word in words:
    if len(word) > len(longest):
        longest = word

print("Longest word:", longest)
```

---

## ✅ 6. Print a list in chunks of size N.

```python
lst = [1,2,3,4,5,6,7,8,9]
n = int(input("Enter chunk size: "))

for i in range(0, len(lst), n):
    print(lst[i:i+n])
```

---

## ✅ 7. Find common elements from 3 lists.

```python
a = [1,2,3,4]
b = [2,3,5]
c = [3,6]

common = []

for x in a:
    if x in b and x in c:
        common.append(x)

print(common)
```

---

## ✅ 8. Count uppercase and lowercase letters in a string.

```python
text = input("Enter string: ")

upper = 0
lower = 0

for ch in text:
    if ch.isupper():
        upper += 1
    elif ch.islower():
        lower += 1

print("Uppercase:", upper)
print("Lowercase:", lower)
```

---

## ✅ 9. Find all unique elements from two lists.

```python
a = [1,2,3,4]
b = [3,4,5,6]

unique = []

for x in a + b:
    if x not in unique:
        unique.append(x)

print(unique)
```

---

## ✅ 10. Check if a number is prime.

```python
num = int(input("Enter number: "))
is_prime = True

if num <= 1:
    is_prime = False
else:
    for i in range(2, num):
        if num % i == 0:
            is_prime = False
            break

print("Prime" if is_prime else "Not Prime")
```

---

## ✅ 11. Print all prime numbers from 1 to N.

```python
n = int(input("Enter N: "))

for num in range(2, n+1):
    prime = True
    for i in range(2, num):
        if num % i == 0:
            prime = False
            break
    if prime:
        print(num, end=" ")
```

---

## ✅ 12. Rotate a list by K positions.

```python
lst = [1,2,3,4,5]
k = int(input("Enter rotation value: "))

k = k % len(lst)
rotated = lst[k:] + lst[:k]

print(rotated)
```

---

## ✅ 13. Flatten a nested list.

```python
nested = [[1,2], [3,4], [5]]
flat = []

for sub in nested:
    for item in sub:
        flat.append(item)

print(flat)
```

---

## ✅ 14. Remove all occurrences of an element from a list.

```python
lst = [1,2,2,3,2,4]
x = int(input("Enter element to remove: "))

result = []

for item in lst:
    if item != x:
        result.append(item)

print(result)
```

---

## ✅ 15. Find the first repeating element in a list.

```python
lst = [1, 5, 2, 3, 5, 2]
seen = set()
repeat = None

for item in lst:
    if item in seen:
        repeat = item
        break
    seen.add(item)

print("First repeating:", repeat)
```

---

## ✅ 16. Convert a string to a dictionary of character counts.

```python
text = input("Enter text: ")
d = {}

for ch in text:
    if ch in d:
        d[ch] += 1
    else:
        d[ch] = 1

print(d)
```

---

## ✅ 17. Find intersection of sets without using set().

```python
a = [1,2,3,4]
b = [3,4,5]

common = []

for x in a:
    if x in b:
        common.append(x)

print(common)
```

---

## ✅ 18. Print pattern (triangle).

```python
n = int(input("Enter rows: "))

for i in range(1, n + 1):
    print("*" * i)
```

---

## ✅ 19. Separate even and odd numbers from a list.

```python
lst = [1,2,3,4,5,6]
even = []
odd = []

for num in lst:
    if num % 2 == 0:
        even.append(num)
    else:
        odd.append(num)

print("Even:", even)
print("Odd:", odd)
```

---

## ✅ 20. Count how many words start with a vowel.

```python
text = input("Enter sentence: ").lower()
words = text.split()

count = 0
vowels = "aeiou"

for w in words:
    if w[0] in vowels:
        count += 1

print("Words starting with vowel:", count)
```

---

