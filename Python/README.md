# Python

## 1. Introduction

**In this course I have learned:**

- How to adopt general coding techniques and best practices in your projects;
- How to process strings;
- How to use object-oriented programming in Python;
- How to import and use Python modules, including the math, random, platform, os, time, datetime, and calendar modules;
- How to create and use your own Python modules and packages;
- How to use the exception mechanism in Python;
- How to use generators, iterators, and closures in Python;
- How to process files.
*The course is divided into four modules:*
- Module 1
    Modules, Packages and PIP;
- Module 2
    Strings, string and list methods, and exceptions;
- Module 3
    Object-Oriented Programming;
- Module 4
    Miscellaneous (generators, iterators, closures, file streams, processing text and binary files, the os, time, datetime, and calendar module).

## 2. Modules in python  

- Computer code has a tendency to grow. We can say that code that doesn't grow is probably completely unusable or abandoned. A real, wanted, and widely used code develops continuously, as both users' demands and users' expectations develop in their own rhythms.

### Importing a module

- To make a module usable, you must import it (think of it like of taking a book off the shelf). Importing a module is done by an instruction named import. Note: import is also a keyword (with all the consequences of this fact).
    ```
    import module
    ```
- **Namespace**
- **Importing Modules Continued**
- **Aliasing**
- **Selected python modeule**

## 3. Modules and Packages

- a module is a kind of container filled with functions - you can pack as many functions as you want into one module and distribute it across the world
![Diagram](<Images/ada86cb502a94eccb75497b1c0c31208.png>)

### Creating own modules
**Folder structure**
![Folder](<Images/4fd776a35a09444594fcdf201c99df89.png>)
- [Download the modules ](packages)for the practice.

1. While a module is designed to couple together some related entities such as functions, variables, or constants, a package is a container which enables the coupling of several related modules under one common name. Such a container can be distributed as-is (as a batch of files deployed in a directory sub-tree) or it can be packed inside a zip file.
2. During the very first import of the actual module, Python translates its source code into a semi-compiled format stored inside the pyc files, and deploys these files into the __pycache__ directory located in the module's home directory.
3. If you want to tell your module's user that a particular entity should be treated as private (i.e. not to be explicitly used outside the module) you can mark its name with either the _ or __ prefix. Don't forget that this is only a recommendation, not an order.
4. The names shabang, shebang, hasbang, poundbang, and hashpling describe the digraph written as #!, used to instruct Unix-like OSs how the Python source file should be launched. This convention has no effect under MS Windows.
5. If you want convince Python that it should take into account a non-standard package's directory, its name needs to be inserted/appended into/to the import directory list stored in the path variable contained in the sys module.
6. A Python file named __init__.py is implicitly run when a package containing it is subject to import, and is used to initialize a package and/or its sub-packages (if any). The file may be empty, but must not be absent.

## 4. PIP in Python

- The PyPI repo is sometimes referred to as the Cheese Shop. Really.
- We refer to the repo as a shop, because you go there for the same reasons you go to other shops: to fulfill your needs. If you want some cheese, you go to the cheese shop. If you want a piece of software, you go to the software shop. Fortunately, the analogy ends here – you don't need any money to take some software out of the repo shop.
- It also requires a special tool to make use of it. Fortunately, this tool is also free, so if you want to make your own digital cheeseburger by using the goods offered by the PyPI Shop, you’ll need a free tool named pip.
**Check the version of pip because in not pirated windowsthe pip is pre-installed.**
```
pip --version
```
**Gives you complete Help guide to use it.**
```
pip help
```
**Install pygame**
```
pip install pygame
pip install --user pygame
```

## 5. Strings, String & List methods
![ASCII Table](<Images/Screenshot 2026-08-27 102620.png>)
- **Multiline string**
- **Operation on strings**
- **Slices**
- **in operator**
- **not in operator**
- **min()**
- **max()**
- **index()**
- **list()**
- **count()**
- **Indexing**
- **len()**
- **center()**
- **endswith()**
- **find()**
- **isalnum()**
- **isalpha()**
- **isdigit()**
- **islower()**
- **isspace()**
- **isupper()**
- **join()**
- **lower()**
- **lstrip()**
- **replace()**
- **rfind()**
- **rstrip()**
- **split()**
- **startswith()**
- **strip()**
- **swapcase()**
- **title()**
- **upper()**
