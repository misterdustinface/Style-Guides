# Lua Style Guide

##### Index
0. [Clean Code](#clean-code)
1. [General Formatting](#general-formatting)
2. [Variable and Function Names](#variable-and-function-names)
3. [Constant Variables](#constant-variables)
4. [Local Variables and Parameters](#local-variables-and-parameters)
5. [The Conditional Expression](#the-conditional-expression)
6. [Error Handling](#error-handling)
7. [Functions](#functions)

##[Clean Code](#index)
  - All names should properly convey usage.
  - Keep function size small. Aim for 4 lines.
  - Keep files small. Aim for 50 lines.
  - Refactor often.
  - Comments should be a last resort.
  - Reads like well written prose.

##[General Formatting](#index)
  - Use 2 OR 4 space indents when programming in Lua.
  - DO NOT make banners or other "roadmap" indicators out of comments.

##[Variable and Function Names](#index)
  - Camel case.  Can mash two words together if the English language treats it as one word.
```Lua
  userName (OR) username
  someValue
  someLocalValue
```
  - Predicates should be named in the form of questions. 
```Lua
  plateStack:isEmpty()
  shouldQuitProgram()
  hasCompletedTask
```
  - Units are denoted with a postfix notation after two underscores.
```Lua
  elapsedTime__sec
  elapsedTime__ms
  displacement__cm
```

##[Constant Variables](#index)
  - Should be in all CAPS, with logical separations delimited by one underscore character.
```Lua
  TABLE_DELIMITER
  MAX_INPUT_SIZE
  MAX_TRAVEL_DISTANCE__cm
```

##[Local Variables and Parameters](#index)
  - Since your function size should be small, I think there should be some freedom allowed here.
  - Sometimes my parameters are named with all CAPS, because I typically treat them as constant variables.
  - If the parameters are part of some type of math function, their names can be one letter in length.
  - Local variable names can be one letter in length if the datatype is specific; otherwise, the name must be more  descriptive -> following the Variables guidelines.

##[The Conditional Expression](#index)
  - MUST NOT be nested.
  - MUST ONLY occupy one line.
```Lua
  -- BAD
  result = condition and trueResolution or falseResolution
  
  -- GOOD
  result = tif(condition, trueResolution, falseResolution)
```

##[Error Handling](#index)
  - ABSOLUTELY NO RETURN CODES.

##[Functions](#index)
  - Parameter restrictions
    1. NO BOOLEAN PARAMETERS
    2. Limit number of parameters to the range [0,2].  (Attempt to do so no matter the cost)
  
  - Fuckery
    1. DO NOT CHECK FOR NIL
    2. NO DEFAULT ARGUMENTS
  
  - Return restrictions
    1. ABSOLUTELY NO RETURN CODES.
    2. nil is a synonym for "No Value"; therefore, you may only return nil from a search function.
    3. Return at the end of the function, unless within a "simple loop".
    4. Only "predicate" functions can return a boolean value, but they must follow the predicate naming convention.  
  
