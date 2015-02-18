# Lua Style Guide

##### Index
0. [Clean Code](#clean-code)
1. [General Formatting](#general-formatting)
2. [Variable and Function Names](#variable-and-function-names)

#[Clean Code](#index)
  - All names should properly convey usage.
  - Keep function size small. Aim for 4 lines.
  - Keep files small. Aim for 50 lines.
  - Refactor often.
  - Comments should be a last resort.
  - Reads like well written prose.

#[General Formatting](#index)
  - Use 2 OR 4 space indents when programming in Lua.
  - DO NOT make banners or other "roadmap" indicators out of comments.

#[Variable and Function Names](#index)
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
