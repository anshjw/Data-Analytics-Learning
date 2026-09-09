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
- A code which is not able to respond to users' needs will be forgotten quickly, and instantly replaced with a new, better, and more flexible code. Be prepared for this, and never think that any of your programs is eventually completed. The completion is a transition state and usually passes quickly, after the first bug report. Python itself is a good example how the rule acts.
- Growing code is in fact a growing problem. A larger code always means tougher maintenance. Searching for bugs is always easier where the code is smaller (just as finding a mechanical breakage is simpler when the machinery is simpler and smaller).
- Moreover, when the code being created is expected to be really big (you can use a total number of source lines as a useful, but not very accurate, measure of a code's size) you may want (or rather, you will be forced) to divide it into many parts, implemented in parallel by a few, a dozen, several dozen, or even several hundred individual developers.
- Of course, this cannot be done using one large source file, which is edited by all programmers at the same time. This will surely lead to a spectacular disaster.

### Importing a module

- To make a module usable, you must import it (think of it like of taking a book off the shelf). Importing a module is done by an instruction named import. Note: import is also a keyword (with all the consequences of this fact).

- Let's assume that you want to use two entities provided by the math module:

    - a symbol (constant) representing a precise (as precise as possible using double floating-point arithmetic) value of π (although using a Greek letter to name a variable is fully possible in Python, the symbol is named pi - it's a more convenient solution, especially for that part of the world which neither has nor is going to use a Greek keyboard)
    - a function named sin() (the computer equivalent of the mathematical sine function)
    ```
    import module
    ```
    ```
    import math
    import sys
    import math, sys
    ```

- **Namespace**
- **Importing Modules Continued**
- **Aliasing**
- **Selected python modeule**

## 3. Modules and Packages

- a module is a kind of container filled with functions - you can pack as many functions as you want into one module and distribute it across the world
- of course, it's generally a good idea not to mix functions with different application areas within one module (just like in a library - nobody expects scientific works to be put among comic books), so group your functions carefully and name the module containing them in a clear and intuitive way 
- e.g., don't give the name arcade_games to a module containing functions intended to partition and format hard disks
![Diagram](Images\ada86cb502a94eccb75497b1c0c31208.png)

## Creating own modules
**Folder structure**
![Folder](Images\4fd776a35a09444594fcdf201c99df89.png)
- [Download the modules ](packages)for the practice.

1. While a module is designed to couple together some related entities such as functions, variables, or constants, a package is a container which enables the coupling of several related modules under one common name. Such a container can be distributed as-is (as a batch of files deployed in a directory sub-tree) or it can be packed inside a zip file.
2. During the very first import of the actual module, Python translates its source code into a semi-compiled format stored inside the pyc files, and deploys these files into the __pycache__ directory located in the module's home directory.
3. If you want to tell your module's user that a particular entity should be treated as private (i.e. not to be explicitly used outside the module) you can mark its name with either the _ or __ prefix. Don't forget that this is only a recommendation, not an order.
4. The names shabang, shebang, hasbang, poundbang, and hashpling describe the digraph written as #!, used to instruct Unix-like OSs how the Python source file should be launched. This convention has no effect under MS Windows.
5. If you want convince Python that it should take into account a non-standard package's directory, its name needs to be inserted/appended into/to the import directory list stored in the path variable contained in the sys module.
6. A Python file named __init__.py is implicitly run when a package containing it is subject to import, and is used to initialize a package and/or its sub-packages (if any). The file may be empty, but must not be absent.

## 4. PIP in Python

- The PyPI repo is sometimes referred to as the Cheese Shop. Really.
- Does that sound a little strange to you? Don't worry, it’s all perfectly innocent.
- We refer to the repo as a shop, because you go there for the same reasons you go to other shops: to fulfill your needs. If you want some cheese, you go to the cheese shop. If you want a piece of software, you go to the software shop. Fortunately, the analogy ends here – you don't need any money to take some software out of the repo shop.
- PyPI is completely free, and you can just pick a code and use it – you’ll encounter neither cashier nor security guard. Of course, it doesn't absolve you from being polite and honest. You have to obey all the licensing terms, so don't forget to read them.
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
**Simple test program**
```
import pygame

run = True
width = 400
height = 100
pygame.init()
screen = pygame.display.set_mode((width, height))
font = pygame.font.SysFont(None, 48)
text = font.render("Welcome to pygame", True, (255, 255, 255))
screen.blit(text, ((width - text.get_width()) // 2, (height - text.get_height()) // 2))
pygame.display.flip()
while run:
  for event in pygame.event.get():
   if event.type == pygame.QUIT\
   or event.type == pygame.MOUSEBUTTONUP\
   or event.type == pygame.KEYUP:
    run = False
```

## 5. Strings, String & List methods
![ASCII Table](<Images/Screenshot 2026-08-27 102620.png>)
- **Multiline string**
```
multiline = '''Line #1
Line #2'''

print(len(multiline))
```
- **Operation on strings**
```
str1 = 'a'
str2 = 'b'

print(str1 + str2)
print(str2 + str1)
print(5 * 'a')
print('b' * 4)
```
- **Indexing**
- **Slices**
```
# Slices

alpha = "abdefg"

print(alpha[1:3])
print(alpha[3:])
print(alpha[:3])
print(alpha[3:-2])
print(alpha[-3:4])
print(alpha[::2])
print(alpha[1::2])
```
- **in operator**
- **not in operator**
- **min()**
- **max()**
- **index()**
- **list()**
- **count()**
