### 1. General Knowledge Data Science Interview Questions about Sequences, Dictionaries & Immutability


### Questions  

1. What are the key differences between lists, tuples, and sets in Python?
2. How do you check if a key exists in a dictionary, and what are the ways to retrieve a value for a given key?
3. Explain the concept of immutability in Python. How does it apply to tuples and dictionaries?
4. How do dictionaries maintain order, and how has this changed in recent versions of Python?
5. What are the advantages and use cases for using a tuple over a list in Python?

### Answers

1. **Key differences between lists, tuples, and sets:**
   - **Lists**: Mutable, ordered, allow duplicate elements, and can be indexed and sliced.
   - **Tuples**: Immutable, ordered, allow duplicate elements, and can also be indexed and sliced.
   - **Sets**: Mutable, unordered, do not allow duplicate elements, and cannot be indexed.

2. **Checking key existence and retrieving a value in a dictionary:**
   - To check if a key exists: Use the `in` keyword (`key in dictionary`).
   - To retrieve a value: Use `dictionary[key]` (raises `KeyError` if key doesn't exist) or `dictionary.get(key)` (returns `None` if key doesn't exist).

3. **Immutability concept:**
   - In Python, immutability means an object’s state cannot be changed after it is created.
   - **Tuples** are immutable, meaning once a tuple is created, its elements cannot be modified, added, or removed. This ensures data integrity and can improve performance.
   - **Dictionaries** are mutable, meaning their content (key-value pairs) can be changed. However, keys in a dictionary must be immutable types (e.g., integers, strings, or tuples) because dictionary keys are hashed.

4. **Order in dictionaries:**
   - Prior to Python 3.7, dictionaries did not maintain the insertion order of keys.
   - Since Python 3.7, dictionaries maintain the order in which keys are inserted. This change is due to an optimization in Python's implementation, making dictionaries both ordered and efficient.

5. **Advantages of tuples over lists:**
   - **Immutability**: Tuples, being immutable, are faster and more memory-efficient than lists. They also provide a form of protection for data that should not be modified.
   - **Use cases**: Tuples are ideal for representing fixed collections of values (e.g., coordinates, RGB colors) or for using as dictionary keys.

   ### 1.  Coding/Scripting Data Science Interview Questions about Sequences, Dictionaries & Immutability

   ### Questions

1. Write a Python script that removes all duplicate elements from a list while preserving the order of the remaining elements.  
2. Given a list of tuples, write a Python script to convert this list into a dictionary where the first element of each tuple becomes the key, and the second element becomes the value. Handle potential duplicate keys by keeping only the first occurrence.
3. How would you implement a script that counts the frequency of elements in a list using a dictionary?  
4. Write a Python script that demonstrates the immutability of a tuple by attempting to modify one of its elements, and handle the resulting error.
5. Write a Python script that merges two dictionaries, where values for matching keys are combined into a list of values from both dictionaries.

### Answers

### 1. Remove Duplicate Elements from a List While Preserving Order

```python
data = [3, 1, 4, 1, 5, 9, 2, 6, 3, 4, 9]
seen = set()
result = []

for item in data:
    if item not in seen:
        result.append(item)
        seen.add(item)

print(result)  # Output: [3, 1, 4, 5, 9, 2, 6]
```

### 2. Convert a List of Tuples into a Dictionary, Keeping Only the First Occurrence of Duplicate Keys

```python
tuples_list = [(1, 'a'), (2, 'b'), (1, 'c'), (3, 'd'), (2, 'e')]
result = {}

for key, value in tuples_list:
    if key not in result:
        result[key] = value

print(result)  # Output: {1: 'a', 2: 'b', 3: 'd'}
```

### 3. Count the Frequency of Elements in a List Using a Dictionary

```python
data = [3, 1, 4, 1, 5, 9, 2, 6, 3, 4, 9]
frequency = {}

for item in data:
    if item in frequency:
        frequency[item] += 1
    else:
        frequency[item] = 1

print(frequency)  # Output: {3: 2, 1: 2, 4: 2, 5: 1, 9: 2, 2: 1, 6: 1}
```

### 4. Demonstrate the Immutability of a Tuple

```python
t = (1, 2, 3)

try:
    t[0] = 10  # Attempt to modify the first element
except TypeError as e:
    print(f"Error: {e}")  # Output: Error: 'tuple' object does not support item assignment
```

### 5. Merge Two Dictionaries, Combining Values of Matching Keys into a List

```python
dict1 = {'a': 1, 'b': 2, 'c': 3}
dict2 = {'b': 4, 'c': 5, 'd': 6}
merged = {}

for key in dict1:
    if key in dict2:
        merged[key] = [dict1[key], dict2[key]]
    else:
        merged[key] = dict1[key]

for key in dict2:
    if key not in merged:
        merged[key] = dict2[key]

print(merged)  # Output: {'a': 1, 'b': [2, 4], 'c': [3, 5], 'd': 6}
```