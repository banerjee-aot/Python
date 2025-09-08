
# Python Strings – Complete Notes

Strings in Python are **sequences of characters** enclosed in single (`' '`), double (`" "`), or triple quotes (`''' '''` / ``).

---

## 📌 Creating Strings
```python
s1 = 'Hello'
s2 = "World"
s3 = '''This is 
a multiline string'''
print(s1, s2, s3)
```

---

## 📌 String Indexing & Slicing
```python
text = "Python"
print(text[0])     # P (1st character)
print(text[-1])    # n (last character)
print(text[0:4])   # Pyth (slice)
print(text[:3])    # Pyt
print(text[2:])    # thon
print(text[::-1])  # nohtyP (reverse)
```
👉 Strings are immutable (cannot be changed directly).

---

## 📌 String Operations
```python
# Concatenation
print("Hello " + "World")   # Hello World

# Repetition
print("Ha" * 3)             # HaHaHa

# Membership test
print("Py" in "Python")     # True
print("Java" not in "Python") # True

# Length
print(len("Python"))        # 6
```

---

## 📌 Escape Sequences
```python
print("Hello\nWorld")   # New line
print("Tab\tSpace")     # Tab space
print("She said \"Hi\"") # Escaping quotes
```

---

## 📌 Raw Strings
Normally, escape sequences like `\n` or `\t` are interpreted as newline and tab.  
**Raw strings** treat backslashes `\` as normal characters.

```python
print("C:\new\folder")   # C:
ewolder (interprets \n as newline)
print(r"C:\new\folder")  # C:\new\folder (raw string, keeps \n)
```
👉 Useful for regex patterns, Windows file paths, etc.

---

## 📌 String Formatting

### f-strings (recommended)
```python
name = "Alice"
age = 25
print(f"My name is {name} and I am {age} years old.")
```

### format()
```python
print("Name: {}, Age: {}".format("Bob", 30))
print("Name: {1}, Age: {0}".format(30, "Bob"))
```

### % formatting (old style)
```python
print("Name: %s, Age: %d" % ("Charlie", 28))
```

---

## 📌 Common String Methods

### Case Conversion
```python
text = "hello world"
print(text.upper())   # HELLO WORLD
print(text.lower())   # hello world
print(text.title())   # Hello World
print(text.capitalize()) # Hello world
print("PyThOn".casefold()) # python (best for case-insensitive)
```

### Checking Content
```python
print("abc".isalnum())  # True (letters/numbers only)
print("123".isdigit())  # True
print("abc".isalpha())  # True
print("   ".isspace())  # True
print("Python".isidentifier()) # True (valid variable name)
print("PYTHON".isupper())  # True
print("python".islower())  # True
print("Title Case".istitle()) # True
```

### Searching & Finding
```python
text = "hello world"
print(text.find("world"))    # 6 (index)
print(text.index("world"))   # 6 (error if not found)
print(text.rfind("l"))       # 9 (last index)
print(text.count("l"))       # 3
print(text.startswith("he")) # True
print(text.endswith("ld"))   # True
```

### Modifying Strings
```python
text = "   Python   "
print(text.strip())   # Removes spaces both sides
print(text.lstrip())  # Left strip
print(text.rstrip())  # Right strip
print("one,two,three".split(","))  # ['one','two','three']
print(" ".join(["I","love","Python"])) # I love Python
print("hello world".replace("world", "Python")) # hello Python
```

### Alignment & Padding
```python
print("Python".center(10, "-")) # --Python--
print("Python".ljust(10, "*"))  # Python****
print("Python".rjust(10, "*"))  # ****Python
print("42".zfill(5))           # 00042
```

### Encoding & Decoding
```python
text = "hello"
encoded = text.encode("utf-8")
print(encoded)             # b'hello'
print(encoded.decode())    # hello
```

---

## 📌 String Tricks & Hacks

### Reverse a string
```python
s = "Python"
print(s[::-1])  # nohtyP
```

### Swap case
```python
print("Hello".swapcase())  # hELLO
```

### Remove duplicates
```python
s = "banana"
print("".join(dict.fromkeys(s)))  # ban
```

### Palindrome check
```python
word = "madam"
print(word == word[::-1])  # True
```

### Most frequent character
```python
from collections import Counter
s = "mississippi"
print(Counter(s).most_common(1))  # [('i', 4)]
```

### Anagram check
```python
s1, s2 = "listen", "silent"
print(sorted(s1) == sorted(s2))  # True
```

### Remove vowels
```python
s = "beautiful"
print("".join([ch for ch in s if ch not in "aeiou"])) # btfl
```

---

# ✅ Summary Notes
- Strings are **immutable sequences of characters**.  
- Use **indexing/slicing** to extract substrings.  
- `+`, `*`, `in` are used for concatenation, repetition, and membership.  
- `strip()`, `replace()`, `split()`, `join()` are key methods for text cleaning.  
- `upper()`, `lower()`, `title()`, `capitalize()` handle case transformations.  
- **Raw strings** preserve backslashes (useful for regex & file paths).  
- **String formatting**: f-strings (best), `format()`, or `%`.  
- Many **built-in methods** simplify searching, validation, and alignment.  
- Hacks like palindrome check, anagram, removing duplicates are easy with string operations.  

---
