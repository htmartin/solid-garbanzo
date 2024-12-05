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
  **Answer**:  
  ```python
  class Animal:
      def speak(self):
          print("Animal speaks")

  class Dog(Animal):
      def speak(self):
          print("Woof!")

  animal = Animal()
  animal.speak()  # Output: Animal speaks

  dog = Dog()
  dog.speak()  # Output: Woof!
  ```

- **Question**: How does method overriding support polymorphism?  
  **Answer**: Method overriding allows subclasses to provide specific implementations of methods from the parent class. Polymorphism ensures that the method call behaves appropriately for the actual object type, allowing flexible and interchangeable code.

---

#### **2. Polymorphism and Duck Typing**
- **Question**: Demonstrate polymorphism by defining a `Shape` class with a `draw()` method and subclasses `Circle` and `Square` that implement `draw()` differently.  
  **Answer**:  
  ```python
  class Shape:
      def draw(self):
          raise NotImplementedError("Subclasses must implement this method")

  class Circle(Shape):
      def draw(self):
          print("Drawing a circle")

  class Square(Shape):
      def draw(self):
          print("Drawing a square")

  shapes = [Circle(), Square()]
  for shape in shapes:
      shape.draw()
  # Output:
  # Drawing a circle
  # Drawing a square
  ```

- **Question**: What is duck typing in Python? Provide an example.  
  **Answer**:  
  Duck typing allows Python to use objects as long as they have the required methods, regardless of their type.  
  ```python
  class Duck:
      def quack(self):
          print("Quack!")

  class Person:
      def quack(self):
          print("I can quack like a duck!")

  def make_quack(obj):
      obj.quack()

  duck = Duck()
  person = Person()

  make_quack(duck)    # Output: Quack!
  make_quack(person)  # Output: I can quack like a duck!
  ```

---

#### **3. Magic Methods**
- **Question**: Define a class `Point` that supports equality comparison using the `__eq__` magic method.  
  **Answer**:  
  ```python
  class Point:
      def __init__(self, x, y):
          self.x = x
          self.y = y

      def __eq__(self, other):
          return self.x == other.x and self.y == other.y

  p1 = Point(1, 2)
  p2 = Point(1, 2)
  p3 = Point(2, 3)

  print(p1 == p2)  # Output: True
  print(p1 == p3)  # Output: False
  ```

- **Question**: Why would you override the `__str__` method? Provide an example.  
  **Answer**: Overriding `__str__` makes the string representation of an object more informative and user-friendly.  
  ```python
  class Point:
      def __init__(self, x, y):
          self.x = x
          self.y = y

      def __str__(self):
          return f"Point({self.x}, {self.y})"

  p = Point(1, 2)
  print(p)  # Output: Point(1, 2)
  ```

---

#### **4. Composition and Aggregation**
- **Question**: Create a `Car` class that uses composition to include an `Engine` class as an attribute.  
  **Answer**:  
  ```python
  class Engine:
      def start(self):
          print("Engine starts")

  class Car:
      def __init__(self):
          self.engine = Engine()

      def drive(self):
          self.engine.start()
          print("Car drives")

  car = Car()
  car.drive()
  # Output:
  # Engine starts
  # Car drives
  ```

---

#### **5. Dataclasses and Named Tuples**
- **Question**: Use a dataclass to define a `Student` class with attributes `name` and `grades` (list of grades). Include a method to calculate the average grade.  
  **Answer**:  
  ```python
  from dataclasses import dataclass
  from typing import List

  @dataclass
  class Student:
      name: str
      grades: List[int]

      def average_grade(self):
          return sum(self.grades) / len(self.grades)

  student = Student("Alice", [90, 85, 88])
  print(student.name)  # Output: Alice
  print(student.average_grade())  # Output: 87.66666666666667
  ```

These objectives and questions cover core OOP principles and encourage practical application, preparing students for complex data science programming challenges.