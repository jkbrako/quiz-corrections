# quiz-corrections

The revisions are for quizzes 4-7. Thank you for taking the time to go through the repository.

## quiz-4

### question-8

The following values that are always considered falsey are null, 0, "", undefined, NaN, and false. These are always considered false because these values are considered false when encountered in a Boolean context.


### question-9 

The valid data types in JavaScript are null, undefined, objects, strings, floating-points, symbols, and numbers. This is true because they can be stored in variables. Since JavaScript types are dynamic types, therefore, the same variable can hold multiple valid data types, within the same variable, if they so choose. 
For example:
```
let a = 321 // "a" is defined as numbers
a = "lol"   // "a" can also be defined as a string
```
### question-10

The following statement that declares and initializes a variable called `x` with the value 27 are:
```
let x;
x = 27;
```
'Let' declares and initialized the variable. The second line assigned 27 to variable `x`.

## quiz-5
### question-1

The following are valid logical operators in JavaScript:
```
! 
&&
||
```
The `!` operator means NOT, the `&&` operator means AND and the `||` operator means OR. These operators can be applied to values of any type, including boolean values.

### question-2
For the code
```
let x = 43;
let y = "43";

if ( /* missing condition */ ) {
    console.log("x and y have equivalent values and data types.");
}

if ( /* missing condition */ ) {
    console.log("x and y have different values and data types.");
}
```
The two expressions that satisfy the missing conditions above are:
```
x === y
x !== y
```
x and y have equivalent values and data types so, `x === y` is appropiate as it means x is equql value and type to y. The  second condition is met as x and y have different values and data types so `x !== y` as it means x is not of equal value and type.

### question-3
The following are valid relational operators in JavaScript:
```
==
===
<
<=
>
!==
!=
>=
```
All of these operators perform comparisons between values. For example, If the operands are numbers, they will perform a numeric comparison.

### question-5
```
let a = 3;
let b = 7;
let c = 9;

if (a < b /* missing operator */ a < c) {
    console.log("we know for sure that a is the smallest of the three.");
}

if (c > a /* missing operator */ c > b) {
    console.log("we know for sure that c is not the smallest of the three.");
}
```
The two operators minimally satisfy the above statements:
```
a < b && a < c
c > a || c > b
```
The 1st operator satisfies the statements as it means `3 < 7` can be coerced to be `false` along with `3 < 9`. The 2nd operator also satisfies `9 > 3`  can be coerced into  being `true` along with `9 > 7`.

### question-6
The following code segment, which is designed to assign a status of HR or ND to each student (given their marking period grades. 
```
let status;
if (studentGrade >= 88) {
    status = "HR";
} else {
    status = "ND";
}
```
The ternary operator that effectively replaces the above if-else statement are:
```
let status = (studentGrade < 88) ? "ND" : "HR";
```
```
let status = (studentGrade >= 88)
   ? "HR" 
   : "ND";
```
```
let status = (studentGrade < 88) ? "ND" : "HR";
```
I forgot to put: 
```
let status = (studentGrade < 88) ? "ND" : "HR";
```
but this is also an operator that effectively replaces the if-else statement as it is the same as the other two operators. They all make `status = "HR";` if `studentGrade >= 88` otherwise, they `status = "ND";`.

### question-7

"Suppose I have stored the current day of the week as a numeric value (0 through 6 representing Monday through Sunday). I want to convert and print the numeric value to its string equivalent. You may assume the following setup:"
```
let dayCode = Number(prompt("Today is... (enter 0 through 6)"));
let day;

/* missing switch statement */

console.log("Today is " + day + "!");
```
Using a switch statement, I can achieve my goal with:
```
switch (dayCode)
   case 0: day = "Monday"; break;
   case 1: day = "Tuesday"; break;
   case 2: day = "Wednesday"; break;
   case 3: day = "Thursday"; break;
   case 4: day = "Friday"; break;
   case 5: day = "Saturday"; break;
   case 6: day = "Sunday"; break;
   default: day = "an unknown day"; break;
}
```
It is not:
```
switch (dayCode)
   case "0": day = "Monday"; break;
   case "1": day = "Tuesday"; break;
   case "2": day = "Wednesday"; break;
   case "3": day = "Thursday"; break;
   case "4": day = "Friday"; break;
   case "5": day = "Saturday"; break;
   case "6": day = "Sunday"; break;
   default: day = "an unknown day"; break;
}
```
as case #'s do not have quotation marks.

### question-9
"Suppose I wanted to convert a student's numeric quiz score to an approximate letter grade. You may assume the following setup is already in place."
```
let score = Number(prompt("Enter score: "));
let letterGrade;
```
The simplest way to achieve that goal is through:
```
if (score >= 90) {
    letterGrade = "A";
} else if (score >= 80) {
    letterGrade = "B";
} else if (score >= 70) {
    letterGrade = "C";
} else if (score >= 60) {
    letterGrade = "D";
} else {
    letterGrade = "F";
}
```
As the parameters for the function only contain `if` and `else if` statements. This is the most straightforward algorithm to solve the problem.

### question-10
"Consider the following code segment:"
```
let score = Number(prompt("How'd you do on the quiz?"));

if (score >= 65) {
    console.log("You passed!");
}
```
"Suppose I wanted to print an alternate message if the student failed." You can d this by:
add an `else` clause that prints the alternate message. The `else` clause allows for alternative message to be displayed if the conditions put above were not met.

### question-12
This set of code represents a valid `for` loop that will execute at least once and will terminate:
```
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```
The `for` loop is set as it sets up and initializes the variable, states the condition as a value for the variable and appends every time the variable does not meet the conditions. It will stop when the conditions are met. The important aspect of the `for` loop is that semicolons (;) separate the parameters inside it, not commas (,). 

### question-13
```
let x = 123;
```
The following code segments that  represents a valid `do...while` loop that will terminate (assuming the following code setup) are:
```
do {
   x--;
} while (x > 100);
```
```
do {
   x++;
} while (x < 100);
```
Even though I stated that the 1st algorithm is correct, the second one is also as you can append values for x until `x < 100`. These algorithms satisfy the stated conditions.

### question-14
The primary difference between a `while` loop and `do...while` loop is that a `while` loop check its condition before running the loop body, whereas a `do...while` loop checks its condition after running the loop body. This is true as the format of a `do...while` is set up to run before checking its conditions while a `while` loop is the opposite.

## quiz-6

### question-3
```
let product = multiply(5, 4, 5);
```
The following that could be a possibly declaration and implementation of the multiply function are:
```
function multiply(x, y, z) {
    let product = x * y * z;

    return product;
}
```
```
function multiply(x, y, z) {
    return x * y * z;
}
```
```
function multiply(a, b, c, d) {
    if (a !=== undefined && b !== undefined && c !== undefined && d !== undefined) {
        return a * b * c * d;
    else if (a !=== undefined && b !== undefined && c !== undefined) {
        return a * b * c;
    } else if (a !=== undefined && b !== undefined) {
        return a * b;
    } else if (a !=== undefined) {
        return a;
    }
}
```
What all of these functions have in common are that they all multiply the values `(5, 4, 5)`. in different abstractions. The 2nd option the least complex, the 1st option is the second most complex, while the last option is the most complex.

### question-4
If I pass in more arguments than there are parameters in the function definition the extra arguments will be ignored. This is true as the program goes from left to right, so once it encounters the values they need, it will not need to continue finding more arguments.

### question-6
These built-in functions accept parameters:
```
console.log
```

```
prompt

```
```
alert
```
All of these functions require parameters to display on the console or to the user. They would not be used as intended if they could not accept parameters.

### question-7
```
function divide() {
    let a = Number(prompt("Enter a number."));
    let b = Number(prompt("Enter another number."));

    return a / b;
}
```
"I want to modify the function so that it accepts the parameters as values being divided. The revision that achieves this is 
```
function divide(a, b) {
    return a / b;
}
```

This function defines that `a, b` are the variables to be used in the function and allows the programmer to return the values by dividing them. The values will most likely be displayed.

### question-8
```
function doSomeStuff(a, b, c) {
   console.log("I need to do " + a + ", " + b + ", and " + c + "... So busy!");
}

doSomeStuff("homework", "chores", "more homework");
doSomeStuff("chores", "homework");
doSomeStuff("homework", "homework", "more homework", "oh, and chores, too");
```
The statements that will be logged to the console are:
```
 I need to do homework, homework, and more homework... So busy!
```
```
I need to do chores, homework, and undefined... So busy!
```
```
I need to do homework, chores, and more homework... So busy!
```

All of the outputs correlate the inputs and display in the correct order and even when `undefined` it displays. You just have to determine the order of the inputs for the outputs.

### question-10
"Consider the following function, for which the implementation details are not shown."
```
function mystery() {
    /* implementation details not shown */
}
```
What you can determine based on the information provided is The name of the function is `mystery`and The function is not designed to accept any parameters. You can tell that the function is not designed to return a value as there are no parameters by the function name `mystery`.

### question-12
```
function example() {       // line 1
    let x = 1;             // line 2
                           // line 3
    if (x === 1) {         // line 4
        let y = 2;         // line 5
                           // line 6
        console.log(x);    // line 7
    }                      // line 8
                           // line 9
    console.log(y);        // line 10
}                          // line 11
```
The result of executing this code snippet is that a ReferenceError will occur on line 10. This will occur as y was declared as 2 in the `if` statement with `let` to declare it. Therefore outside the `if` statement, `y` does not exist. If `y` was declared with `var`, then a ReferenceError would not occur.

### question-13

"A variable declared inside of an if statement can only be referenced from within that same scope."

(What is the accuracy of the above statement?)

This is true for variables declared using `const` and `let`. If you used `var` than the variables would go through a global scope.

## quiz-7

### question-7
```
// assume an array named numbers has been initialized with:
//     [ 2, 4, 6, 10, 8, 12 ]

let a = numbers[3];
numbers[3] = numbers[4]
numbers[4] = a;
```

The result of executing this code segment is that 10 and 8 are swapped in placed in the array. 10 was temporarily placed in the `a` variable while 8 now turned into 10. The position where 10 previously was, is now replaced by the `a` variable.

### question-10
"Consider the following code segment, which is designed to determine the largest value in an array of integers."
```
function getLargest(integers) {
    let largest = 0;

    for (let integer of integers) {
        if (integer > largest) {
            largest = integer;
        }
    }

    return largest;
}
```
The following sets of test data demonstrates that `getLargest` does not work as intended is:
```
[ -9, -1, -8, -2, -7, -3, -6, -4, -5 ]
```

The `for...of` assumes that the array is already in order, however, the order of the array puts the lowest value then the highest. This pattern continues through the rest of the array. This proves that `getLargest` does not work as intended.

### question-11
"Consider the following code segment."
```
let tripleDigits = numbers.every(function(num) {
   return num >= 100 && num <= 999;
});
```
"Assuming numbers has been declared and initialized as shown below, what will be the value of tripleDigits after executing this code?"
```
let numbers = [ 101, 202, 303, 4444, 505, 606, 707 ];
```
The line above is true. First `every` means that it checks that all elements of an array to pass a test implemented by the provided function. The value `4444` is < 999 so it is included in the array.
 
### question-12
I have the following array declaration and initialization.
```
let numbers = [ 2, 4, 6 ];
```
I want to add `8`, `10`, and `12` to the array. The following will achieve that:
```
numbers[3] = 8;
numbers[4] = 10;
numbers[5] = 12;
```
```
numbers.push(8);
numbers.push(10);
numbers.push(12);
```
```
numbers.push(8, 10, 12);
```
In addition to the first two options, `numbers.push(8, 10, 12);` puts `8`, `10` and `12`go at the end of the array. That's why it works.

### question-14
```
let cars = [ "Audi", "BMW", "Mercedes", "Porsche", "Volkswagen" ];
let car = prompt("What kind of car do you drive?");

if (/* missing */) {
    console.log("You drive a German-made car.");
}
```
"The console.log statement should only execute if the user enters a value that exists in the cars array." The following that are possible replacements for `/* missing */` that will achieve this goal.

```
cars.includes(car)
```
```
cars.indexOf(car) !== -1
```
```
cars.lastIndexOf(car) !== -1
```
What all of these lines of code have in common are that they ask if a position for car is found in the order of the array. The lines of code either ask if it is in the array or if it is not something in the array.





 

