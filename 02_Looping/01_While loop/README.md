# While loop 🔄🔄

The `while loop` allows us to repeatedly execute a block of code as long as a specified condition remains true. This type of loop is particularly useful when the `number of iterations isn't known` beforehand and needs to be determined dynamically during runtime.

The `while loop` checks the condition before executing the block of code. If the condition is true, the loop continues to execute until the condition becomes false.

```javascript
while (condition) {
    // code to be executed as long as the condition is true
}
```

## Assignment Questions

### 1. Find Even Numbers

**Task**: Write a program using only `while loops` to print all the even numbers from `1` to `n`.

**Example**:
- **Input**: `n = 10`
- **Output**: `2 4 6 8 10`

**Solution**: 
To solve this problem, we'll start with the number 2 (the smallest even number) and increment by 2 each time using a while loop until we reach or exceed the value of n.

```javascript
function printEvenNumbers(n) {
    let i = 2;
    while (i <= n) {
        console.log(i);
        i += 2;
    }
}
```

### 2. Armstrong number

**Task**: Write a program to print whether a given number is an `Armstrong number or not`..

**Example**:
- **Input**: `n = 153`
- **Output**: `true`

**Solution**: 
An Armstrong number (also known as a narcissistic number) is a number that is equal to the sum of its own digits each raised to the power of the number of digits.

For example, 153 is an Armstrong number because:
```
> 1 * 1 * 1 + 5 * 5 * 5 + 3 * 3 * 3
> 1 + 125 + 27
> 153
```

We can solve this by calculating the sum of the digits, each raised to the power of three (since we’re dealing with a three-digit number), and then comparing this sum to the original number.

```javascript
function isArmstrongNumber(n) {
    let sum = 0;
    let temp = n;

    while (temp > 0) {
        let digit = temp % 10;
        sum += digit * digit * digit;
        temp = Math.floor(temp / 10);
    }

    return sum === n;
}
```

## Connect with me 🎉🎉

Hey there! I'm Sandeep Sharma, currently deep into learning Data Structures and Algorithms (DSA). If you're interested in connecting, discussing, or sharing insights about DSA and more, feel free to connect with me on LinkedIn. Let's learn and grow together!

[Connect with me on LinkedIn](https://www.linkedin.com/in/devsandeepsharma/)