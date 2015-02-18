# Java

0. [Clean Code](#cleancode)
1. [General Formatting](#formatting)
2. [Variables](#variables)
3. [Constant Variables](#constant variables)
4. [Local Variables and Parameters](#local variables and parameters)
5. [Enumerated Types](#enumerated types)
6. [Conditional Statements](#conditional statements)
7. [The Conditional Expression](#conditional expression)
8. [Functions](#functions)
9. [Classes](#classes)
10. [Interfaces](#interfaces)
11. [Singletons](#singletons)
12. [High Level Software Design Guidelines](#software design)

# Clean Code
  - All names should properly convey usage.
  - Keep function size small. Aim for 4 lines.
  - Keep classes small. Aim for 50 lines.
  - Comments should be a last resort.
  - Reads like well written prose.

# General Formatting
  - Use 4-space indents when programming in Java.
  - Conditional Statements and Loops should have a space between keywords, parenthesis, and curly braces.
  - DO NOT make banners or other "roadmap" indicators out of comments.

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

# Enumerated Types
  - Typename should be in all CAPS.
  - Defined type values should be in all CAPS.
  - Usage should be a private implementation detail.

# Conditional Statements
  - Many accepted formats. Use "Clean Code" judgement. When in doubt use { braces }.
```Java
  if (shouldAcceptRequest()) {
    performAction();
  }
```
```Java
  if (shouldAcceptRequest()) 
    performAction();
```
```Java
  if (shouldAcceptRequest()) performAction();
```
```Java
  if (shouldAcceptRequest()) {
    performAction();
  } else {
    logUnacceptedRequest();
  }
```

# The Conditional Expression
  - MUST NOT be nested.
  - MUST ONLY occupy one line.
  - MUST have the following format (the "resolutions" can be function calls).
```Java
  result = condition ? trueResolution : falseResolution;
```

# Functions

# Classes

# Interfaces

# Singletons

# High Level Software Design Guidelines
