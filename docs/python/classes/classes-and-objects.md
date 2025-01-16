# Classes and Objects

When you’re just creating small scripts, chances are you don’t need to create your own Python classes. But once you
start creating larger applications, objects and classes allow you to organize your code naturally.

## Python objects

You probably know the built-in `len()` function. It simply returns the length of the object you give it. But what is the
length of, say, the number five? Let’s ask Python:

```shell 
>>> len(5)
```

```shell title="output:"
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: object of type 'int' has no len()
```

In this case, Python is telling us that `5` is an object, and it has no `len()`.  
In Python, everything is an object. Strings, booleans, numbers, and even Python functions are objects.

We can inspect an object in the REPL using the built-in function `dir()`. When we try `dir()` on the number `5`, it
reveals a
big list of functions that are part of any object of type `number`:

```shell
>>> dir(5)
```

```shell title="output:"
['__abs__', '__add__', 
'__and__', '__bool__', 
'__ceil__', '__class__', 
...
'__str__', '__sub__',
 '__subclasshook__', '__truediv__',
 '__trunc__', '__xor__', 
'bit_length', 'conjugate', 
'denominator', 'from_bytes',
 'imag', 'numerator', 
'real', 'to_bytes']
```

The list starts with these weirdly named functions containing underscores, like `__add__` .
These are called **_magic methods_**, or **_dunder methods_** (short for double underscore).

If you look closely, you’ll see that there’s no `__len__` dunder method for objects of type `int`. That’s how Python’s
`len()` function knows that a number does not have a length. All `len()` does, is call the `__len__()` method on the
object you offered it. That’s also why Python complained that _“objects of type ‘int’
have no len().”_

## What are Python Methods?

### Method

> When a function is part of an object or Python class, we call it a method.

A string must have a `len()` method:

```shell 
dir("test")
```

```shell title="output:"
['__add__', '__class__',
...
'__dir__', '__doc__', '__len__', 
... ]
```

And since this is a method, we can call it too:

```shell
"test".__len__()
```

```shell title="output:"
4
```

This is equivalent to `len("test")` but a lot less elegant, so don’t do this. It’s just to illustrate how this stuff
works.  
There’s also a list of other, less magical methods that `dir()` revealed to us. like `islower()` and `replace()`:

```shell
"test".islower()
```

## What is a Python object?

Now that we’ve used objects and know that everything in Python is an object, it’s time to define what an object is:

### Object

> An object is a collection of data (variables) and methods that operate on that data. Objects are defined by a Python
> class.

Objects and object-oriented programming are concepts that became popular in the early 1990s. It turned out that objects
are an easy-to-understand paradigm for humans. Objects can be used to model many real-life concepts and situations.

## What is a Python class?

Since objects are the building blocks of the Python language, it’s only logical that you can create objects yourself
too. If you want to create your own type of object, you first need to define its methods and what data it can hold. This
blueprint is called a class.

### Class

> A class is the blueprint for one or more objects

All Python objects are based on a class. When we create an object, we call this ‘creating an instance of a class’.
Strings, numbers, and even booleans are instances of a class too. Let’s explore with the built-in function `type()`:

```shell
>>> type('a')
<class 'str'>

>>> type(1)
<class 'int'>

>>> type(True)
<class 'bool'>
```

Apparently, there are classes called `str`, `int`, and `bool`. These are some of Python’s native classes.

## Creating a Python class

Let’s make a Python class that represents a car.

```python
class Car:
    speed = 0
    started = False

    def start(self):
        self.started = True
        print("Car started, let's ride!")

    def increase_speed(self, delta):
        if self.started:
            self.speed = self.speed + delta
            print('Vrooooom!')
        else:
            print("You need to start the car first")

    def stop(self):
        self.speed = 0
        print('Halting')
```

## Create a Python object

create and use a Python object of type Car:

```shell
>>> car = Car()
>>> car.increase_speed(10)
You need to start the car first

>>> car.start()
Car started, let's ride!

>>> car.increase_speed(40)
Vrooooom!
```

An object in Python is always an instance of a class. One class can have many instances. We just created an instance of
class `Car`, with `Car()`, and assigned it to the variable `car` . Creating an instance looks like calling a
function.

## What Is `self` in Python?

* When we call a method on a Python object, Python automatically fills in the first variable, which we call self by
  convention.
* This first variable is a reference to the object itself, hence its name.
* We can use this variable to reference other instance variables and functions of this object, like `self.speed` and
  `self.start()`

So only inside the Python class definition, we use `self` to reference variables that are part of the instance. To
modify
the `started` variable that’s part of our class, we use `self.started` and not just `started`. By using `self`, it’s
made abundantly clear that we are operating on a variable that’s part of this instance and not some other variable that
is defined outside the object and happens to have the same name.

## Creating Multiple Python Objects

A Python class is just a blueprint, you can use it to create multiple objects, just like you can build multiple
identical-looking cars. They all behave similarly, but they all have their own data that is not shared between objects:

```shell
>>> car1 = Car()
>>> car2 = Car()
>>> id(car1)
139771129539104

>>> id(car2)
139771129539160
```

Each object in Python has a unique identifier, and used the built-in method `id()` to get their ids.

---
source: [Python Land](https://python.land/objects-and-classes)