# Python Modules and Packages

Python modules and Python packages, are  two mechanisms that facilitate modular programming.
**Modular programming** refers to the process of breaking a large, unwieldy programming task into separate, smaller, more manageable subtasks or modules

There are several advantages to modularizing code in a large application:
* Maintainability: Modules are typically designed so that they enforce logical boundaries between different problem domains
* Reusability: Functionality defined in a single module can be easily reused (through an appropriately defined interface) by other parts of the application
* Scoping: Modules typically define a separate namespace, which helps avoid collisions between identifiers in different areas of a program.

## Python Modules: Overview

There are actually three different ways to define a module in Python:

1. A module can be written in Python itself.
2. A module can be written in C and loaded dynamically at run-time, like the re (regular expression) module.
3. A built-in module is intrinsically contained in the interpreter, like the itertools module.

# The import Statement
Module contents are made available to the caller with the import statement. The import statement takes many different forms, shown below.

import <module_name>
The simplest form is :
```
>>> import mod
>>> mod.__file__
'C:\\Users\\john\\mod.py'

>>> import re
>>> re.__file__
'C:\\Python36\\lib\\re.py'
```

> import <module_name>

## The dir() Function
The built-in function dir() returns a list of defined names in a namespace. Without arguments, it produces an alphabetically sorted list of names in the current local symbol table:
```
>>> dir()
['__annotations__', '__builtins__', '__doc__', '__loader__', '__name__',
'__package__', '__spec__']

>>> qux = [1, 2, 3, 4, 5]
>>> dir()
['__annotations__', '__builtins__', '__doc__', '__loader__', '__name__',
'__package__', '__spec__', 'qux']

>>> class Bar():
...     pass
...
>>> x = Bar()
>>> dir()
['Bar', '__annotations__', '__builtins__', '__doc__', '__loader__', '__name__',
'__package__', '__spec__', 'qux', 'x']
```

