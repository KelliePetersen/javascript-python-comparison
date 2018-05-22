# JavaScript vs Python
This is a side-by-side comparison of JavaScript (ES2015) and Python (3.6) syntax.  
Searching for something specific? Use ctrl + f (or cmd + f)

## Contents

[Important Notes](#important-notes)  
[Similarities](#similarities)  
[Basics](#basics)  
[Functions](#functions)  
[Loops](#loops)  
[Classes](#classes)  

## Important Notes

JavaScript uses brackets { } to create blocks. Python uses indentation instead of brackets. This means that expressions inside statements (such as a loop or class) must be on a new line and indented. Look at [Functions](#functions) or [Loops](#loops) sections for examples.

## Similarities

| Description | JavaScript | Python |
| --- | --- | --- |
| Creating an array/list | var array = [1,2,3] | list = [1,2,3] |
| Select an index inside a array/list/string | array[2] | list[2] |
| Get an array/list backwards | array.reverse() | list.reverse() or list[::-1] |

## Basics

| Description | JavaScript | Python |
| --- | --- | --- |
| Shebang |
| Single-line Comment | `// I am a comment` | `# I am a comment` |
| Multi-line Comment| `/* I am a multi-line comment \*/` | `""" I am a multi-line comment """` |
| Defining variables | `var/const/let myVariable = "I am a variable";` | `myVariable = "I am a variable"` | 
| Printing lines | `console.log("Hello world");` | `print("Hello world")` |
| Variables inside strings (old) | `"Hello, I feel " + mood` | `"Hello, I feel {}".format(mood)` |
| Variables inside strings (new) | \`Hello, I feel ${mood}\` | `f"Hello, I feel {mood}"` |
| Swap values of variables | `[a, b] = [b, a];` | `a, b = b, a` |
| Find string/array length | `string.length();` | `len(string)` |
| Find string inside a string | `"Hello".indexOf("ell");` returns 1 | `"Hello".find("ell")` returns 1 |
| Find string from a starting index | `"Kellie". indexOf("e", 3)` returns 5 | `"Kellie".find("ell", 3)` returns 5 |
| Capitalize string | string[0].toUpperCase(); | string.capitalize() |
| Upper case string | string.toUpperCase(); | string.upper() |
| Lower case string | string.toLowerCase(); | string.lower() |
| User input prompt | let x = prompt("What is your name?") | x = input("What is your name?") |
| Get the last element of an array/list | array[array.length-1]| list[-1] |
| Copying a portion of an array/list | array.slice(start, end) | list[start:end] |

## Functions

Creating a function or defining procedures

| JavaScript | Python |
| --- | --- |
| `let myFunction = function() {` <br> &nbsp; &nbsp; `console.log("Hello world!");` <br> `}` | `def name():` <br> &nbsp; &nbsp; `print("Hello world!")` |
| `function myFunction() {` <br> &nbsp; &nbsp; `console.log("Hello world!");` <br> `}` |

## Loops

**While Loop**

| JavaScript | Python |
| --- | --- |
| `while (i < 10) {` <br> &nbsp; &nbsp; `// do a thing` <br> `}` | `while i < 10:` <br> &nbsp; &nbsp; `# do a thing` |

**if/else**

| JavaScript | Python |
| --- | --- |
| `if (i < 10) {` <br> &nbsp; &nbsp; `// do a thing;` <br> `} else if (i === 5) {` <br> &nbsp; &nbsp; `// do another thing;` <br> `} else {` <br> &nbsp; &nbsp; `// whatever` <br> `}` | `if i < 10:` <br> &nbsp; &nbsp; `# do a thing` <br> `else if i === 5:` <br> &nbsp; &nbsp; `# do another thing` <br> `else:` <br> &nbsp; &nbsp; ` # whatever` |

**For Loops**

| JavaScript | Python |
| --- | --- |
| for (let i = 0; i < 10; i++) { <br> &nbsp; &nbsp; // do a thing <br> } | for i in range(10): <br> &nbsp; &nbsp; # do a thing |
| for (var property in object) { <br> &nbsp; &nbsp; // do a thing <br> } | for thing in things: <br> &nbsp; &nbsp; # do a thing |
| for (let value in array) { <br> &nbsp; &nbsp; // do a thing <br> } |

## Classes

**Creating a Class**

```
class Duck {
  constructor(name) {
    this.name = name;
  }
  const sound = 'Quack';
  quack() {
    console.log(this.sound); 
  }
}
```
```
class Duck:
  def __init__(self, name):
    self._name = name
  sound = 'Quack'
  def quack(self):
    print(self.sound)
```

**Inheritance**
```
class Duckling extends Duck {
    constructor(name) {
        super();
        this.name = name;
    }
}
```
```
class Duckling(Duck):
    def __init__(self, name):
        super().__init__(name)
        self.name = name
```

| Description | JavaScript | Python |
| --- | --- | --- |
Assigning a class | `const donald = new Duck(‘donald’);` | `donald = Duck(‘donald’)` |
Using a class method | `donald.quack();` | `donald.quack()` |



