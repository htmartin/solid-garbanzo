### Week 4 Learning Objectives

By the end of this lesson, students will be able to:

1. Explain the use and purpose of `for` and `while` loops, including their control mechanisms (`break`, `continue`, and `else`).  
2. Iterate over data structures like strings, lists, and ranges using Python loops.  
3. Apply the `range()` function to generate sequences with varying start, stop, and step values in practical programming scenarios.  
4. Analyze the behavior and efficiency of different loop structures and control statements in solving algorithmic problems.  
5. Design and implement nested loops and algorithmic solutions for real-world problems, optimizing for readability and efficiency.

---

### Questions to Assess Learning Objectives

#### 1. Explain the use and purpose of `for` and `while` loops, including their control mechanisms.

- Question: What is the difference between a `for` loop and a `while` loop in Python, and when would you use each?  
  Answer:  
  - A `for` loop iterates over a sequence (like a list, string, or range) and is used when the number of iterations is known.  
  - A `while` loop continues as long as a condition is true and is more flexible for situations where the number of iterations is unknown or depends on dynamic conditions.

- Question: What is the purpose of the `break`, `continue`, and `else` statements in loops?  
  Answer:  
  - `break`: Exits the loop immediately.  
  - `continue`: Skips the current iteration and proceeds to the next.  
  - `else`: Executes if the loop completes without encountering a `break`.

---

#### 2. Demonstrate how to iterate over data structures like strings, lists, and ranges.

- Question: Write a `for` loop to print each character in the string `"data"`.  
  Answer:  
  ```python
  for char in "data":
      print(char)
  ```

- Question: How would you iterate through the list `[1, 2, 3, 4]` to print each element multiplied by 2?  
  Answer:  
  ```python
  for num in [1, 2, 3, 4]:
      print(num  2)
  ```

---

#### 3. Apply the `range()` function to generate sequences.

- Question: How would you use the `range()` function to generate the numbers 0, 2, 4, 6, and 8?  
  Answer:  
  ```python
  for num in range(0, 10, 2):
      print(num)
  ```

- Question: Write a loop using `range()` to count down from 5 to 0.  
  Answer:  
  ```python
  for num in range(5, -1, -1):
      print(num)
  ```

---

#### 4. Analyze the behavior and efficiency of loop structures.

- Question: Compare the efficiency of a `for` loop using `range()` versus a `while` loop for iterating from 1 to 10.  
  Answer:  
  - A `for` loop is generally more efficient and readable for fixed ranges since it automatically handles iteration.  
  - A `while` loop requires manual management of the loop variable and condition, which can introduce errors or inefficiencies.

- Question: Why might using a `break` statement inside a loop improve efficiency?  
  Answer:  
  A `break` statement allows the loop to exit as soon as a desired condition is met, avoiding unnecessary iterations and improving runtime performance.

---

#### 5. Design and implement nested loops and algorithmic solutions.


- Question: Design an algorithm using loops to check if a number is prime.  
  Answer:  
  ```python
  num = 29  # Example number
  is_prime = True
  for i in range(2, int(num  0.5) + 1):
      if num % i == 0:
          is_prime = False
          break
  if is_prime:
      print(f"{num} is prime.")
  else:
      print(f"{num} is not prime.")
  ```

