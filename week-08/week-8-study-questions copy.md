### **Weekly Learning Objectives**

By the end of this week, students will be able to:

1. Design Python classes that implement inheritance, enabling the reuse of code and the creation of hierarchical relationships between parent and child classes.
2. Use polymorphism and duck typing to write flexible, interchangeable code that can process objects with similar behaviors regardless of their class types.
3. Define and override magic methods like `__init__`, `__str__`, and `__eq__` to customize class behavior for operations such as initialization, string representation, and comparisons.
4. Apply composition and aggregation to model real-world relationships between objects, emphasizing "has-a" over "is-a" where appropriate.
5. Create efficient data models using Python's dataclasses and named tuples, reducing boilerplate code while maintaining readability and performance.

---

### Study Questions

#### **1. Inheritance and Method Overriding**
- **Question**: Write a parent class `Animal` with a method `speak()` that prints "Animal speaks." Create a subclass `Dog` that overrides `speak()` to print "Woof!"  

- **Question**: How does method overriding support polymorphism?  
  **Answer**: Method overriding allows subclasses to provide specific implementations of methods from the parent class. Polymorphism ensures that the method call behaves appropriately for the actual object type, allowing flexible and interchangeable code.

---

#### **2. Polymorphism and Duck Typing**
- **Question**: Demonstrate polymorphism by defining a `Shape` class with a `draw()` method and subclasses `Circle` and `Square` that implement `draw()` differently.  
  
- **Question**: What is duck typing in Python? Provide an example.  

#### **3. Magic Methods**
- **Question**: Define a class `Point` that supports equality comparison using the `__eq__` magic method.  
  
- **Question**: Why would you override the `__str__` method? Provide an example.  

#### **4. Composition and Aggregation**
- **Question**: Create a `Car` class that uses composition to include an `Engine` class as an attribute.  

#### **5. Dataclasses and Named Tuples**
- **Question**: Use a dataclass to define a `Student` class with attributes `name` and `grades` (list of grades). Include a method to calculate the average grade.  
  