### Week 3 Learning Objectives 

By the end of this lesson, students will be able to:

1. Describe Python's core data structures (lists, tuples, dictionaries, and sets) and explain their distinct properties, including mutability and immutability.
2. Demonstrate the ability to manipulate lists and dictionaries by performing operations such as appending, slicing, merging, and copying.
3. Create and transform data structures with list comprehensions, dictionary comprehensions, and functional techniques like `zip()`.
4. Analyze the behavior of mutable objects in Python and differentiate between shallow and deep copies in terms of side effects and references.
5. Create nested data structures (e.g., dictionaries of lists) to solve real-world data organization and processing challenges.

---

### Questions and Answers

#### Objective 1: Describe Python's core data structures
Question:  
Describe the difference between a list and a tuple in Python. Provide an example where using a tuple is preferable to a list.  

Answer:  
- Difference: A list is mutable, meaning its elements can be changed, while a tuple is immutable and cannot be altered after creation.  
- Example: Tuples are preferable when storing fixed data that should not be modified, such as geographical coordinates `(latitude, longitude)`.

---

#### Objective 2: Demonstrate list and dictionary manipulation
Question:  
Given the list `numbers = [1, 2, 3, 4, 5]`, demonstrate how to:  
1. Append the number 6.  
2. Remove the third element.  
3. Slice the list to include only the first three elements.  

Answer:  
1. `numbers.append(6)` → `[1, 2, 3, 4, 5, 6]`  
2. `numbers.pop(2)` → `[1, 2, 4, 5, 6]`  
3. `numbers[:3]` → `[1, 2, 4]`  

---

#### Objective 3: Apply comprehensions and functional techniques
Question:  
Write a list comprehension to create a list of squares of even numbers from 1 to 10.  

Answer:  
`[x2 for x in range(1, 11) if x % 2 == 0]` → `[4, 16, 36, 64, 100]`  

---

#### Objective 4: Analyze behavior of mutable objects
Question:  
Explain the difference between shallow and deep copies in Python with an example.  

Answer:  
- Difference: A shallow copy creates a new object but does not copy nested objects, so changes to nested elements affect both copies. A deep copy duplicates all levels of the object.  
- Example:  
  ```python
  import copy
  original = [1, [2, 3]]
  shallow = copy.copy(original)
  deep = copy.deepcopy(original)
  shallow[1][0] = 99
  print(original)  # Output: [1, [99, 3]]
  print(deep)      # Output: [1, [2, 3]]
  ```

---

#### Objective 5: Create nested data structures
Question:  
Create a nested dictionary to represent a library system with categories "Fiction" and "Non-Fiction," each containing a list of books.  

Answer:  
```python
library = {
    "Fiction": ["1984", "The Great Gatsby"],
    "Non-Fiction": ["Sapiens", "Educated"]
}
print(library["Fiction"])  # Output: ['1984', 'The Great Gatsby']
```  

These objectives and questions ensure students engage with both theoretical and practical aspects of Python's data structures and operations.