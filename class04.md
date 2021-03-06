# Classes and Objects
* Objects get their variables and functions from classes.
* Classes are essentially a template to create your objects.

* Accessing Object Variables
```
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

myobjectx = MyClass()

myobjectx.variable
```
* Accessing Object Functions
```
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

myobjectx = MyClass()

myobjectx.function()
```

# Thinking Recursively in Python : Naive Recursion is Naive
Thus, we avoid recomputation by explicitly checking for the value before trying to compute it. One thing to keep in mind about lru_cache is that since it uses a dictionary to cache results, the positional and keyword arguments (which serve as keys in that dictionary) to the function must be hashable.

##  Pesky Details
- Python doesn’t have support for tail-call elimination. 
- Also, Python’s mutable data structures don’t support structural sharing, so treating them like immutable data structures is going to negatively affect your space and GC (garbage collection) efficiency because you are going to end up unnecessarily copying a lot of mutable objects. 

>Recursively doing that over large lists can negatively affect your space and GC efficiency.