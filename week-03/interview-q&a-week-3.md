## Questions

1. **Given a list of numbers, write Python code to create a new list containing only the even numbers.**
2. **How would you create a dictionary where the keys are numbers from 1 to 10 and the values are the squares of those numbers?**
3. **Explain the difference between a list and a tuple in Python, providing examples of when you would use each.**
4. **Given two lists, write Python code to create a new list containing the elements that are common to both lists.**
5. **How can you efficiently remove duplicate elements from a list in Python?**

## Answers

1. **Answer 1** 
   ```python
   numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
   even_numbers = [num for num in numbers if num % 2 == 0] 
   print(even_numbers)  # Output: [2, 4, 6, 8, 10]
   ```

2. **Answer 2**
   ```python
   squares = {num: num**2 for num in range(1, 11)}
   print(squares) 
   ```

3. **Answer 3**
   * **List:** 
      - Mutable (can be changed after creation)
      - Represented by square brackets `[]`
      - Example: `my_list = [1, 2, 3]`
   * **Tuple:**
      - Immutable (cannot be changed after creation)
      - Represented by parentheses `()`
      - Example: `my_tuple = (1, 2, 3)`
      - Used when you want to ensure data remains constant, improve performance in some cases, or use tuples as keys in dictionaries.

4. **Answer 4**
   ```python
   list1 = [1, 2, 3, 4, 5]
   list2 = [4, 5, 6, 7, 8]
   common_elements = [item for item in list1 if item in list2]
   print(common_elements)  # Output: [4, 5] 
   ```

5. **Answer 5**
   ```python
   my_list = [1, 2, 2, 3, 3, 3, 4, 4, 5]
   unique_list = list(set(my_list)) 
   print(unique_list)  # Output: [1, 2, 3, 4, 5]
   ```

## Conceptual Questions

1. **Explain the concept of mutability in Python. How does it affect how you work with data structures?**
2. **Describe the process of creating a dictionary comprehension in Python. Provide a practical example.**
3. **What are the advantages of using list comprehensions over traditional `for` loops?**
4. **Explain the difference between a shallow copy and a deep copy of a list. When might you use each?**
5. **How can you use nested data structures (like a dictionary of lists) to represent real-world data, such as a collection of student records with their names, grades, and courses?**

## Conceptual Answers

1. **Answer 1**
   - Mutability refers to the ability to change an object after it's created. 
      - Mutable objects (like lists) can be modified in place.
      - Immutable objects (like tuples) cannot be changed once created.
   - Mutability has implications for how data is stored and passed around in your code, affecting performance and potential side effects.

2. **Answer 2**
   - Dictionary comprehensions provide a concise way to create dictionaries.
   - **Syntax:** `{key_expression: value_expression for item in iterable}`
   - **Example:** 
      ```python
      squares = {x: x**2 for x in range(1, 6)} 
      ```
      This creates a dictionary where the keys are numbers from 1 to 5 and the values are their squares.

3. **Answer 3**
   - **Advantages of list comprehensions:**
      - More concise and readable for certain operations.
      - Can be more efficient in terms of execution speed.
      - More Pythonic and often considered more elegant.

4. **Answer 4**
   - **Shallow Copy:** Creates a new list object but only copies the references to the original elements. If the original elements are mutable, changes to them will be reflected in the copy.
   - **Deep Copy:** Creates a new list object and recursively copies all the elements, creating new objects for any nested mutable objects. Changes to the original elements will not affect the copy.
   - Use a shallow copy when you want to create a separate view of the original list but don't need to completely isolate it. Use a deep copy when you need to ensure that the copy is completely independent of the original.

5. **Answer 5**
   - **Example:**
      ```python
      student_records = {
          "Alice": {"Math": 90, "Science": 85, "English": 92},
          "Bob": {"Math": 88, "Science": 95, "English": 80},
          "Charlie": {"Math": 78, "Science": 82, "English": 90}
      }
      ```
   - This nested structure allows for efficient organization and retrieval of student information. 
