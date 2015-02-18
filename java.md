# Java

0. [Clean Code](#cleancode)
1. [Variables](#variables)
2. [Constant Variables](#constant variables)
3. [Local Variables and Parameters](#local variables and parameters)
4. [Conditional Statements](#conditional statements)
5. [Functions](#functions)
6. [Classes](#classes)
7. [Interfaces](#interfaces)
8. [Singletons](#singletons)
9. [High Level Software Design Guidelines](#software design)

# Clean Code
  - All names should properly convey usage.
  - Keep function size small. Aim for 4 lines.
  - Keep classes small. Aim for 50 lines.
  - Comments should be a last resort.
  - Reads like well written prose.

# Variables
  - Camel case.  Can mash two words together if the English language treats it as one word.
```Java
  userName (OR) username
  someValue
  someLocalValue
```
  - Predicates should be named in the form of questions. 
```Java
  plateStack.isEmpty()
  shouldQuitProgram()
  boolean hasCompletedTask
```
  - Units are denoted with a postfix notation after two underscores.
```Java
  elapsedTime__sec
  elapsedTime__ms
  displacement__cm
```

# Constant Variables
  - Should use the final keyword.
```Java 
  final 
```
  - Should be in all CAPS, with logical separations delimited by the underscore (_).
```Java
  TABLE_DELIMITER
  MAX_INPUT_SIZE
  MAX_TRAVEL_DISTANCE__cm
```

# Local Variables and Parameters
  - Since your function size should be small, I think there should be some freedom allowed here.
  - Sometimes my parameters are named with all CAPS, because I typically treat them as constant variables, you should use the final keyword when doing so.
  - If the parameters are part of some type of math function, their names can be one letter in length.
  - Local variable names can be one letter in length if the datatype is specific; otherwise, the name must be more  descriptive -> following the Variables guidelines.

# Conditional Statements
```Java
  if (isEmpty()) {
    // perform action or actions;
  }
```
```Java
  if (isEmpty()) 
    // perform simple action;
```
```Java
  if (isEmpty()) // perform simple action;
```
```Java
  if (isEmpty()) {
    // perform action or actions;
  } else {
    // perform action or actions;
  }
```

# Functions

# Classes

# Interfaces

# Singletons

# High Level Software Design Guidelines
