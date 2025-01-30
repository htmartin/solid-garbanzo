In Python, you can time an algorithm using the `time` module or the `timeit` module. Here are some common ways:

### **1. Using the `time` module**
This method records the start and end times and calculates the elapsed time.

```python
import time

# Start the timer
start_time = time.time()

# Code to time (Finding the max number in a list)
numbers = [12, 45, 78, 23, 89, 56, 90, 34]
max_number = numbers[0]
i = 1
while i < len(numbers):
    if numbers[i] > max_number:
        max_number = numbers[i]
    i += 1

# End the timer
end_time = time.time()

# Print elapsed time
print("The maximum number in the list is:", max_number)
print(f"Execution time: {end_time - start_time:.6f} seconds")
```

---

```
# Start the timer
start_time = time.time()

numbers = [12, 45, 78, 23, 89, 56, 90, 34]

# Initialize max_number with the first element of the list
max_number = numbers[0]

# Iterate through the list to find the maximum number
for num in numbers:
    if num > max_number:
        max_number = num

# End the timer (Fix)
end_time = time.time()

# Print the maximum number & execution time
print("The maximum number in the list is:", max_number)
print(f"Execution time: {end_time - start_time:.6f} seconds")
```



### The `for` loop version of the algorithm is **faster** than the `while` loop version because of differences in how Python executes these loops. 

### 🔍 **1. `for` Loop is Optimized in Python**
- The `for` loop is **optimized for iterating over sequences** like lists. Python handles the iteration internally using an efficient iterator, which reduces the number of explicit operations.
- In a `for` loop:
  ```python
  for num in numbers:
      if num > max_number:
          max_number = num
  ```
  - Python directly fetches each item from the list using an **iterator**.
  - The loop control is handled efficiently, minimizing overhead.

### `while` Loop Has More Overhead
- The `while` loop requires **manual indexing and comparison** before accessing elements:
  ```python
  i = 1
  while i < len(numbers):
      if numbers[i] > max_number:
          max_number = numbers[i]
      i += 1
  ```
  - Python has to **check the loop condition (`i < len(numbers)`) at every iteration**.
  - It also needs to **increment `i` manually (`i += 1`)**, which adds computational overhead.

### Additional Overhead of `while` Loop**
- `while` loops require:
  - A **manual index variable (`i`)**.
  - A **boundary check (`i < len(numbers)`)** on every iteration.
  - **Explicit list indexing (`numbers[i]`)**, which takes additional time compared to the `for` loop’s direct iteration.

### 🕒 **Performance Comparison**
Since `while` loops require more operations per iteration than `for` loops, they generally take **longer** to execute.



### WHy for is faster:
The `for` loop version of the algorithm is **faster** than the `while` loop version because of differences in how Python executes these loops. Here’s why:

### 1. `for` Loop is Optimized in Python
- The `for` loop is **optimized for iterating over sequences** like lists. Python handles the iteration internally using an efficient iterator, which reduces the number of explicit operations.

### What's an iterator

In Python, an iterator is a class (User defined object with attributes and methods):

Implements two special methods:
__iter__() → Returns the iterator object itself.
__next__() → Returns the next item in the sequence.
Automatically remembers where it left off when retrieving elements.
Raises StopIteration when there are no more elements.
Python automatically does the following behind the scenes:

Calls `iter(numbers)` to get an iterator object.

Calls `next(iterator)` to get the next item in the sequence without using an index.
Continues until StopIteration is raised (which happens when there are no more elements).


- In a `for` loop:
  ```python
  for num in numbers:
      if num > max_number:
          max_number = num
  ```
  - Python directly fetches each item from the list using an **iterator**.
  - The loop control is handled efficiently, minimizing overhead.

