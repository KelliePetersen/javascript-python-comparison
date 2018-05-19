# JavaScript vs Python
This is a side-by-side comparison of JavaScript (ES2015) and Python (3.6) syntax.

## Contents

[Important Notes](#important-notes)  
[Basics](#basics)  
[Functions](#functions)  
[Loops](#loops)  
[Classes](#classes)  

## Important Notes

JavaScript uses brackets { and } to create blocks.  
Python uses indentation instead of brackets. Expressions inside statements (such as a loop or class) must be indented. 

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
| Swap values of variables | `[a, b] = [b, a]` | `a, b = b, a` |
| Find string inside a string | `"Hello".indexOf("ell");` returns 1 | `"Hello".find("ell")` returns 1 |
| Find string from a starting index | `"Kellie". indexOf("e", 3)` returns 5 | `"Kellie".find("ell", 3)` returns 5 |

## Functions

Creating a function or defining procedures

let myFunction = function() { 
  console.log("Hello world!"); 
} 

function myFunction() {
  console.log("Hello world!"); 
} 

def name():
  print("Hello world!")
  
## Loops

while i < 10:
  \# do a thing

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
Assigning a class | const donald = new Duck(‘donald’); | donald = Duck(‘donald’) |
Using a class method | donald.quack(); | donald.quack() |



