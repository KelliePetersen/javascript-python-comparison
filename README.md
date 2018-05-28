# JavaScript vs Python
This is a side-by-side comparison of JavaScript (ES2015) and Python (3.6) syntax.  
I created it so that I could use a description to find the command I need.  
Searching for something specific? Use ctrl + f (or cmd + f)

## Contents

[Important Notes](#important-notes)  
[Basics](#basics)  
[Strings](#strings)  
[Arrays and Lists](#arrays-and-lists)  
[Functions](#functions)  
[Loops](#loops)  
[Classes](#classes)  

## Important Notes

JavaScript uses brackets { } to create blocks. Python uses indentation instead of brackets. This means that expressions inside statements (such as a loop or class) must be on a new line and indented. Look at [Classes](#classes) section for examples.

## Basics

| Description | JavaScript | Python |
| --- | --- | --- |
| Shebang |
| Single-line Comment | `// I am a comment` | `# I am a comment` |
| Multi-line Comment| `/* I am a multi-line comment \*/` | `""" I am a multi-line comment """` |
| Defining variables | `var/const/let myVariable = "I am a variable";` | `myVariable = "I am a variable"` | 
| Printing lines | `console.log("Hello world");` | `print("Hello world")` |
| Swap values | `[a, b] = [b, a];` | `a, b = b, a` |
| User input prompt | let x = prompt("What is your name?") | x = input("What is your name?") |

## Strings
A lowercase "string" means that you replace "string" with the string's name. A capitalized "String" should be kept as it is. 

| Description | JavaScript | Python |
| --- | --- | --- |
| Create a string with UTF | String.fromCharCode(UTF, UTF, ...) | |
| Create a string with code points | String.fromCodePoint() | |
| Create new string containing another string's UTF value from a specific index | string.charAt(index) | |
| Return the UTF code of a string at an index | string.charCodeAt(index) | |
| Return the code point at an index | string.codePointAt(index) | |
| Variables inside strings (old) | "Hello, I feel " + mood | "Hello, I feel {}".format(mood) |
| Variables inside strings (new) | \`Hello, I feel ${mood}\` | f"Hello, I feel {mood}" |
| Find string length | string.length(); | len(string) |
| Find string inside a string | "Hello".indexOf("ell"); returns 1 | "Hello".find("ell") returns 1 |
| Find string from a starting index | "Kellie". indexOf("e", 3) returns 5 | "Kellie".find("ell", 3) returns 5 |
| Capitalize string | string[0].toUpperCase(); | string.capitalize() |
| Upper case string | string.toUpperCase(); | string.upper() |
| Lower case string | string.toLowerCase(); | string.lower() |
| Concatenate with other objects | string.concat(arguments) or + | |

## Arrays and Lists   
A lowercase "array" means that you replace "array" with the string's name. A capitalized "Array" should be kept as it is. 

| Description | JavaScript | Python |
| --- | --- | --- |
| Create an array/list | var array = [1,2,3] | list = [1,2,3] |
| Turn input into an array/list | Array.from(input) | list(input) |
| Select an index | array[2] | list[2] |
| Find array length | string.length(); | len(string) |
| Get an array/list backwards | array.reverse() | list.reverse() or list[::-1] |
| Get the last element | array[array.length-1]| list[-1] |
| Copy a portion of an array/list | array.slice(start, end) | list[start:end] |
| Add an element to the end | array.push(element) | list.append(element) |
| Add an element to the start | array.unshift(element) | list.insert(0, element) |
| Combine two arrays/lists | array.concat(array2) | list.extend(list2) |
| Insert an element into a specific index | array.splice(index, 0, element) | list.insert(index, element) | 
| Remove an element at a specific index | array.splice (index, 1) | list.pop(index) |
| Remove an element | | list.remove(element) | 
| Remove the first element | array.shift() | list.pop(0) |
| Remove the last element | array.pop() | list.pop() |
| Return the first index of an element | array.indexOf(element) | list.index(element) |
| Return the last index of an element | array.lastIndexOf(element) | |
| Couns the occurences of an element | array.filter(function(x){return x===element}).length | list.count(element) |
| Sort elements in an array/list | array.sort() | list.sort() |
| Create a new sorted version of the array/list | | sorted(list) |
| Make a shallow copy | array.slice(0, array.length) | list.copy() | 
| Remove all elements in an array/list | array.splice(0, array.length) | list.clear() |
| Check if there is at least one element <br> matching the specified element | array.includes(element) | list.any(element) |
| Check if all elements equal a specified element | array.every(function(x){return x===element} | list.all(element) |
| Check if an object is an array/list | array.isArray(object) | |
| Check if all elements pass a function test | array.every(function) | |
| Check if some elements pass a function test | array.some(function) | |
| Create an array/list of elements that pass a test | array.filter(function) | |
| Return the first element that passes a test | array.find(function(element)) | |
| Perform a function on each element | array.map(function)| map(function, list) |
| Copy and reorder elements | array.copyWithin(position, start, end) | |
| Fill an existing array/list with values | array.fill(value, start, end) | |
| Return an iterator with keys [a,b]-> 0 1 | var iterator = array.keys() | |
| Return an iterator with values [a,b]-> a b | var iterator = array.value() | |
| Return an iterator with key/value pairs | var iterator = array.entries() | |

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
| for (let value of array) { <br> &nbsp; &nbsp; // do a thing <br> } |
| array.forEach(function(item, index) { <br> &nbsp; &nbsp; // do a thing <br> });

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



