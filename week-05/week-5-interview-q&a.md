# Week 5 

## General knowledge Data Science Interview Questions 

### Questions

1. What is a function in Python, and why are functions important for writing modular code?
2. How do you define and call a function in Python, and what are the roles of parameters and arguments in functions?
3. What is the difference between the `return` statement and docstrings in Python functions?
4. What is the role of the call stack in Python's function execution flow?
5. How do local and global variables differ, and what are the best practices for using global variables inside functions?

### Answers

1. A function in Python is a block of reusable code that performs a specific task. Functions are important because they allow code to be modular, making it easier to organize, reuse, and maintain, especially in large programs. They improve code readability and reduce redundancy.

2. A function in Python is defined using the `def` keyword, followed by the function name and parentheses. Inside the parentheses, parameters can be listed. The function is called by using its name followed by parentheses, optionally passing arguments. Parameters are placeholders in the function, while arguments are the actual values passed to the function during a call.

3. The `return` statement in a Python function is used to send a result back to the calling code, allowing further manipulation of the output. Docstrings, on the other hand, are used to document the purpose of the function, including its inputs and outputs, and are accessible via the `help()` function. While `return` deals with functionality, docstrings enhance code readability and usability.

4. The call stack is a structure Python uses to manage function execution. When a function is called, a new frame is added to the call stack, and control passes to the function. Once the function completes, control returns to the previous point in the code, and the frame is removed from the stack. This process helps Python keep track of function calls and their order of execution.

5. Local variables are those defined within a function and are only accessible inside that function. Global variables are defined outside all functions and can be accessed from any part of the program. However, modifying global variables within a function requires the `global` keyword. Best practices suggest minimizing the use of global variables to avoid unintended side effects and make code easier to debug and maintain.


## Coding/Scripting Data Science Interview Questions 

### Questions

1. Write a Python function that calculates the factorial of a given number using recursion.
2. Write a Python function that takes two arguments and swaps them using a return statement.
3. Write a Python function that computes the nth Fibonacci number using recursion.
4. Write a Python function that checks if a given string is a palindrome, considering the string case-insensitive.
5. Write a Python function that sums all elements in a nested list, handling both integers and sublists recursively.

---

### Answers

1. 
```python
def factorial(n):
    """Returns the factorial of a given number n."""
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)
```

2. 
```python
def swap(a, b):
    """Swaps two variables and returns them in swapped order."""
    return b, a
```

3. 
```python
def fibonacci(n):
    """Returns the nth Fibonacci number using recursion."""
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)
```

4. 
```python
def is_palindrome(s):
    """Checks if a string is a palindrome, ignoring case."""
    s = s.lower()
    return s == s[::-1]
```

5. 
```python
def sum_nested_list(lst):
    """Sums all elements in a nested list, handling sublists recursively."""
    total = 0
    for element in lst:
        if isinstance(element, list):
            total += sum_nested_list(element)
        else:
            total += element
    return total
```
