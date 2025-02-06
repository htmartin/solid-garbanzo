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

#### **2. Using Docstrings**
- **Question**: Why are docstrings important, and how can they be accessed for a function? Write an example.  
  
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

#### **4. Advanced Function Techniques**
- **Question**: Write a lambda function to compute the square of a number, and use it to calculate the square of 7.  

- **Question**: Demonstrate a function with `*args` and `**kwargs`.  

#### **5. Recursion and Generators**
- **Question**: Write a recursive function to compute the factorial of a number.  

- **Question**: Create a generator function `count_up_to` that yields numbers from 1 to a given number. Use it to generate numbers up to 5.  
  
