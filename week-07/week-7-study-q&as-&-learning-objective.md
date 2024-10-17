### Learning Objectives for the Week:

1. Students will be able to explain the core principles of Object-Oriented Programming (OOP) relating to the use of classes and objects in Python.
2. Students will be able to define and implement Python classes, distinguishing between instance attributes and class attributes.
3. Students will be able to demonstrate encapsulation by using getter and setter methods to control access to class attributes.
4. Students will be able to implement methods in Python classes, understanding the role of `self` and applying it to access instance-specific data.
5. Students will be able differentiate between an instance method and a class method in Python.
6. Students will be able to design and pseudocode their projects at some level prior to coding

### Questions to Assess Learning Objectives:

1. **What is the difference between a class and an object in Python?**
   - **Answer**: A class is a blueprint for creating objects. An object is an instance of a class, meaning it’s created from that class blueprint and can have attributes and behaviors defined by the class.

2. **How do instance attributes differ from class attributes in Python? Provide an example.**
   - **Answer**: Instance attributes are specific to each object created from the class, while class attributes are shared across all instances of the class. For example:
     ```python
     class Dog:
         species = 'Canine'  # Class attribute
         def __init__(self, name):
             self.name = name  # Instance attribute
     dog1 = Dog('Buddy')
     dog2 = Dog('Max')
     ```
     Here, `species` is shared by both `dog1` and `dog2`, but each has its own `name`.

3. **Why is `self` used in Python class methods, and how is it different from other method parameters?**
   - **Answer**: `self` is a reference to the current instance of the class and is used to access instance attributes and methods. Unlike other parameters, `self` is automatically passed by Python when an instance calls a method.

4. **How can you control access to an attribute in Python using encapsulation? Provide an example using getter and setter methods.**
   - **Answer**:
     ```python
     class Student:
         def __init__(self, name, age):
             self.__age = age  # Private attribute
         
         def get_age(self):
             return self.__age
         
         def set_age(self, age):
             if age > 0:
                 self.__age = age
     ```
     Here, `__age` is a private attribute, and `get_age()` and `set_age()` control access to it.


5. **Explain the difference between an instance method and a class method in Python. Provide an example of each.**
   - **Answer**:
     - **Instance Method**: Operates on an instance of the class. It requires `self`.
       ```python
       def instance_method(self):
           print(self.name)
       ```
     - **Class Method**: Operates on the class itself. It requires `cls`.
       ```python
       @classmethod
       def class_method(cls):
           print(cls.species)
       ```