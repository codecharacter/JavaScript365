# Complete JavaScript Course - Notes
## S2: JavaScript Fundamentals - Part 1
### Hello, World!
`alert("Hello, World!");`

### Linking a JS File
`<body><script src="script.js"></script></body>`

### Values & Variables
`let js = "amazing";`
`console.log(js);`
`let PI = 3.14;`

### Data Types
- Number: floating point
- String: sequence of chars
- Boolean: logical type
- Undefined: empty value
- Null: also, empty value
- Symbol: unique
- BigInt: larger integers

### Dynamic Typing
- note: do not have to define
- KEY: the value has type, NOT variable
`console.log(typeof true);`

### let, const and var
`let age = 49;`
`age = 50; // reassigned, mutate`
`const birthYear = 1973;`
- default to this in practice
- var: legacy JS (prior to ES6) ... do NOT use

### Basic Operators
- Math operators
- Assignment operators
- Comparison operators

### Operator Precedence
- MDN Docs: [Operator Precedence](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)
- left-to-right > , < right-to-left

### Coding Challenge #1

### Strings & Template Literals
- const jonasNew = `I'm ${variable} a ${job}...`;"
- back tick, template literals
- multi-line strings

### Taking Decisions: if/else Statements
- control structure
    if () {
    
    } else {

    }

### Coding Challenge #2

### Type Conversion & Coercion
- type conversion = manually change types
- type coercion = JS auto converts types

### Truthy & Falsy Values
- falsy: not exactly false but will be converted to false
    - 0
    - ' ' (empty)
    - undefined
    - null
    - NaN
- truthy: will be converted to true

### Equality Operators: == vs ===
- = assignment
- === comparison (strict)
- == does type coercion (loose)
- !== "not", different

### Boolean Logic
- AND, OR, NOT
- AND: true when ALL are true
- OR: true when ONE is true
- NOT: inverts true/false value (!var)

### Logical Operators
- examples of Boolean logic

### Coding Challenge #3

### switch Statement
    switch(var) {
        case "var":
            console.log();
            break;
        case "var":
            console.log();
            break;
        default:
            console.log();
    }

### Statements & Expressions
- Expression = produces a value
- Statement = code executed, does not produce a value

### Conditional (Ternary) Operator
`(condition) ? (if) : (else)`

### Coding Challenge #4

### JS Releases: ES5, ES6, ESNext

## S3: JavaScript Fundamentals - Part 2

### Activating Strict Mode
`'use strict';`
- write more secure code, avoid introducing bugs
- prevents us from doing certain things
- presents visible error output in editor

### Functions
- function: a piece of code we can reuse in our code
    function fruitProcessor (apples, oranges) {
        const juice = `Juice with ${apples} apples and ${oranges} oranges.`;
        return juice;
    }

    const appleJuice = fruitProcessor(5, 0);
    console.log(appleJuice);

    const appleOrangeJuice = fruitProcessor(2, 4);
    console.log(appleOrangeJuice);
- DRY: Don't Repeat Yourself
- console.log is a built-in function

### Function Declarations vs Expressions
- function declaration
    function calcAge1(birthYear) {
        return 2037 - birthYear;
    }
- function expression
    const calcAge2 = function (birthYear) {
        return 2037 - birthYear;
    }
- a function really is just a "value"
- difference: we can call fn declarations BEFORE they're defined

### Arrow Functions
- special form of function expression
- value returned implicitly
    const calcAge3 = birthYear => 2037 - birthYear;
- arrow functions do not get a "this" keyword (future lecture)

### Functions Calling Other Functions
    function cutFruitPieces(fruit) {
        return fruit * 4;
    }

    function fruitProcessor (apples, oranges) {
        
        const applePieces = cutFruitPieces(apples);
        const orangePieces = cutFruitPieces(oranges);

        const juice = `Juice with ${applePieces} pieces of apple and ${orangePieces} pieces of orange.`;
        return juice;
    }
    console.log(fruitProcessor(2, 3));

### Reviewing Functions
- return keyword will immediately exit a function
    - "the function has returned"
- Function declaration: fn that can be used before it's declared
- Function expression: essentially a function value stored in a variable
- Arrow function: great for quick one-line functions. Has no "this" keyword.
- Work similarly: input data, transform data, output data

### Coding Challenge #1


### Intro to Arrays
- Data Structure
    const friends = ['Michael', 'Steven', 'Peter'];
    const years = new Array(1991, 1984, 2008, 2020);
- change array values, even if "const"
    - primitive values cannot be changed, but arrays are not primitve

### Basic Array Operations (Methods)
- methods = array operations
    - add/remove/check elements
    const friends = ['Michael', 'Steven', 'Peter'];
    friends.push('Jay');
    friends.unshift('John');
    friends.pop(); // Last
    friends.shift(); // First

### Coding Challenge #2


### Intro to Objects
- Object data structure
- define key:value pairs
- order of elements does not matter for retrieval
- useful for more unstructured data

### Dot vs Bracket Notation
    const myCountry = {
        country: 'USA',
        capital: 'Washington DC',
        language: 'English',
        population: 330,
        neighbors: ['Canada', 'Mexico']
    };
- bracket: use when requiring computation
    myCountry.population = myCountry.population + 2;
- dot: most cases where you know/need key value
    myCountry['population'] = myCountry['population'] - 2;

### Object Methods
- any function attached to an object is called a method
- this keyword


### Coding Challenge #3


### Iteration: The for Loop
    for(let rep = 1; rep <= 10; rep++) {
        console.log(`Lifting weights repetition ${rep}`);
    }
- control structure to automate repetitive tasks


### Looping Arrays, Breaking and Continuing
    console.log("--- ONLY STRINGS ---");
    for(let i = 0; i < jonas.length; i++) {
        if(typeof jonas[i] !== 'string') continue;

        console.log(jonas[i], typeof jonas[i]);
    }

    console.log("--- BREAK WITH NUMBER ---");
    for(let i = 0; i < jonas.length; i++) {
        if(typeof jonas[i] === 'number') break;

        console.log(jonas[i], typeof jonas[i]);
    }

### Looping Backwards and Loops in Loops
    for(let i = jonas.length - 1; i >= 0; i--) {
        console.log(i, jonas[i]);
    }

    for(let exercise = 1; exercise < 4; exercise++) {
        console.log(`--- Starting Exercise ${exercise}`);

        for(let rep = 1; rep < 6; rep++) {
            console.log(`Lifting weights rep ${rep}`);
        }
    }

### The while Loop
    let dice = Math.trunc(Math.random() * 6) + 1;

    while (dice !== 6) {
        console.log(`You rolled a ${dice}`);
        dice = Math.trunc(Math.random() * 6) + 1;
    }

### Coding Challenge #4


## S4: How to Navigate this Course

### Pathways and Section Roadmaps


### Course Pathways


## S5: Developer Skills & Editor Setup