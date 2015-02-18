# Java

0. [Clean Code](#clean-code)
1. [General Formatting](#general-formatting)
2. [Restricted Keyword Usage](#restricted-keyword-usage)
3. [Variable and Function Names](#variable-and-function-names)
4. [Constant Variables](#constant-variables)
5. [Local Variables and Parameters](#local-variables-and-parameters)
6. [Enumerated Types](#enumerated-types)
7. [Conditional Statements and Loops](#conditional-statements-and-loops)
8. [The Conditional Expression](#the-conditional-expression)
9. [Error Handling](#error-handling)
10. [Functions](#functions)
11. [Classes](#classes)
12. [Interfaces](#interfaces)
13. [Singletons](#singletons)
14. [High Level Software Design Guidelines](#high-level-software-design-guidelines)

# Clean Code
  - All names should properly convey usage.
  - Keep function size small. Aim for 4 lines.
  - Keep classes small. Aim for 50 lines.
  - Refactor often.
  - Comments should be a last resort.
  - Reads like well written prose.

# General Formatting
  - Use 4-space indents when programming in Java.
  - Conditional Statements and Loops should have a space between keywords, parenthesis, and curly braces.
  - DO NOT make banners or other "roadmap" indicators out of comments.

# Restricted Keyword Usage
  - continue: Should NEVER appear.
  - do: Should refrain from using.  A while loop can typically increase readability.
  - instanceof: Should only use as a private implementation detail.  Can typically be replaced via polymorphism.
  - switch, case: Should only use as a private implementation detail.  Can typically be replaced via polymorphism.
  - null: It is not a keyword, but it is often treated as one.  It should be used as a synonym for "No Value".

# Variable and Function Names
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
  - Should be in all CAPS, with logical separations delimited by one underscore character.
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

# Error Handling
  - ABSOLUTELY NO RETURN CODES.
  - Create descriptive exceptions that extend runtime exception.
  - Throw your custom, descriptive runtime exception.

# Functions
  - Parameter restrictions
    1. NO BOOLEAN PARAMETERS
    2. Limit number of parameters to the range [0,2].  (Attempt to do so no matter the cost)
  
  - Fuckery
    1. DO NOT CHECK FOR NULL
  
  - Return restrictions
    1. ABSOLUTELY NO RETURN CODES.
    2. null is a synonym for "No Value"; therefore, you may only return null from a search function.
    3. Return at the end of the function, unless within a "simple loop".
    4. Only "predicate" functions can return a boolean value, but they must follow the predicate naming convention. 

# Classes
  - Initialize member variables within the constructor.
  - Prefer composition over inheritance.
  - Utilize encapsulation.

# Interfaces
  - Do not name with a prefix notation.
  - An interface is an API, so keep the method names short and to-the-point.

# Singletons
  - Designed as a Java class.
  - The "getter" function(s) must be declared static.
  - The singleton object should be an instantiated private static data member of the class.
  - All class constructors must be private.

# High Level Software Design Guidelines
  - Dependencies should be representable by Directed Asynchronous Graphs; resolve all dependencies that do not conform to this standard.
  - Decouple packages/projects from each other.
  - Invert dependencies with interfaces.
  - Utilize design patterns, but only when they improve readability.
