# JavaScript vs Python
This is a side-by-side comparison of JavaScript (ES2015) and Python (3.6) syntax.

Ctrl + F is your friend.

## Contents

[Basics](https://github.com/KelliePetersen/javascript-python-comparison#Basics)  
[Classes](https://github.com/KelliePetersen/javascript-python-comparison#Classes)

## Basics

| Description | JavaScript | Python |
| --- | --- | --- |
| Shebang |
| Single-line Comment | `// I am a comment` | `# I am a comment` |
| Multi-line Comment| `/* I am a multi-line comment \*/` | `""" I am a multi-line comment """` |
| Defining variables | `var/const/let myVariable = "I am a variable";` | `myVariable = "I am a variable"` | 
| Printing lines | console.log("Hello world"); | print("Hello world") |
| Variables inside strings (old) | "Hello, I feel " + mood | "Hello, I feel {}".format(mood) |
| Variables inside strings (new) | \`Hello, I feel ${mood}\` | f"Hello, I feel {mood}" |
| Swap values of variables | [a, b] = [b, a] | a, b = b, a |
| Find string inside a string | `"Hello".indexOf("ell");` returns 1 | `"Hello".find("ell")` returns 1 |
| Find string from a starting index | `"Kellie". indexOf("e", 3)` returns 5 | `"Kellie".find("ell", 3)` returns 5 |
