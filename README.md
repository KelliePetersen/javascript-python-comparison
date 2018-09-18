# JavaScript vs Python
This is a side-by-side comparison of JavaScript (ES6/ES2015) and Python (3.6) syntax.  
I created it so that I could use a description to find the command I need.  
Searching for something specific? Use ctrl + f (or cmd + f)

## Contents

- [Important Notes](#important-notes)  
- [Basics](#basics)  
- [Strings](#strings)  
  - [Length and White Space](#length-and-white-space)  
  - [Character Types](#character-types)  
- [Arrays and Lists](#arrays-and-lists)  
- [Conditional Statements and Loops](#conditional-statements-and-loops)  
- [Functions](#functions)  
- [Classes](#classes)  
- [Objects](#objects)  
- [Iterators and Generators](#iterators-and-generators)

## Important Notes

JavaScript uses brackets { } to create blocks. Python uses colons and indentation. This means that expressions inside statements (such as a loop or class) must be on a new line and indented. Look at the [Classes](#classes) section for examples.

## Basics

| Description | JavaScript | Python |
| --- | --- | --- |
| Single-line Comment | // I am a comment | # I am a comment |
| Multi-line Comment| /* I am a multi-line comment \*/ | """ I am a multi-line comment """ |
| Defining variables | var/const/let myVariable = "I am a variable"; | myVariable = "I am a variable" | 
| Printing lines | console.log("Hello world"); | print("Hello world") |
| Swap values | [a, b] = [b, a]; | a, b = b, a |
| User input prompt | let x = prompt("What is your name?") | x = input("What is your name?") |

## Strings
A lowercase "string" means that you replace "string" with the string's name. A capitalized "String" should be kept as it is.  
*Italics* mean that a parameter is optional. An ellipsis (...) means there can be many parameters. 'Start' and 'end' are indexes. 

| Description | JavaScript | Python |
| --- | --- | --- |
| Copy every nth element of a string | | string[slice(start, end, step)] |
| Return a string of the specified object | string.toString() | |
| Return the primitive value of a string | string.valueOf() | |
| Create a string with UTF | String.fromCharCode(UTF, UTF, ...) | |
| Create a string with code points | String.fromCodePoint() | |
| Create new string containing another string's <br> UTF value from a specific index | string.charAt(index) | |
| Return the UTF code of a string at an index | string.charCodeAt(index) | |
| Return the code point at an index | string.codePointAt(index) | |
| Turn a string into an array/list | string.split('') | list(string) |
| Variables inside strings (old) | "Hello, I feel " + mood | "Hello, I feel {}".format(mood) |
| Variables inside strings (new) | \`Hello, I feel ${mood}\` | f"Hello, I feel {mood}" |
| Find text inside a string | string.indexOf('text') | string.find('text') |
| Find text from a starting index | string.indexOf('text', *index*) | string.find('text', *index*) |
| Capitalize string | string[0].toUpperCase(); | string.capitalize() |
| Swap case of a string | | string.swapcase() |
| Uppercase string | string.toUpperCase(); | string.upper() |
| Lowercase string | string.toLowerCase(); | string.lower() |
| Uppercase in locale case mappings | string.toLocaleUpperCase(locale, ...) | |
| Lowercase in locale case mappings | string.toLocaleLowerCase(locale, ...) | |
| Casefold string (caseless matching) | | string.casefold() |
| Copy a portion of a string | string.slice(start, end) | string[start, end] |
| Return a portion of a string by length | string.substring(start, *start+length*) | string[start, start+end] |
| Return a portion of a string by index | string.substring(start, *end*) | string[start, end] |
| Check if string includes specified text | string.includes(text) | text in string |
| Check if string starts with specified text | string.startsWith(text, *index*) | |
| Check if string ends with specified text | string.endsWith(text, *index*) | string.endswith(text, *start*, *end*) |
| Find the index of specified text | string.indexOf(text, *index*) | string.find(text, *start*, *end*) <br> or string.index(text, *start*, *end*) |
| Find the last index of specified text | string.lastIndexOf(text) | |
| Find the index of text matching RegExp | string.search(RegExp) | |
| Count occurrences of the specified text | | string.count(text, *start*, *end*) |
| Return a new string that has replaced RegExp <br> matching content with the specified text | string.replace(RegExp, text) | |

### Length and White Space
| Description | JavaScript | Python |
| --- | --- | --- |
| Find string length | string.length(); | len(string) |
| Concatenate with other objects | string.concat(arguments) or + | +, += or StringIO module |
| Concatenate with an iterable | | string.join(iterable) |
| Increase string length with spaces at start | string.padStart(length) | |
| Increase string length with specified text | string.padStart(length, *text*) | |
| Increase string length with spaces at end | string.padEnd(length) | |
| Increase string length with specified text | string.padEnd(length, *text*) | |
| Increase string length with spaces at both sides | Combine padStart and padEnd | string.center(length) |
| Increase string length with specified text | Combine padStart and padEnd | string.center(length, *text*) |
| Remove white space from start and end | string.trim() | string.strip() |
| Remove white space from the start | string.trimStart() | string.lstrip() |
| Remove white space from the end | string.trimEnd() | string.rstrip() |
| Repeat the text in a string multiple times | string.repeat(number) | string * number |
| Replace tabs in string with spaces | string.replace(/\t+/g, " ") | string.expandtabs(*number*) |

### Character Types  
| Description | JavaScript | Python |
| --- | --- | --- |
| Check if all characters are lowercase | Use RegExp or char == char.toLowerCase() in a loop | string.islower() |
| Check if all characters are uppercase | Use RegExp or char == char.toUpperCase() in a loop | string.isupper() |
| Check if all characters are titlecase | Use RegExp | string.istitle() |
| Check if all characters are letters | Use RegExp | string.isalpha() |
| Check if all characters are alphanumeric | Use RegExp | string.isalnum() |
| Check if all characters are digits | Use RegExp or loop | string.isdigit() |
| Check if all characters are decimal | Use RegExp | string.isdecimal() |
| Check if all characters are numeric | Use RegExp or loop | string.isnumeric() |
| Check if all characters are space | string.trim() == "" | string.isspace() |
| Check if all characters are printable | |string.isprintable() |

## Arrays and Lists   
A lowercase "array" means that you replace "array" with the array's name. A capitalized "Array" should be kept as it is.  
*Italics* mean that a parameter is optional. An ellipsis (...) means there can be many parameters. 'Start' and 'end' are indexes.

| Description | JavaScript | Python |
| --- | --- | --- |
| Create an array/list | var array = [1,2,3] | list = [1,2,3] |
| Make a shallow copy | array.slice(0, array.length) or <br> ES6: let copy = [...array]; | list.copy() | 
| Copy a portion of an array/list | array.slice(start, end) | list[start:end] |
| Copy every nth element | | list[slice(start, end, step)] |
| Sort elements in an array/list | array.sort() | list.sort() |
| Create a new sorted version of the array/list | | sorted(list) |
| Remove all elements in an array/list | array.splice(0, array.length) | list.clear() |
| Turn input into an array/list | Array.from(input) | list(input) |
| Turn array/list into a string | array.join('') | |
| Return a new string of the array/list | array.toString() | |
| Return a locale string of the elements | array.toLocaleString(locales, options) | |
| Select an index | array[2] | list[2] |
| Find array length | string.length(); | len(string) |
| Get an array/list backwards | array.reverse() | list.reverse() or list[::-1] |
| Get the last element | array[array.length-1]| list[-1] |
| Add an element to the end | array.push(element) | list.append(element) |
| Add an element to the start | array.unshift(element) | list.insert(0, element) |
| Combine two arrays/lists | array.concat(array2) | list.extend(list2) |
| Combine multiple arrays/lists | let combo = [...array1, ...array2, ...etc]; | |  
| Insert an element into a specific index | array.splice(index, 0, element) | list.insert(index, element) | 
| Remove an element at a specific index | array.splice (index, 1) | list.pop(index) |
| Remove an element | | list.remove(element) | 
| Remove the first element | array.shift() | list.pop(0) |
| Remove the last element | array.pop() | list.pop() |
| Return the first index of an element | array.indexOf(element) | list.index(element) |
| Return the last index of an element | array.lastIndexOf(element) | |
| Count  the occurences of an element | array.filter(function(x) { <br> return x===element }).length | list.count(element) |
| Check if there is at least one element <br> matching the specified element | array.includes(element) | list.any(element) |
| Check if all elements equal a specified element | array.every(function(x) { <br> return x===element } | list.all(element) |
| Check if an object is an array/list | array.isArray(object) | |
| Check if all elements pass a function test | array.every(function) | |
| Check if some elements pass a function test | array.some(function) | |
| Create an array/list of elements that pass a test | array.filter(function) | |
| Return the first element that passes a test | array.find(function(element)) | |
| Perform a function on each element | array.map(function)| map(function, list) |
| Copy and reorder elements | array.copyWithin(position, start, end) | |
| Fill an existing array/list with values | array.fill(value, start, end) | |
| Flatten a nested array/list | array.flat(depth) | |
| Return an iterator with keys [a,b]-> 0 1 | var iterator = array.keys() | |
| Return an iterator with values [a,b]-> a b | var iterator = array.value() | |
| Return an iterator with key/value pairs | var iterator = array.entries() | |
| Destructuring an array/list | const [a, b,, ...arr] = [1, 2, 3, 4, 5, 6]; <br> (a=1, b=2, 3 is skipped, arr=[4,5,6]) | |

## Conditional Statements and Loops

**While Loop**

| JavaScript | Python |
| --- | --- |
| while (i < 10) { <br> &nbsp; &nbsp; // do a thing <br> } | while i < 10: <br> &nbsp; &nbsp; # do a thing |

**if/else**

| JavaScript | Python |
| --- | --- |
| if (i < 10) { <br> &nbsp; &nbsp; // do a thing; <br> } else if (i === 5) { <br> &nbsp; &nbsp; // do another thing; <br> } else { <br> &nbsp; &nbsp; // whatever <br> } | if i < 10: <br> &nbsp; &nbsp; # do a thing <br> elif i === 5: <br> &nbsp; &nbsp; # do another thing <br> else: <br> &nbsp; &nbsp;  # whatever |

**Ternary Operators**

| JavaScript | Python |
| --- | --- |
| `(condition) ? trueResult : falseResult;` | `trueResult if condition else falseResult` |

**Switch**
```
switch(expression) {
  case value1:
    //do a thing
    break;
  case value2:
    // do a different thing
    break;
  default:
    // do the default thing
} 
```

Python's closest equivalent to Switch, besides if/elif/else, are dictionaries:
```
def switch(expression):
  return {
    'a': value1,
    'b': value2,
  }.get(expression, defaultvalue)
```

**For Loops**

| JavaScript | Python |
| --- | --- |
| for (let i = 0; i < 10; i++) { <br> &nbsp; &nbsp; // do a thing <br> } | for i in range(10): <br> &nbsp; &nbsp; # do a thing |
| for (var property in object) { <br> &nbsp; &nbsp; // do a thing <br> } | for thing in things: <br> &nbsp; &nbsp; # do a thing |
| for (let value of array) { <br> &nbsp; &nbsp; // do a thing <br> } |
| array.forEach(function(item, index) { <br> &nbsp; &nbsp; // do a thing <br> });

## Functions

Creating a function or defining procedures

| JavaScript | Python |
| --- | --- |
| let double = function() { <br> &nbsp; &nbsp; return num * 2; <br> } | def double(num): <br> &nbsp; &nbsp; return num * 2 |
| function double(num) { <br> &nbsp; &nbsp; return num * 2; <br> } | |
| const double = (num) => num * 2; | |

Creating default parameters

| JavaScript | Python |
| --- | --- |
| `myFunction(name = "Bob", age = 34) {}` | |

Creating a function that accepts any number of parameters

| JavaScript | Python |
| --- | --- |
| `myFunction(...args) {}` | |

Creating a constructor (ES5)
```
function Duck(name, color) {
  this.name = name;
  this.color = color;
}
```

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

**Creating a Class with Private Variables**
```
class Duck {
  constructor(name) {
    this._name = name;
  }
  get name() {
    return this._name;
  }
  set name(newName) {
    this._name = newName;
  }
}
```

| Description | JavaScript | Python |
| --- | --- | --- |
| Assigning a class | `const donald = new Duck('donald');` | `donald = Duck('donald')` |
| Using a class method | `donald.quack();` | `donald.quack()` |
| Changing a class value | | |
| Checking if an instance | `donald instanceof Duck;` | |

## Objects

**Creating an Object**
```
var myObject = {
  name: "Jerry",
  age: 28,
  sayHello: function() { return "Hello!" } OR
  sayHello() { return "Hello!" } 
}
```

**Destructuring assignment** (assigning variables to object properties) 

| Description | JavaScript | Python |
| --- | --- | --- |
| The test object | `var object = {a:10, b:20, c:30};` | |
| Singular destructuring | `var a = object.a;` (a returns 10) | |
| Multiple destructuring | `var {a, b, c} = object;` | |
| Destructuring with different variable names | `var {a:x, b:y, c:z} = object;` <br> (x returns 10, y returns 20, z returns 30) | |

## Iterators and Generators

**Creating an Iterator**
```
function createIterator(array) {
  let nextIndex = 0;
  return {
    next: function() {
      return nextIndex < array.length ? 
        {value: item[nextIndex++], done: false} :
        {done: true}
    }
  };
}
```
In Python, iterators can be returned with the iter() function or built yourself.  
For..in loops also internally create an iterator object. 
```
my_array = [1, 2, 3]
my_iterator = iter(my_array)
next(my_iterator) #1
my_iterator.__next__() #2
```
```
class create_iterator:
  def __init__(self, max = 0):
    self.max = max
  def __iter__(self):
    self.n = 0
    return self
  def __next__(self):
    if self.n <= self.max:
      return self.n += 1
    else:
      raise StopIteration
```

**Iterating**
```
let myIterator = createIterator([1, 2, 3]);
myIterator.next().value //1
myIterator.next().value //2
myIterator.next().done //False
myIterator.next().value //3
myIterator.next().done //True
```
*Note: This returns the current value BEFORE iterating, which is normal behavior for an iterator.  
To return the value after iterating, change [nextIndex++] to [++nextIndex] in the createIterator function.*
```
my_iterator = create_iterator(3)
i = iter(my_iterator)
next(i) #1
next(i) #2
next(i) #3
```

**Generator**
```
function* createGenerator() {
  console.log("Start of block 1");
  yield "End of block 1";
  console.log("Start of block 2");
  console.log("End of block 2");
}

const myGenerator = createGenerator();
myGenerator.next(); //Start of block 1, End of block 1
myGenerator.next(); //Start of block 2, End of block 2
```
```
def my_generator():
  print("Start of block 1")
  yield "End of block 1"
  print("Start of block 2")
  print("End of block 2")
  
for num in my_generator():
  print(num) 
```
