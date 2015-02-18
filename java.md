# Java

0. [Clean Code](#cleancode)
1. [Variables](#variables)
2. [Constants](#constants)
3. [Statements](#statements)
4. [Functions](#functions)
5. [Classes](#classes)
6. [Interfaces](#interfaces)
7. [Singletons](#singletons)

# Clean Code
  - All names should properly convey usage.
  - Keep function size small. Aim for 4 lines.
  - Keep classes small. Aim for 50 lines.
  - Comments should be a last resort.

# Variables
  - Camel case.  Can mash two words together if the English language treats it as one word.
```Java
  userName (OR) username;
  someValue;
  someLocalValue;
```
  - Predicates should be named in the form of questions. 
```Java
  plateStack.isEmpty()
  shouldQuitProgram()
  boolean hasCompletedTask;
```
  - Units are denoted with a postfix notation after two underscores.
```Java
  elapsedTime__sec
  elapsedTime__ms
  displacement__cm
```

# Constants

# Statements
```Java
  if (isEmpty()) {
    //
  }
```

# Functions

# Classes

# Interfaces

# Singletons
