# PYTHON CODING QUESTIONS — SET 3 (InfoCepts Style)

---

## ✅ 1. Given a list, print elements that appear more than once.

```python
lst = [1,2,3,2,4,5,1]
freq = {}
dupes = []

for x in lst:
    if x in freq:
        freq[x] += 1
    else:
        freq[x] = 1

for key, val in freq.items():
    if val > 1:
        dupes.append(key)

print("Duplicates:", dupes)
```

---

## ✅ 2. Find the first non-repeating character in a string.

```python
text = input("Enter text: ")
freq = {}

for ch in text:
    freq[ch] = freq.get(ch, 0) + 1

ans = None
for ch in text:
    if freq[ch] == 1:
        ans = ch
        break

print("First non-repeating:", ans)
```

---

## ✅ 3. Find the second most frequent element in a list.

```python
lst = [1,1,2,2,2,3,3]
freq = {}

for x in lst:
    freq[x] = freq.get(x, 0) + 1

sorted_items = sorted(freq.items(), key=lambda x: x[1], reverse=True)

print("Second most frequent:", sorted_items[1][0])
```

---

## ✅ 4. Given a sentence, reverse each word but keep word order same.

```python
text = input("Enter sentence: ")

words = text.split()
result = []

for w in words:
    rev = ""
    for ch in w:
        rev = ch + rev
    result.append(rev)

print(" ".join(result))
```

---

## ✅ 5. Count characters that appear exactly twice.

```python
text = input("Enter string: ")
freq = {}
count_two = 0

for ch in text:
    freq[ch] = freq.get(ch, 0) + 1

for v in freq.values():
    if v == 2:
        count_two += 1

print("Characters appearing twice:", count_two)
```

---

## ✅ 6. Write a function to check if two lists are identical (same elements, same order).

```python
def are_equal(a, b):
    if len(a) != len(b):
        return False
    
    for i in range(len(a)):
        if a[i] != b[i]:
            return False
    return True

print(are_equal([1,2,3], [1,2,3]))
```

---

## ✅ 7. Convert a list of tuples into a dictionary.

```python
lst = [("a", 1), ("b", 2), ("c", 3)]
d = {}

for key, val in lst:
    d[key] = val

print(d)
```

---

## ✅ 8. From a mixed list, separate integers and strings.

```python
lst = [1, "hi", 2, "hello", 3]
ints = []
strings = []

for item in lst:
    if isinstance(item, int):
        ints.append(item)
    else:
        strings.append(item)

print("Integers:", ints)
print("Strings:", strings)
```

---

## ✅ 9. Check if a list is sorted (ascending).

```python
lst = [1,2,3,4,5]
sorted_flag = True

for i in range(len(lst)-1):
    if lst[i] > lst[i+1]:
        sorted_flag = False
        break

print("Sorted" if sorted_flag else "Not sorted")
```

---

## ✅ 10. Print numbers that appear only once in a list.

```python
lst = [1,2,2,3,4,4,5]
freq = {}

for x in lst:
    freq[x] = freq.get(x, 0) + 1

unique = []

for key, val in freq.items():
    if val == 1:
        unique.append(key)

print(unique)
```

---

## ✅ 11. Given a string of words, find the shortest and longest word.

```python
text = input("Enter text: ")

words = text.split()
shortest = words[0]
longest = words[0]

for w in words:
    if len(w) < len(shortest):
        shortest = w
    if len(w) > len(longest):
        longest = w

print("Shortest:", shortest)
print("Longest:", longest)
```

---

## ✅ 12. Count digits, alphabets, and special characters in a string.

```python
text = input("Enter text: ")

digits = 0
alphas = 0
special = 0

for ch in text:
    if ch.isdigit():
        digits += 1
    elif ch.isalpha():
        alphas += 1
    else:
        special += 1

print("Digits:", digits)
print("Alphabets:", alphas)
print("Special characters:", special)
```

---

## ✅ 13. Remove all special characters from a string.

```python
text = input("Enter text: ")
result = ""

for ch in text:
    if ch.isalnum() or ch == " ":
        result += ch

print(result)
```

---

## ✅ 14. Find the difference between maximum and minimum number in a list.

```python
lst = [5, 10, 2, 7, 9]

maxi = lst[0]
mini = lst[0]

for x in lst:
    if x > maxi:
        maxi = x
    if x < mini:
        mini = x

print("Difference:", maxi - mini)
```

---

## ✅ 15. Check if two strings are rotations of each other.

Example:  
"abcde" → "deabc" ✔ rotation

```python
s1 = input("Enter first string: ")
s2 = input("Enter second string: ")

if len(s1) == len(s2) and s2 in (s1 + s1):
    print("Rotation")
else:
    print("Not rotation")
```

---

## ✅ 16. Return all indices of an element in a list.

```python
lst = [1,2,3,2,4,2,5]
x = int(input("Enter element: "))

indices = []

for i in range(len(lst)):
    if lst[i] == x:
        indices.append(i)

print(indices)
```

---

## ✅ 17. Extract digits from a mixed string.

Input: "abc123de45" → Output: 12345

```python
text = input("Enter string: ")

digits = ""

for ch in text:
    if ch.isdigit():
        digits += ch

print(digits)
```

---

## ✅ 18. Convert a list of strings to uppercase.

```python
lst = ["hello", "world", "python"]
result = []

for word in lst:
    result.append(word.upper())

print(result)
```

---

## ✅ 19. Given a dictionary, find the key with the maximum value.

```python
d = {"a": 10, "b": 50, "c": 30}

max_key = None
max_val = float('-inf')

for key, val in d.items():
    if val > max_val:
        max_val = val
        max_key = key

print("Key with max value:", max_key)
```

---

## ✅ 20. Convert a number to binary without using bin().

```python
num = int(input("Enter number: "))
binary = ""

if num == 0:
    binary = "0"
else:
    while num > 0:
        binary = str(num % 2) + binary
        num //= 2

print("Binary:", binary)
```

---

