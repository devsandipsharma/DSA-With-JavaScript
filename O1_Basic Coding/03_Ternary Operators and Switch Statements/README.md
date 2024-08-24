# Ternary Operators and Switch Statements ⚖️⚖️

Here, we learn about Ternary Operators and Switch Statements.

## Ternary Operators

Ternary operators provide a shorthand way to write simple `if-else statements`. They are useful for making concise decisions within expressions.

The syntax for a ternary operator is:

```javascript
condition ? expressionIfTrue : expressionIfFalse;
```

## Switch Statements

The switch statement allows us to handle multiple conditions by comparing the same expression to different values. It’s useful when we have a single expression that needs to be evaluated against various possible values.

The syntax for a switch statement is:

```javascript
switch (expression) {
    case value1:
        // code to be executed if expression === value1
        break;
    case value2:
        // code to be executed if expression === value2
        break;
    default:
        // code to be executed if expression doesn't match any case
}
```

## Assignment Questions

### 1. Find the Largest of Two Numbers using Ternary Operators

**Task**: Write a program to print the largest of the two given numbers using a `ternary operator`.

**Example**:
- **Input**: `a = 3, b = 4`
- **Output**: `4`

**Solution**: 
To solve this problem using the ternary operator, compare the two numbers `a` and `b` in `a` single line and print the larger number.

```javascript
function findLargest(a, b) {
    console.log(a > b ? a : b);
}
```

### 2. Print Day Name Using Switch Statement

**Task**: Given the day number, print the day name in lowercase corresponding to it using a `switch statement`. If the day number is not valid (i.e., not between 1 and 7), print "invalid".

**Example**:
- **Input**: `Day - 3`
- **Output**: `wednesday`

**Solution**: 
To solve this problem, use a `switch statement` to handle each day number and print the corresponding day name. Include a `default` case to handle invalid day numbers.

```javascript
function printDayName(day) {
    switch (day) {
        case 1:
            console.log("monday");
            break;
        case 2:
            console.log("tuesday");
            break;
        case 3:
            console.log("wednesday");
            break;
        case 4:
            console.log("thursday");
            break;
        case 5:
            console.log("friday");
            break;
        case 6:
            console.log("saturday");
            break;
        case 7:
            console.log("sunday");
            break;
        default:
            console.log("invalid");
    }
}
```

## Connect with me 🎉🎉

Hey there! I'm Sandeep Sharma, currently deep into learning Data Structures and Algorithms (DSA). If you're interested in connecting, discussing, or sharing insights about DSA and more, feel free to connect with me on LinkedIn. Let's learn and grow together!

[Connect with me on LinkedIn](https://www.linkedin.com/in/devsandeepsharma/)