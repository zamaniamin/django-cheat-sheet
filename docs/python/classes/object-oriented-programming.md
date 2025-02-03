# Object-Oriented Programming (OOP)

Object-oriented programming (OOP) in Python helps you structure your code by grouping related data and behaviors into
objects. You start by defining classes, which act as blueprints, and then create objects from them. OOP simplifies
modeling real-world concepts in your programs and enables you to build robust systems in Python that are more reusable
and scalable.

The four key concepts of OOP in Python are **encapsulation**, **inheritance**, **abstraction**, and **polymorphism**.

## What Is Object-Oriented Programming in Python?

Object-oriented programming is a programming paradigm that provides a means of structuring programs so that properties
and behaviors are bundled into individual objects.

OOP models real-world entities as software objects that have some data associated with them and can perform certain
operations.

The four key concepts of OOP in Python:

1. **Encapsulation** allows you to bundle data (attributes) and behaviors (methods) within a class to create a cohesive
   unit.
   By defining methods to control access to attributes and its modification, encapsulation helps maintain data integrity
   and promotes modular, secure code.
2. **Inheritance** enables the creation of hierarchical relationships between classes, allowing a subclass to inherit
   attributes and methods from a parent class. This promotes code reuse and reduces duplication.
3. **Abstraction** focuses on hiding implementation details and exposing only the essential functionality of an object.
   By
   enforcing a consistent interface, abstraction simplifies interactions with objects, allowing developers to focus on
   what an object does rather than how it achieves its functionality.
4. **Polymorphism** allows you to treat objects of different types as instances of the same base type, as long as they
   implement a common interface or behavior. Python’s [duck typing](https://realpython.com/duck-typing-python/) make it
   especially suited for polymorphism, as it allows you to access attributes and methods on objects without needing to
   worry about their actual class.

## Why You Define a Class in Python?

But what does all of that mean? And why do you even need classes in the first place? Take a step back and consider using
built-in, primitive data structures as an alternative.

For example, you might want to track employees in an organization. You need to store some basic information about each
employee, such as their name, age, position, and the year they started working.

One way to do this is to represent each employee as a `list`:

```python
kirk = ["James Kirk", 34, "Captain", 2265]
spock = ["Spock", 35, "Science Officer", 2254]
mccoy = ["Leonard McCoy", "Chief Medical Officer", 2266]
```

There are a number of issues with this approach.
First, it can make larger code files more difficult to manage. If you reference `kirk[0]` several lines away from where
you declared the `kirk` list, will you remember that the element with index `0` is the employee’s name?  
Second, it can introduce errors if employees don’t have the same number of elements in their respective lists. In the
`mccoy` list above, the age is missing, so `mccoy[1]` will return "Chief Medical Officer" instead of Dr. McCoy’s age.

A great way to make this type of code more manageable and more maintainable is to use **classes**.

```python
class Employee:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

## Classes vs Instances

Classes allow you to create user-defined data structures. Classes define functions called `methods`, which identify the
behaviors and actions that an object created from the class can perform with its data.

In this tutorial, you’ll create a Dog class that stores some information about the characteristics and behaviors that an
individual dog can have.

A class is a blueprint for how to define something. It doesn’t actually contain any data. The Dog class specifies that a
name and an age are necessary for defining a dog, but it doesn’t contain the name or age of any specific dog.

While the class is the blueprint, an instance is an object that’s built from a class and contains real data. An instance
of the Dog class is not a blueprint anymore. It’s an actual dog with a name, like Miles, who’s four years old.

Put another way, a class is like a form or questionnaire. An **instance** is like a form that you’ve filled out with
information. Just like many people can fill out the same form with their own unique information, you can create many
instances from a single class.

---
source: [Real Python](https://realpython.com/python3-object-oriented-programming/)