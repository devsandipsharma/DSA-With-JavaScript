# Do While Loop 🔄🔄

The `do while loop` allows us to repeatedly execute a block of code as long as a specified condition remains true. Unlike `the while loop`, the `do while loop` guarantees that the code block executes at least once before the condition is checked. This is useful when we need to ensure the code runs at least once and then continue based on the condition.

The `do while loop` executes the code block first and then checks the condition. If the condition is true, the loop continues to execute. If the condition is false, the loop terminates.

```javascript
do {
    // code to be executed
} while (condition);
```

## Assignment Questions

### 1. Factorial Calculation

**Task**: Write a program using only `do while loops` to calculate the `factorial` of a given number `n`.

**Example**:
- **Input**: `n = 4`
- **Output**: `24`

**Solution**: 
To solve this problem, initialize a variable for the factorial result and use a do while loop to multiply the numbers from 1 to n.

```javascript
function factorial(n) {
    let result = 1;
    let i = 1;
    do {
        result *= i;
        i++;
    } while (i <= n);
    return result;
}
```

## Connect with me 🎉🎉

Hey there! I'm Sandeep Sharma, currently deep into learning Data Structures and Algorithms (DSA). If you're interested in connecting, discussing, or sharing insights about DSA and more, feel free to connect with me on LinkedIn. Let's learn and grow together!

[Connect with me on LinkedIn](https://www.linkedin.com/in/devsandeepsharma/)