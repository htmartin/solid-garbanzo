### **Weekly Learning Objectives**

By the end of this week, students will be able to:

1. Explain the role of the PyData ecosystem in data science workflows and how NumPy complements other tools like pandas and Matplotlib.
2. Create and manipulate NumPy arrays, utilizing their efficient memory storage and high-performance capabilities compared to Python lists.
3. Apply vectorized operations and broadcasting in NumPy to perform efficient, element-wise computations and transformations on arrays.
4. Use advanced array manipulation techniques, including slicing, Boolean indexing, and reshaping, to prepare data for analysis and modeling tasks.
5. Perform fundamental linear algebra operations and random number generation using NumPy, applying these concepts to practical data science problems.

---

### Study Questions 

#### **1. Understanding the PyData Ecosystem**
- **Question**: How does NumPy fit within the PyData ecosystem, and why is it essential for data science?  
  **Answer**:  
  NumPy provides the foundational array structure and numerical operations that power data manipulation in Python. Its efficient handling of vectors, matrices, and linear algebra operations underpins tools like pandas (for tabular data manipulation) and scikit-learn (for machine learning). Its speed and efficiency make it indispensable in scientific computing.

---

#### **2. Creating and Manipulating NumPy Arrays**
- **Question**: Write Python code to create a NumPy array of integers from 1 to 10. Reshape it into a 2x5 matrix and calculate the sum of all elements.  
  **Answer**:  
  ```python
  import numpy as np

  array = np.arange(1, 11)  # Create array from 1 to 10
  matrix = array.reshape(2, 5)  # Reshape into 2x5 matrix
  total_sum = matrix.sum()  # Calculate the sum of all elements

  print(matrix)
  print(total_sum)
  ```
  **Output**:  
  ```
  [[ 1  2  3  4  5]
   [ 6  7  8  9 10]]
  55
  ```

---

#### **3. Vectorized Operations and Broadcasting**
- **Question**: What is vectorization, and how does it improve performance? Demonstrate with an example of squaring all elements in a NumPy array without using explicit loops.  
  **Answer**:  
  Vectorization applies operations across an entire array without the need for explicit loops, leveraging optimized, compiled code for performance.  
  ```python
  import numpy as np

  array = np.array([1, 2, 3, 4, 5])
  squared = array**2  # Vectorized squaring

  print(squared)  # Output: [ 1  4  9 16 25 ]
  ```

---

#### **4. Array Manipulation Techniques**
- **Question**: Given the NumPy array `np.array([1, 2, 3, 4, 5, 6])`, write code to:
  1. Select only even numbers using Boolean indexing.
  2. Reshape it into a 2x3 matrix.
  **Answer**:  
  ```python
  import numpy as np

  array = np.array([1, 2, 3, 4, 5, 6])

  # Boolean indexing for even numbers
  evens = array[array % 2 == 0]

  # Reshape into a 2x3 matrix
  reshaped = array.reshape(2, 3)

  print("Even numbers:", evens)
  print("Reshaped matrix:\n", reshaped)
  ```
  **Output**:  
  ```
  Even numbers: [2 4 6]
  Reshaped matrix:
  [[1 2 3]
   [4 5 6]]
  ```

---

#### **5. Linear Algebra and Random Number Generation**
- **Question**: Write Python code to:
  1. Generate a 3x3 matrix of random integers between 1 and 10.
  2. Compute its transpose and perform matrix multiplication with the original matrix.  
  **Answer**:  
  ```python
  import numpy as np

  # Generate a 3x3 matrix of random integers
  np.random.seed(42)  # Set seed for reproducibility
  matrix = np.random.randint(1, 11, size=(3, 3))

  # Transpose and matrix multiplication
  transpose = matrix.T
  result = np.dot(matrix, transpose)

  print("Original matrix:\n", matrix)
  print("Transpose:\n", transpose)
  print("Matrix multiplication result:\n", result)
  ```
  **Output**:  
  ```
  Original matrix:
  [[ 7  4  8]
   [ 5  7 10]
   [ 3  7  7]]
  Transpose:
  [[ 7  5  3]
   [ 4  7  7]
   [ 8 10  7]]
  Matrix multiplication result:
  [[129 138 122]
   [138 174 144]
   [122 144 123]]
  ```

