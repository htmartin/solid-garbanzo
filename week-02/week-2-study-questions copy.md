### Week 2 Learning Objectives

By the end of this week, students will be able to:

1. Describe the purpose and structure of Python as a high-level programming language, including its syntax simplicity and utility in data science. 
2. Demonstrate how to use Python’s core data types and perform typecasting operations to ensure data integrity in programs. 
3. Construct conditional statements, loops, and nested control structures to solve algorithmic problems. 
4. Analyze the behavior of variables, assignments, and references in Python, distinguishing between mutable and immutable data types. 
5. Debug Python code effectively using techniques like print statements, kernel restarts, and error tracing in Jupyter Notebook. 

---

### Questions and Answers

#### 1. Describe the purpose and structure of Python.
Question:  
What makes Python a suitable programming language for beginners and professionals in data science?  
Answer:  
Python is a high-level, user-friendly programming language known for its simplicity, clear syntax, and readability. Its flexibility and extensive ecosystem of libraries like NumPy and pandas make it ideal for data analysis and scientific computing. Python's interpreted nature allows for interactive development, making it accessible to beginners while being powerful enough for professionals.

---

#### 2. Demonstrate how to use Python’s core data types.
Question:  
Write a Python script that converts the string `"123"` to an integer, multiplies it by 2, and then converts the result back to a string.  
Answer:  
```python
num_str = "123"
num_int = int(num_str)  # Convert to integer
result = num_int  2    # Multiply by 2
result_str = str(result)  # Convert back to string
print(result_str)  # Output: "246"
```

---

#### 3. Construct conditional statements and loops.
Question:  
Write a Python function that takes a number as input and prints whether it is even or odd. Use a loop to repeat this for numbers 1 through 10.  
Answer:  
```python
def check_even_odd(num):
    if num % 2 == 0:
        print(f"{num} is even")
    else:
        print(f"{num} is odd")

for i in range(1, 11):
    check_even_odd(i)
```

---

#### 4. Analyze variable behavior and data types.
Question:  
Explain the difference between mutable and immutable objects in Python, and provide an example where modifying a mutable object affects another variable pointing to it.  
Answer:  
Mutable objects (e.g., lists) can be modified after creation, whereas immutable objects (e.g., strings, integers) cannot. If two variables reference the same mutable object, changes to one will affect the other.  

Example:  
```python
list1 = [1, 2, 3]
list2 = list1  # Both reference the same list object
list1.append(4)  # Modify the list through list1
print(list2)  # Output: [1, 2, 3, 4], list2 also reflects the change
```

---

#### 5. Debug Python code effectively.
Question:  
The following code throws an error. Identify and fix it using debugging techniques:  
```python
x = 10
if x = 10:
    print("x is 10")
```
Answer:  
Error: The `=` operator is used for assignment, not comparison. Replace it with `==`.  

Corrected Code:  
```python
x = 10
if x == 10:
    print("x is 10")
```  

Debugging steps:
1. Read the error message to locate the problematic line.
2. Verify syntax rules (e.g., comparison vs. assignment).
3. Use `print(x)` to confirm the variable's value, if necessary.

---

This structure ensures that the objectives align with Bloom’s Taxonomy and provides students with clear, measurable skills for assessing their understanding.