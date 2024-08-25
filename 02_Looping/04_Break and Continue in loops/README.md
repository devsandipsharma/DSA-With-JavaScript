# Break and Continue in Loops 🔄🔄

In JavaScript, `break` and `continue` are control flow statements that can be used to `alter the execution flow within loops`. Understanding how to use these statements effectively allows for more flexible and controlled `looping`.

## Break Statement

The `break statement` is used to terminate the nearest enclosing loop or `switch statement`. When a `break statement` is encountered, the `loop` or `switch statement` is immediately exited, and control is transferred to the statement following the `loop` or `switch`.

```javascript
for (initialization; condition; update) {
    // code to be executed
    if (conditionToBreak) {
        break;
    }
    // more code
}
```

## Continue Statement

The `continue statement` is used to `skip the current iteration` of a `loop` and proceed to the `next iteration`. When a `continue statement` is encountered, the rest of the code inside the `loop` for the current iteration is skipped, and control is transferred to the `loop’s condition check` for the next iteration.

```javascript
for (initialization; condition; update) {
    // code to be executed
    if (conditionToContinue) {
        continue;
    }
    // more code
}
```

## Assignment Questions

### 1. Program to Print Numbers and Stop at m

**Task**: Write a program to print all numbers from `1` to `n`. If `m` is present in the sequence, stop printing any other numbers and `break` out of the `loop`.

**Example**:
- **Input**: `n = 10`, `m = 4`
- **Output**: `1 2 3`

**Solution**: 
Use a `for loop` to iterate from `1` to `n`. Check if the current number equals `m`. If it does, use the `break statement` to exit the `loop` and stop printing further numbers.

```javascript
function printNumbersUntil(m, n) {
    for (let i = 1; i <= n; i++) {
        if (i === m) {
            break;
        }
        console.log(i);
    }
}
```

### 2. Program to Print Even Numbers Skipping Multiples of 4

**Task**: Write a program to print even numbers from `1` to `n`, skipping any numbers that are divisible by `4`. Use `the continue statement` to skip printing those numbers.

**Example**:
- **Input**: `n = 10`
- **Output**: `2 6 10`

**Solution**: 
Use a `for loop` to iterate from `1` to `n`. Check if the number is even and not divisible by 4. Use `the continue statement` to skip the number if it is divisible by `4`.

```javascript
function printEvenNumbersSkippingMultiplesOfFour(n) {
    for (let i = 1; i <= n; i++) {
        if (i % 2 !== 0) {
            continue;
        }
        if (i % 4 === 0) {
            continue;
        }
        console.log(i);
    }
}
```

## Connect with me 🎉🎉

Hey there! I'm Sandeep Sharma, currently deep into learning Data Structures and Algorithms (DSA). If you're interested in connecting, discussing, or sharing insights about DSA and more, feel free to connect with me on LinkedIn. Let's learn and grow together!

[Connect with me on LinkedIn](https://www.linkedin.com/in/devsandeepsharma/)