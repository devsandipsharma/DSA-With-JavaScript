# Conditional Statement ⚖️⚖️

Conditional statements allow us to make decisions in our code based on certain conditions. They enable our programs to execute different code paths depending on whether a condition is true or false. In JavaScript, the most common conditional statements are `if`, `else if`, and `else`.

## Basic if Statement

The `if` statement is used to execute a block of code only if a specified condition is true.

```javascript
if (condition) {
    // code to be executed if the condition is true
}
```

## else Statement
The `else` statement specifies a block of code that will be executed if the condition in the if statement is false.

```javascript
if (condition) {
    // code to be executed if the condition is true
} else {
    // code to be executed if the condition is false
}
```

## else if Statement
The `else if` statement allows us to check multiple conditions. If the first condition is false, it checks the next one, and so on.

```javascript
if (condition1) {
    // code to be executed if condition1 is true
} else if (condition2) {
    // code to be executed if condition2 is true
} else {
    // code to be executed if none of the conditions are true
}
```

## Assignment Questions

### 1. Find the magical number

**Task**: The number is said to be magical if it is greater than 10. If n is greater than 10 print "magical"

**Example**:
- **Input**: `15`
- **Output**: `magical`

**Solution**: 
To solve this problem, use a simple if statement to check if the number n is greater than 10. If the condition is true, the program will output the string "magical". This involves comparing the value of n to 10 and printing the result based on that comparison. 

```javascript
function checkMagicalEnergy(n) {
    if (n > 10) {
        console.log("magical")
    }
}
```

### 2. Largest among 2 numbers

**Task**: Write a program to print the largest number of the two numbers given.

**Example**:
- **Input**: `a = 3`, `b = 4`
- **Output**: `4`

**Solution**: 
To solve this problem, we can use an if-else statement to compare the two numbers. If `a` is greater than `b`, we can print `a` otherwise we can print `b`.

```javascript
function max(a, b){
    if (a > b) {
        console.log(a)
    } else {
        console.log(b)
    }
}
```

## Connect with me 🎉🎉

Hey there! I'm Sandeep Sharma, currently deep into learning Data Structures and Algorithms (DSA). If you're interested in connecting, discussing, or sharing insights about DSA and more, feel free to connect with me on LinkedIn. Let's learn and grow together!

[Connect with me on LinkedIn](https://www.linkedin.com/in/devsandeepsharma/)