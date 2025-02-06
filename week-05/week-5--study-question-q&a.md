### **Weekly Learning Objectives**

By the end of this week, students will be able to:

1. Define and call Python functions, explaining the roles of arguments, parameters, and return values in modular and reusable code.
2. Utilize docstrings to document Python functions and use `help()` to retrieve function documentation.
3. Distinguish between local and global variables and explain how Python's namespace and scope rules affect function behavior.
4. Apply advanced function techniques, including lambda functions, `*args`/`**kwargs`, and decorators, to enhance code flexibility and readability.
5. Implement recursion and generator functions to solve complex data processing problems efficiently.

---

### Study Questions

#### 1. Defining and Calling Functions
- **Question**: Write a function `calculate_area` that takes `length` and `width` as arguments and returns the area of a rectangle. How would you call this function with the arguments 5 and 10?  
  **Answer**:  
  ```python
  def calculate_area(length, width):
      return length * width

  # Calling the function
  area = calculate_area(5, 10)
  print(area)  # Output: 50
  ```

#### **2. Using Docstrings**
- **Question**: Why are docstrings important, and how can they be accessed for a function? Write an example.  
  **Answer**:  
  Docstrings are important because they provide a description of the function's purpose, inputs, and outputs, making the code easier to understand and maintain. They can be accessed using the `help()` function or `__doc__` attribute.  
  ```python
  def calculate_area(length, width):
      """Calculate the area of a rectangle.
      Args:
          length (float): The length of the rectangle.
          width (float): The width of the rectangle.
      Returns:
          float: The area of the rectangle.
      """
      return length * width

  print(calculate_area.__doc__)
  help(calculate_area)
  ```

#### **3. Local vs Global Variables**
- **Question**: What will the following code output? Explain why.  
  ```python
  x = 10

  def update_x():
      x = 5
      print("Inside function:", x)

  update_x()
  print("Outside function:", x)
  ```  
  **Answer**:  
  ```
  Inside function: 5
  Outside function: 10
  ```
  The function defines a local variable `x` inside its scope, which does not affect the global `x`. The `print` statement inside the function refers to the local variable, while the one outside refers to the global variable.

#### **4. Advanced Function Techniques**
- **Question**: Write a lambda function to compute the square of a number, and use it to calculate the square of 7.  
  **Answer**:  
  ```python
  square = lambda x: x**2
  result = square(7)
  print(result)  # Output: 49
  ```

- **Question**: Demonstrate a function with `*args` and `**kwargs`.  
  **Answer**:  
  ```python
  def print_info(*args, **kwargs):
      print("Positional arguments:", args)
      print("Keyword arguments:", kwargs)

  print_info(1, 2, 3, name="Alice", age=25)
  # Output:
  # Positional arguments: (1, 2, 3)
  # Keyword arguments: {'name': 'Alice', 'age': 25}
  ```

#### **5. Recursion and Generators**
- **Question**: Write a recursive function to compute the factorial of a number.  
  **Answer**:  
  ```python
  def factorial(n):
      if n == 0 or n == 1:
          return 1
      else:
          return n * factorial(n - 1)

  print(factorial(5))  # Output: 120
  ```

- **Question**: Create a generator function `count_up_to` that yields numbers from 1 to a given number. Use it to generate numbers up to 5.  
  **Answer**:  
  ```python
  def count_up_to(maximum):
      count = 1
      while count <= maximum:
          yield count
          count += 1

  for number in count_up_to(5):
      print(number)
  # Output:
  # 1
  # 2
  # 3
  # 4
  # 5
  ```
