
# Python Lists – Complete Notes

A **list** in Python is a mutable, ordered collection of items.  
Lists can store elements of mixed data types (numbers, strings, objects, even other lists).

---

## 📌 Creating Lists
```python
list1 = [1, 2, 3, 4]
list2 = ["apple", "banana", "cherry"]
list3 = [1, "hello", 3.14, True]
list4 = []  # empty list
list5 = list(range(5))  # [0, 1, 2, 3, 4]
```

---

## 📌 Indexing & Slicing
```python
nums = [10, 20, 30, 40, 50]
print(nums[0])     # 10 (first element)
print(nums[-1])    # 50 (last element)
print(nums[1:4])   # [20, 30, 40]
print(nums[:3])    # [10, 20, 30]
print(nums[::2])   # [10, 30, 50]
print(nums[::-1])  # [50, 40, 30, 20, 10] (reverse)
```

👉 Lists are **mutable** → elements can be modified.

```python
nums[2] = 99
print(nums)  # [10, 20, 99, 40, 50]
```

---

## 📌 List Operations
```python
a = [1, 2, 3]
b = [4, 5]
print(a + b)    # [1, 2, 3, 4, 5] (concatenation)
print(a * 2)    # [1, 2, 3, 1, 2, 3] (repetition)
print(2 in a)   # True (membership test)
print(len(a))   # 3 (length)
```

---

## 📌 Adding Elements
```python
fruits = ["apple"]
fruits.append("banana")    # ['apple', 'banana']
fruits.extend(["cherry", "mango"])  # ['apple', 'banana', 'cherry', 'mango']
fruits.insert(1, "grape")  # Insert at index 1
print(fruits)
```

---

## 📌 Removing Elements
```python
nums = [1, 2, 3, 4, 3]
nums.remove(3)   # removes first occurrence → [1, 2, 4, 3]
print(nums.pop()) # removes last element (3)
print(nums.pop(0)) # removes element at index 0 → 1
nums.clear()     # removes all elements → []
```

---

## 📌 Searching & Counting
```python
nums = [10, 20, 30, 20, 40]
print(nums.index(20))  # 1 (first index of 20)
print(nums.count(20))  # 2 (occurrences of 20)
```

---

## 📌 Sorting & Reversing
```python
nums = [4, 1, 3, 2]
nums.sort()         # [1, 2, 3, 4]
nums.sort(reverse=True)  # [4, 3, 2, 1]
print(sorted([3,1,2]))  # [1, 2, 3] (returns new list)
nums.reverse()      # Reverses list order
```

---

## 📌 Copying Lists
```python
a = [1, 2, 3]
b = a.copy()
c = list(a)
d = a[:]   # slicing copy
print(b, c, d)
```

⚠️ `b = a` does **not** create a copy (both refer to same list).

---

## 📌 List Comprehensions
```python
squares = [x**2 for x in range(5)]
print(squares)  # [0, 1, 4, 9, 16]

evens = [x for x in range(10) if x % 2 == 0]
print(evens)  # [0, 2, 4, 6, 8]
```

---

## 📌 Nested Lists (2D Lists)
```python
matrix = [[1, 2], [3, 4], [5, 6]]
print(matrix[0][1])  # 2
```

---

## 📌 Useful List Methods
```python
nums = [1, 2, 3]
nums.append(4)          # [1, 2, 3, 4]
nums.extend([5, 6])     # [1, 2, 3, 4, 5, 6]
nums.insert(2, 99)      # [1, 2, 99, 3, 4, 5, 6]
nums.remove(99)         # [1, 2, 3, 4, 5, 6]
nums.pop()              # removes last element
nums.clear()            # []
```

---

## 📌 List Tricks & Hacks

### Flatten a nested list
```python
nested = [[1, 2], [3, 4], [5, 6]]
flat = [x for row in nested for x in row]
print(flat)  # [1, 2, 3, 4, 5, 6]
```

### Remove duplicates (preserve order)
```python
nums = [1, 2, 2, 3, 1]
unique = list(dict.fromkeys(nums))
print(unique)  # [1, 2, 3]
```

### Swap two elements
```python
nums = [10, 20, 30]
nums[0], nums[2] = nums[2], nums[0]
print(nums)  # [30, 20, 10]
```

### Find max & min
```python
nums = [5, 8, 2, 9]
print(max(nums))  # 9
print(min(nums))  # 2
```

### List comprehension with condition
```python
nums = [1, 2, 3, 4, 5]
squared_evens = [x**2 for x in nums if x % 2 == 0]
print(squared_evens)  # [4, 16]
```

### Transpose a matrix
```python
matrix = [[1,2,3],[4,5,6]]
transpose = list(zip(*matrix))
print(transpose)  # [(1,4), (2,5), (3,6)]
```

### Most frequent element
```python
from collections import Counter
nums = [1,2,2,3,3,3,4]
print(Counter(nums).most_common(1))  # [(3, 3)]
```

### Flatten using sum()
```python
nested = [[1,2],[3,4]]
flat = sum(nested, [])
print(flat)  # [1, 2, 3, 4]
```

---

# ✅ Summary Notes
- Lists are **mutable, ordered collections**.  
- Support **indexing, slicing, concatenation, repetition, membership**.  
- Common methods: `append`, `extend`, `insert`, `remove`, `pop`, `clear`, `sort`, `reverse`.  
- Use **list comprehensions** for concise list creation.  
- Powerful tricks: flattening, removing duplicates, swapping, transposing, finding frequencies.  

---
