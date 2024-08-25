# For Loop 🔄🔄

The `for loop` is a powerful control structure that allows us to execute a block of code a specific number of times. It is particularly useful when the number of iterations is known beforehand or can be determined before the loop starts.

The `for loop` consists of three parts:

* Initialization: Set up the loop counter.
* Condition: Define the condition that must be true for the loop to continue.
* Update: Modify the loop counter after each iteration.

The syntax for a for loop is:

```javascript
for (initialization; condition; update) {
    // code to be executed
}
```

## Assignment Questions

### 1. Odd Number Series

**Task**: Write a program to print all `odd numbers` from `1` to `n` using `for loops`.

**Example**:
- **Input**: `n = 7`
- **Output**: `1 3 5 7`

**Solution**: 
To solve this problem, use a for loop to iterate from 1 to n, and check if the current number is odd. Print the number if it is odd.

```javascript
function printOddNumbers(n) {
    for (let i = 1; i <= n; i += 2) {
        console.log(i);
    }
}
```

### 2. Series using for Loop

**Task**:  Print the following series using `for loop`:- `1, 8, 27, 64, 125, 216, ...` up to the number `n`.

**Example**:
- **Input**: `n = 125`
- **Output**: `1 8 27 64 125`

**Solution**: 
To solve this problem, we need to print the `cubes` of integers starting from `1` up to `n`. We can use a `for loop` to calculate the `cubes` and print them as long as the cube is less than or equal to `n`.

```javascript
function printSeries(n) {
    let cube = 1;
    for (let i = 1; cube < n; i++) {
        cube = i * i * i;
        console.log(cube);
    }
}
```

## Connect with me 🎉🎉

Hey there! I'm Sandeep Sharma, currently deep into learning Data Structures and Algorithms (DSA). If you're interested in connecting, discussing, or sharing insights about DSA and more, feel free to connect with me on LinkedIn. Let's learn and grow together!

[Connect with me on LinkedIn](https://www.linkedin.com/in/devsandeepsharma/)