### **Weekly Learning Objectives**

By the end of this week, students will be able to:

1. Evaluate algorithm efficiency using asymptotic analysis, applying Big-O and Big-Theta notation to classify algorithms based on growth rates.
2. Implement algorithms for linear and bisection search in Python, analyzing their time complexities and justifying their use cases.
3. Measure the execution time of Python functions using modules like `time` and `timeit` and explain the influence of dataset size on runtime performance.
4. Apply recursive and iterative techniques to solve computational problems, including efficient implementations like Kadane’s algorithm.
5. Demonstrate proficiency with Python’s module and package system to structure code and use external libraries for data processing tasks.

---

### **Study Questions**

#### **1. Evaluating Algorithm Efficiency**
- **Question**: Explain the difference between Big-O and Big-Theta notation. Provide an example of when to use each.  
  **Answer**:  
  - **Big-O** describes the upper bound or worst-case scenario of an algorithm's growth rate. It is used to ensure an algorithm will not exceed a certain runtime.  
  - **Big-Theta** provides a tighter bound, describing both the upper and lower bounds. It is used when the growth rate is well understood and behaves predictably.  
  - Example:  
    - Linear search: \( O(n) \) in the worst case but \( \Theta(n) \) when analyzing both best and worst cases consistently.

#### **2. Linear and Bisection Search**
- **Question**: Write Python code for a bisection search algorithm to find an element in a sorted list. What is its time complexity?  
  **Answer**:  
  ```python
  def bisection_search(arr, target):
      start, end = 0, len(arr) - 1
      while start <= end:
          mid = (start + end) // 2
          if arr[mid] == target:
              return mid
          elif arr[mid] < target:
              start = mid + 1
          else:
              end = mid - 1
      return -1

  # Time complexity: O(log n)
  ```
  
#### **3. Measuring Execution Time**
- **Question**: How can you measure the execution time of a function in Python? Demonstrate with an example.  
  **Answer**:  
  ```python
  import time

  def example_function():
      total = 0
      for i in range(1000000):
          total += i
      return total

  start_time = time.time()
  example_function()
  end_time = time.time()

  print(f"Execution time: {end_time - start_time} seconds")
  ```

#### **4. Recursive and Iterative Techniques**
- **Question**: Implement Kadane’s algorithm to find the maximum subarray sum in a list. Explain why it is more efficient than a naive approach.  
  **Answer**:  
  ```python
  def kadane(arr):
      max_current = max_global = arr[0]
      for x in arr[1:]:
          max_current = max(x, max_current + x)
          if max_current > max_global:
              max_global = max_current
      return max_global

  # Efficiency: O(n), as it processes the array in a single pass.
  ```

- **Naive approach**:
  - Brute force using nested loops results in \( O(n^2) \), as it evaluates all possible subarrays.

#### **5. Python Modules and Packages**
- **Question**: What is the difference between a Python module and a package? How would you create a package for your project?  
  **Answer**:  
  - A **module** is a single Python file containing definitions and functions (e.g., `math.py`).
  - A **package** is a collection of modules grouped into a directory with an `__init__.py` file, allowing hierarchical organization.
  - To create a package:  
    ```
    my_package/
    ├── __init__.py
    ├── module1.py
    └── module2.py
    ```

- **Usage**:
  ```python
  from my_package.module1 import some_function
  some_function()
  ```