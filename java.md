# Java

0. [Clean Code](#cleancode)
1. [General Formatting](#formatting)
2. [Restricted Keyword Usage](#restricted keyword usage)
3. [Variables](#variables)
4. [Constant Variables](#constant variables)
5. [Local Variables and Parameters](#local variables and parameters)
6. [Enumerated Types](#enumerated types)
7. [Conditional Statements and Loops](#conditional statements and loops)
8. [The Conditional Expression](#conditional expression)
9. [Functions](#functions)
10. [Classes](#classes)
11. [Interfaces](#interfaces)
12. [Singletons](#singletons)
13. [High Level Software Design Guidelines](#software design)

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

# Restricted Keyword Usage
  - continue: should not appear
  - do: should refrain from using
  - instanceof: should only use as a private implementation detail
  - switch, case: should only use as a private implementation detail

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

# Conditional Statements and Loops
  - Many accepted formats. Use "Clean Code" judgement. When in doubt use { braces }.
  - Avoid do-while loops.
  - Loops should follow the Initialize - Check - Change pattern.
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
```Java
  for (int i = 0; i < 10; i++) {
      output(i);
  }
```
```Java
  for (int i = 0; i < 10; i++)
      output(i);
```
```Java
  for (Shape s : shapes) {
      draw(s);
  }
```
```Java
  for (Shape s : shapes) 
      draw(s);
```
```Java
  for (Shape s : shapes) {
      if (s.contains(x,y)) {
          recordCollision(x,y);
      }
  }
```
```Java
  for (Shape s : shapes)
      if (s.contains(x,y))
          recordCollision(x,y);
```
```Java
  while (shouldHurtFeels()) {
      hurtFeels();
  }
```
```Java
  while (shouldHurtFeels())
      hurtFeels();
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
