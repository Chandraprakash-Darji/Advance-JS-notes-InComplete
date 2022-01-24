# Notes for Javascript

**[Live Site Link](https://chandraprakash-darji.github.io/Js-notes/)**

**Navigate to the Topic**

1. [Basis of JS](#basis-of-jS)
2. [The 7 Primitive Data types](#the-7-primitive-data-types)
3. [Operators in JS](#operators-in-js)
4. [Template literals (Template strings)](#template-literals-template-strings)
5. [Conditional Statment ( if-Else )](#conditional-statment--if-else-)
6. [Type Conversion and Coercion](#type-conversion-and-coercion)
7. [Functions](#functions)
8. [Arrays](#arrays)
9. [Objects](#objects)
10. [Loops](#loops)
11. [DOM Manuplication](#dom-Manuplication)
12. [Developer Skills](#Developer-Skills-Credits-Jonas-Schmedtmannhttpstwittercomjonasschmedtman-JS-Course)
13. [How JavaScript Works](#how-javascript-works)

## Basis of JS

1. On page Script

```html
<script type="text/javascript">
  ...
</script>
```

2. Include external JS file

```html
<script src="filename.js"></script>
```

3. Output

```js
console.log(a); // write to the browser console
document.write(a); // write to the HTML
alert(a); // output in an alert box
confirm("Really?"); // yes/no dialog, returns true/false depending on user click
prompt("Your age?", "0"); // input dialog. Second argument is the initial value
```

4. Comments

```js
/* Multi line
comment */
// One line
```

6. Strict mode

```js
"use strict"; // Use strict mode to write secure code
x = 1; // Throws an error because variable is not declared
```

## The 7 Primitive Data types

- To check the Data type of any Varible / Value

```js
console.log(typeof "ChandraPrakash");
```

- Way of Declaring Variables

```js
var a; // variable
var a = 1,
  b = 2,
  c = a + b; // one line
const PI = 3.14; // constant
let z = "zzz"; // block scope local variable

("use strict"); // Use strict mode to write secure code
x = 1; // Throws an error because variable is not declared
// Creates property on global scope. [Not reccomend to wright Variable without Declaring]
```

1. Number: Floating point numbers -> Used for decimal and integers.

```js
let age = 23;
console.log(typeof age);
```

2. String: Sequence of characters -> Used for text.

```js
let firstName = "ChandraPrakash";
console.log(typeof firstname);
```

3. Boolean: Logical type that can only be true or false -> Used for taking decisiions.

```js
let fullAge = true;
console.log(typeof fullAge);
```

4. Undefined Value by a variables is not yet defind("empty value").

```js
let children;
console.log(typeof children);
```

5. Null: Also means 'empty value'.

```js
let myNull = null;
console.log(typeof myNull);
```

6. Symbol (ES2015): Value that is unquie and cannot be changed _[Not useful for now]_.

7. Biglnt (ES2020): Larger integers than the Number type can hold.

## Operators in JS

- [Arithmetic Operators](#arithmetic-operators)
- [Assignment Operators](#assignment-operators)
- [Comparison Operators](#comparison-operators)
- [Logical Operators](#logical-operators)
- [Ternary Operators](#ternary-operators)

### Arithmetic Operators

```js
console.log(10 + 5); // Addition -> 15
console.log(10 - 5); // Subtraction -> 5
console.log(10 / 2); // Division -> 5
console.log(10 * 4); // Multply -> 40
console.log(7 % 2); // Modulas -> 1
console.log(2 ** 4); // 16
console.log(2++); // Increment -> 3
console.log(2--); // Decrement -> 1
```

- Post and Pre Increment/Decrement

```js
let x = 5;
// x++, it will increase the value of x when the program control goes to the next statement.
// ++x, it will increase the value of x there only

x++; //post-increment, x will be 5 here and 6 in the next line
++x; //pre-increment, x will be 7 here
x--; //post-decrement, x will be 7 here and 6 in the next line
--x; //pre-decrement, x will be 5 here
```

### Assignment Operators

```js
let x = 10 + 5; // Assigns right operand value to the left operand. -> 15
x += 10; // Sum left and right operand and stores in left operand -> 25
x *= 4; // Multiply left and right operand and stores in left operand -> 100
// [ " -= " for Subtraction , " /= " for Division , " %= " for Modulas ]
x++; // 101
x--; // 100
x--; // 99
console.log(x); // 99
```

### Comparison Operators

```js
console.log(40 == 8); // Compares the equality of two operands without considering type.
console.log(40 === 8); // Compares equality of two operands with type.
console.log(40 != 8); // Compares inequality of two operands without considering type.
console.log(40 !== 8); // Compares inequality of two operands with type.
console.log(40 < 8); // Less Than / return true if 40 <> 8
console.log(40 >= 8); // Greater Than equal to / return true if 40 >= 8
console.log(40 <= 8); // Less Than equal to / return true if 40 <>= 8
```

### Logical Operators

```js
let a = 5,
  b = 10;

a != b && a < b; // returns true. // Both Condition should true.
a > b || a == b; // returns false // One Condition should true
a < b || a == b; // returns true
!(a < b); // returns false // Inverse the Solution true <-> false
!(a > b); // returns true
```

### Ternary Operators

The second part (after ? and before :) will be executed if the condition turns out to be true. Suppose, the condition returns false, then the third part (after :) will be executed.

```js
let a = 10,
  b = 5;

var c = a > b ? a : b; // value of c would be 10
var d = a > b ? b : a; // value of d would be 5
```

## Template literals (Template strings)

```js
// Untagged, these create strings:
`string text``string text line 1 
 string text line 2` // Multi line String
`string text ${expression} string text`; // access any veriable by ${variable_name}
```

- Without Template Literals

```js
let a = 5,
  b = 10;
console.log("Fifteen is " + (a + b) + " and \n not " + (2 * a + b) + ".");
// "Fifteen is 15 and
// not 20."
```

- With Template Literals

```js
let a = 5,
  b = 10;
console.log(`Fifteen is ${a + b} and
not ${2 * a + b}.`);
// "Fifteen is 15 and
// not 20."
```

## Conditional Statment ( if-Else )

```js
const age = 19;
if (age >= 18) {
  // logical condition
  status = "Eligible for driving License."; // executed if condition is true
} else {
  // else block is optional
  const yearsLeft = 18 - age;
  status = `Not eligible for driving License. Wait for ${yearsLeft} years`;
  // executed if condition is false
}
```

## Type Conversion and Coercion

- [Type Conversion](#type-conversion) Changing type of the Data explicitly.
- [Type Coercion](#type-coercion) Javascript changing type of the Data implicitly.

### Type Conversion

```js
const inputYear = "1991";
// number() for String to Number
console.log(Number(inputYear), inputYear); // 1991 '1991'
console.log(Number(inputYear) + 18); // 2009

console.log(Number("ChandraPrakash")); // NaN

// String() for Number to String
console.log(String(23)); // 23
```

#### Falsy values

[ 0 , "" , undefined , null , NaN , false ] are false if they are converted to Boolean

```js
console.log(Boolean(0)); // false
console.log(Boolean("")); // false
console.log(Boolean(NaN)); // false
console.log(Boolean(false)); // false
console.log(Boolean(undefined)); // false
console.log(Boolean(null)); // false
```

#### Truely Value

All values are truely if it is not [ 0 , "" , undefined , null , NaN , false ]

### Type Coercion

```js
// 23 Automatically converted to String while logging the String.
// " + " convert number to String
console.log("I am " + 23 + " years old."); // I am 23 years old.

// " - " , " / " , " * "  and also logical operators
// convert String to Number
console.log("23" - "10" - 3); // 10
console.log("23" > "10"); // true

// Example
let n = "1" + 1; // 11
n = n - 1; // 10
console.log(n);
```

## Switch Statment

```js
switch (
  new Date().getDay() // input is current day
) {
  case 6: // if (day == 6)
    text = "Saturday";
    break;
  case 0: // if (day == 0)
    text = "Sunday";
    break;
  default:
    // else...
    text = "Whatever";
}
```

## Functions

```js
// Function Declaration // Pros we can call Before Declaration
function addNumbers(a, b) {
  return a + b;
}
x = addNumbers(1, 2);
console.log(x); // 3

// Function Expression  // Can't call before Declration
const birthYear = 2002;
const calcAge = function (birthYear) {
  return 2022 - birthYear;
};
console.log(calcAge(birthYear)); // 20

// Arow function
const calcAge2 = (birthYear) => 2022 - birthYear;

// Arrow functions with more than one Variablea
const yearsUntilRetirment = (birthYear, firstName) => {
  const age = 2022 - birthYear;
  const retirment = 65 - age;
  return `${firstName} retires in ${retirment} years`;
};
console.log(yearsUntilRetirment(2002, "rega"));
```

## Arrays

```js
// Methoda 1 of declaring Arrays
const friends = ["Ankit", "Dave", "Jonas"];
console.log(friends);

// Method 2 of Declaring Arrays
const years = new Array(1991, 1992, 1993, 1994, 1995, 1996, 1997);
console.log(years);

// Access the Elements
console.log(friends[0], years[3]);

// length of Arrays
console.log(friends.length);

// Last item of Array
console.log(friends[friends.length - 1]);

// Changing Element
friends[1] = "Jay";
console.log(friends);

// Diffrent type of Data
const chandraPrakash = [
  "ChandraPrakash",
  "Darji",
  2022 - 2002,
  "India",
  friends,
];
console.log(chandraPrakash);

// Pushing Element
const NewLength = friends.push("C2"); // Element is pushed and NewLenght is Returned
console.log(friends, NewLength);

// Push Element at index 0
friends.unshift("Raj");
console.log(friends);

// Remove Element
const popedValue = friends.pop();
console.log(friends, popedValue);

// Remove first Element
friends.shift();
console.log(friends);

// find Element
console.log(friends.indexOf("Jay")); // 1
console.log(friends.indexOf("Jay2")); // -1 means not Exist

// check if exist
console.log(friends.includes("Jay")); // true
```

## Objects

```js
const chandraPrakash = {
  firstName: "ChandraPrakah",
  lastName: "Darji",
  age: 2022 - 2002,
  job: "Student",
  languages: ["JavaScript0", "Python", "Html", "CSS"],
  drivingLicense: false,
  // can also hold a function beacuse function is a datatype
  calcAge: function (birthYear) {
    return 2022 - birthYear;
  },
  calcAgeThis: function () {
    return 2022 - this.birthYear; // Takes value from object
  },
  getSummary: function () {
    console.log(
      `${this.firstName} is a ${
        this.job
      } of ${this.calcAgeThis()} learnig today ${this.languages[0]} with ${
        this.drivingLicense ? "a" : "no"
      } driving License`
    );
  },
};
console.log(chandraPrakash);

// Calling function
console.log(chandraPrakash.calcAge(2002));
console.log(chandraPrakash.calcAgeThis());
chandraPrakash.getSummary();

// Accesing Element
console.log(chandraPrakash.firstName); // Dot Notation
console.log(chandraPrakash["job"]); // Bracket Notation

// In Bracket Notation Expresion are Allowded
const nameKey = "Name";
console.log(chandraPrakash["first" + nameKey]);
console.log(chandraPrakash["last" + nameKey]);

// Adding a Element in Objects
chandraPrakash.location = "india";
chandraPrakash["twitter"] = "@chandra_7852";
```

## Loops

**For Loops**

```js
for (let rep = 0; rep <= 10; rep++) {
  console.log(`Hello World ${rep}`);
}
/* output =>  Hello World 0
              Hello World 1
              Hello World 2
              Hello World 3
              Hello World 4
              Hello World 5
              Hello World 6
              Hello World 7
              Hello World 8
              Hello World 9
              Hello World 10 */

// Looping through Array
const chandraPrakash = [
  "ChandraPrakah",
  "Darji",
  2022 - 2002,
  "Student",
  ["JavaScript", "Python", "Html", "CSS"],
];
const type = [];
for (let index = 0; index < chandraPrakash.length; index++) {
  // reading
  console.log(chandraPrakash[index]);
  // filling the array
  type[index] = typeof chandraPrakash[index];
}

// Backword Loop
for (let index = chandraPrakash.length - 1; index >= 0; index--) {
  console.log(chandraPrakash[index]);
}
/* output ->  ['JavaScript', 'Python', 'Html', 'CSS']
              Student
              20
              Darji
              ChandraPrakah */
```

**Continue**

```js
// Continue -> When loop gets Continue the current itreation
// is stopped and skipped to next one ...
for (let index = 0; index < chandraPrakash.length; index++) {
  if (typeof chandraPrakash[index] !== "string") continue;
  console.log(chandraPrakash[index]);
}
/* Output -> ChandraPrakah
              Darji
              Student*/
```

**Break**

```js
// Break -> When loop gets Break the whole is breaked
// and all itreation will not happen
for (let index = 0; index < chandraPrakash.length; index++) {
  if (typeof chandraPrakash[index] === "number") break;
  console.log(chandraPrakash[index]); // no item will print if number is found
}
/* Output -> ChandraPrakah
              Darji*/
```

**Nested Loops**

```js
for (let i = 0; i < 5; i++) {
  console.log(`---------- Exersie Set No ${i} ----------`);
  for (let j = 0; j < i; j++) {
    console.log(`---- Exersie lift ${j}`);
  }
}
```

**While loop**

```js
// while loop -> Loop that doesn't require a counter
let rep = 1;
while (rep <= 3) {
  console.log(`( ${rep} )is counter`);
  rep++;
}
// Loop without Counter -> If we dont know how many time loop will run
let dice = Math.trunc(Math.random() * 6);
while (dice !== 6) {
  console.log(dice);
  dice = Math.trunc(Math.random() * 7);
  if (dice === 6) console.log("Loops is about to end");
}
```

## DOM Manuplication

**Document Object Model** Structured Representation Of Html Documents. Allows Javascript To Access Html Elements And Styles To Manipulate Them.

DOM tree Structure _(Credits [Jonas Schmedtmann](https://twitter.com/jonasschmedtman) JS Course)_

![Dom Tree](./DOM/DOM_tree.png)
DOM is not Part of JavaScript ...
Javscript interact with DOM by WEB API's that browser Implements ...

- [Accessing Dom Elements](#accessing-dom-elements)
- [Grab Children/Parent Node(s)](#grab-childrenparent-nodes)
- [Create New DOM Elements](#Create-New-DOM-elements)
- [Add Elements to the DOM](#Add-Elements-to-the-DOM)
- [Add Elements to the DOM cont](#Add-Elements-to-the-DOM-cont)
- [Add/Remove/Toggle/Check Classes](#AddRemoveToggleCheck-Classes)
- []()

### Accessing Dom Elements

```js
// Returns a reference to the element by its ID.
document.getElementById("someid");

// Returns an array-like object of all child elements which have all of the given class names.
document.getElementsByClassName("someclass");

// Returns an HTMLCollection of elements with the given tag name.
document.getElementsByTagName("LI");

// Returns the first element within the document that matches the specified group of selectors.
document.querySelector(".someclass");

// Returns a list of the elements within the document (using depth-first pre-order traversal of the document's nodes)
// that match the specified group of selectors.
document.querySelectorAll("div.note, div.alert");
```

### Grab Children/Parent Node(s)

```javascript
// Get child nodes
var stored = document.getElementById("someid");
var children = stored.childNodes;

// Get parent node
var parental = children.parentNode;
```

### Create New DOM Elements

```javascript
// create new elments
var newHeading = document.createElement("h1");
var newParagraph = document.createElement("p");

// create text nodes for new elements
var h1Text = document.createTextNode("This is a nice header text!");
var pText = document.createTextNode("This is a nice paragraph text!");

// attach new text nodes to new elements
newHeading.appendChild(h1Text);
newParagraph.appendChild(pText);

// elements are now created and ready to be added to the DOM.
```

### Add Elements to the DOM

```javascript
// grab element on page you want to add stuff to
var firstHeading = document.getElementById("firstHeading");

// add both new elements to the page as children to the element we stored in firstHeading.
firstHeading.appendChild(newHeading);
firstHeading.appendChild(newParagraph);

// can also insert before like so

// get parent node of firstHeading
var parent = firstHeading.parentNode;

// insert newHeading before FirstHeading
parent.insertBefore(newHeading, firstHeading);
```

### Add Elements to the DOM cont.

Suppose you have the following HTML:

```html
<div id="box1">
  <p>Some example text</p>
</div>
<div id="box2">
  <p>Some example text</p>
</div>
```

You can insert another snippet of HTML between #box1 and #box2:

```javascript
var box2 = document.getElementById("box2");
box2.insertAdjacentHTML("beforebegin", "<div><p>This gets inserted.</p></div>");

// beforebegin - The HTML would be placed immediately before the element, as a sibling.
// afterbegin - The HTML would be placed inside the element, before its first child.
// beforeend - The HTML would be placed inside the element, after its last child.
// afterend - The HTML would be placed immediately after the element, as a sibling.
```

### Add/Remove/Toggle/Check Classes

```javascript
// grab element on page you want to use
var firstHeading = document.getElementById("firstHeading");

// will remove foo if it is a class of firstHeading
firstHeading.classList.remove("foo");

// will add the class 'anotherClass' if one does not already exist
firstHeading.classList.add("anotherclass");

// add or remove multiple classes
firstHeading.classList.add("foo", "bar");
firstHeading.classList.remove("foo", "bar");

// if visible class is set remove it, otherwise add it
firstHeading.classList.toggle("visible");

// will return true if it has class of 'foo' or false if it does not
firstHeading.classList.contains("foo");
```

## Developer Skills _(Credits [Jonas Schmedtmann](https://twitter.com/jonasschmedtman) JS Course)_

### HOW TO FAIL 🤦 AT LEARNING HOW TO CODE

- 💥 He didn’t have a clear goal at the beginning of his journey.
- 💥 He started by watching courses and reading tutorials, but he would just copy. the code without caring how it works. Sometimes he would just copy and paste code!
- 💥 He didn’t reinforce what he was learning by doing small challenges or taking notes.
- 💥 He didn’t practice coding, and didn’t come up with his own project ideas.
- 💥 He quickly became frustrated when his code was not perfectly clean or efficient.
- 💥 He lost motivation because he thought he could never know everything.
- 💥 He was learning in isolation.
- 💥 After finishing a couple of courses, he thought he now was a web developer and could start applying to jobs. But he couldn’t even build an app on his own!

### HOW TO SUCCEED 🎉 AT LEARNING HOW TO CODE

- 💥 He didn’t have a clear goal at the beginning of his journey.

  - 👌 Set a specific, measurable, realistic and time-based goal
  - 👌 Know exactly why you are learning to code: Switching careers? Finding a better job?
  - 👌 Imagine a big project you want to be able to build!
  - 👌 Research technologies you need and then learn them.

- 💥 He would just copy the code without caring how it works. Sometimes he would just copy and paste code!

  - 👌 Understand the code that you’re studying and typing
  - 👌 Always type the code, don’t copy-paste!

- 💥 He didn’t reinforce what he was learning by doing small challenges or taking notes.

  - 👌 After you learn a new feature or concept, use it immediately.
  - 👌 Take notes
  - 👌 Challenge yourself and practice with small coding exercises and challenges.
  - 👌 Don’t be in a hurry to complete the course fast!

- 💥 He didn’t practice coding, and didn’t come up with his own project ideas.

  - 👌 Practicing on your own is the most important thing to do.
  - 👌 This is NOT optional! Without practice outside of courses, you won’t go anywhere!
  - 👌 Come up with your own project ideas or copy popular sites or applications, or just parts of them in the beginning.
  - 👌 Don’t be stuck in “tutorial hell”

- 💥 He quickly became frustrated when his code was not perfectly clean or efficient.

  - 👌 Don’t get stuck trying to write the perfect code!
  - 👌 Just write tons of code, no matter the quality!
  - 👌 Clean and efficient code will come with time.
  - 👌 You can always refactor code later.

- 💥 He lost motivation because he thought he could never know everything.

  - 👌 Embrace the fact that you will nesver you know everything.
  - 👌 Just focus on what you need to achieve your goal!

- 💥 He was learning in isolation.

  - 👌 Explain new concepts to other people. If you can explain it, you truly understand it!
  - 👌 Share your goals to make yourself accountable.
  - 👌 Share your learning progress with the web dev community (#100DaysOfCode, #CodeNewbie, #webdev, etc).

- 💥 After finishing a couple of courses, he thought he now was a web developer and could start applying to jobs.

  - 👌 The biggest misconception that people have!
  - 👌 Courses are an amazing starting point, but are only the beginning of your journey.

[!how to code process](./DOM/Codingprocess.png)

### HOW TO FAIL 🤦 AT SOLVING PROBLEMS

- **WHENEVER JOHN ENCOUNTERS A PROBLEM:**

  - 💥 He jumps at the problem without much thinking.
  - 💥 He implements his solution in an unstructured way.
  - 💥 He gets stressed out when things don’t work.
  - 💥 He is too proud to research solutions.

- **FIX**

  - 💥 Stay calm and slow down, don’t just jump at a problem without a plan.
  - 💥 Take a very logical and rational approach (programming is just logic, in the end…).
  - 💥 Use my 4-step framework to solve any problem.

### 4 STEPS FRAMEWORK TO SOLVE ANY PROBLEM

1. Make sure you 100% understand the problem. Ask the right questions to get a clear picture of the problem.
2. Divide and conquer: Break a big problem into smaller sub-problems.
3. Don't be afraid to do as much research as you have to.
4. For bigger problems, write pseudo-code before writing the actual code.

### WHAT IS A SOFTWARE BUG?

- 💥 Software bug: Defect or problem in a computer program. Basically, any unexpected or unintended behavior of a computer program is a software bug.
- 💥 Bugs are completely normal in software development!
- 💥 Debugging: Process of finding, fixing and preventing bugs.

### THE DEBUGGING PROCESS

1. Identify

- 👉 During development
- 👉 Testing software
- 👉 User reports duringproduction
- 👉 Context: browsers,users, etc.

2. Find

- 👉 Developer console (simple code)
- 👉 Debugger (complexcode)

3. Fix

- 👉 Replace wrong solution with new correct solution

4. Prevent

- 👉 Searching for thesame bug in similar code
- 👉 Writing tests usingtesting software

## How JavaScript Works
