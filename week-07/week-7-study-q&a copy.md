### **Weekly Learning Objectives**

By the end of this week, students will be able to:

1. Define and initialize Python classes using the `class` keyword, understanding the roles of attributes, the `__init__` method, and the `self` parameter.
2. Differentiate between class and instance attributes and implement them in class design for real-world modeling scenarios.
3. Apply encapsulation to manage access to class attributes using private variables, getter and setter methods, and Python's `@property` decorator.
4. Explain and use instance, class, and static methods within Python classes, identifying their appropriate use cases.
5. Build and utilize custom Python classes to solve domain-specific problems, integrating principles of object-oriented programming like encapsulation and abstraction.

---

### Study Questions

#### **1. Defining and Initializing Classes**
- **Question**: Write a Python class `Car` that has attributes `make`, `model`, and `year`. Include an `__init__` method to initialize these attributes. Create an instance of the class for a 2020 Toyota Corolla.  
  **Answer**:  
  ```python
  class Car:
      def __init__(self, make, model, year):
          self.make = make
          self.model = model
          self.year = year

  my_car = Car("Toyota", "Corolla", 2020)
  print(my_car.make, my_car.model, my_car.year)
  # Output: Toyota Corolla 2020
  ```

#### **2. Class vs. Instance Attributes**
- **Question**: Explain the difference between class attributes and instance attributes. Provide an example where both are used.  
  **Answer**:  
  - **Class attributes** are shared across all instances of a class, while **instance attributes** are unique to each instance.  
  ```python
  class Dog:
      species = "Canis familiaris"  # Class attribute
      def __init__(self, name, age):
          self.name = name  # Instance attribute
          self.age = age    # Instance attribute

  dog1 = Dog("Buddy", 5)
  dog2 = Dog("Luna", 3)
  print(Dog.species)  # Output: Canis familiaris
  print(dog1.name, dog1.age)  # Output: Buddy 5
  print(dog2.name, dog2.age)  # Output: Luna 3
  ```

#### **3. Encapsulation and Property Decorators**
- **Question**: Modify the `Car` class to make the `year` attribute private. Add getter and setter methods using the `@property` decorator to manage access.  
  **Answer**:  
  ```python
  class Car:
      def __init__(self, make, model, year):
          self.make = make
          self.model = model
          self.__year = year  # Private attribute

      @property
      def year(self):
          return self.__year

      @year.setter
      def year(self, value):
          if value > 1885:  # Year of the first car
              self.__year = value
          else:
              raise ValueError("Invalid year for a car!")

  my_car = Car("Toyota", "Corolla", 2020)
  print(my_car.year)  # Output: 2020
  my_car.year = 2021
  print(my_car.year)  # Output: 2021
  ```

#### **4. Method Types**
- **Question**: Write a Python class `MathOperations` with three methods: an instance method `add` that adds two numbers, a class method `description` that returns a string description, and a static method `square` that returns the square of a number.  
  **Answer**:  
  ```python
  class MathOperations:
      def add(self, x, y):
          return x + y  # Instance method

      @classmethod
      def description(cls):
          return "This class provides basic math operations."  # Class method

      @staticmethod
      def square(x):
          return x ** 2  # Static method

  math_ops = MathOperations()
  print(math_ops.add(3, 5))  # Output: 8
  print(MathOperations.description())  # Output: This class provides basic math operations.
  print(MathOperations.square(4))  # Output: 16
  ```

#### **5. Building Custom Classes**
- **Question**: Design a `Student` class to model a university student. Include attributes for `name` and `grades` (a list of grades), and a method `average_grade` to calculate the average grade.  
  **Answer**:  
  ```python
  class Student:
      def __init__(self, name, grades):
          self.name = name
          self.grades = grades

      def average_grade(self):
          return sum(self.grades) / len(self.grades)

  student = Student("Alice", [90, 85, 88])
  print(student.name)  # Output: Alice
  print(student.average_grade())  # Output: 87.66666666666667
  ```

