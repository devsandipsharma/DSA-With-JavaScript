# Variables 🗳🗳

We can think of variables as containers or boxes where we store values. In JavaScript, we use the var, let, and const keywords to create variables.

## How to Create Variables

Creating variables in JavaScript is straightforward. We just need to give the variable a name and assign a value to it. A variable can store various types of values, such as numbers, booleans, strings, objects, and arrays.

```javascript
var name = "values";
```

## When to Use var, let, and const

* var: Used for variables that can be re-declared and updated within their scope. However, it's generally less common in modern JavaScript due to potential issues with scope.

* let: Ideal for variables that may need to be updated but not re-declared within the same scope. It has block scope, meaning it's only available within the block it was defined in.

* const: Best for variables that should not change once assigned. It also has block scope, like let.

## Assignment Questions

### 1. Add Two Variables

**Task**: Write a program to add two variables, `a` and `b`. The values of `a` and `b` will be provided by the user, and your task is to display the sum.

**Example**:
- **Input**: `a = 3`, `b = 4`
- **Output**: `7`

**Solution**: 
To solve this problem, we can create a variable named `result` and use the `+` operator to add the values of `a` and `b`. Finally, we can log the result to the console.

```javascript
function add(a, b) {
    var result = a + b;
    console.log(result);
}
```

### 2. Swap Two Variables a and b

**Task**: Write a program to Swap two Variables a and b (Swapping basically means interchanging)

**Example**:
- **Input**: `a = 3`, `b = 4`
- **Output**: `a = 4`, `b = 3`

**Solution**: 
To solve this problem, we can create a `temp` variable to temporarily hold the value of `a`. Then, we assign the value of `b` to `a`, and finally, assign the value stored in `temp` to `b`.

```javascript
function swap(a, b){
    var temp = a;
    a = b;
    b = temp;

    console.log('a value is =', a);
    console.log('b value is =', b);
}
```

## Connect with me 🎉🎉

Hey there! I'm Sandeep Sharma, currently deep into learning Data Structures and Algorithms (DSA). If you're interested in connecting, discussing, or sharing insights about DSA and more, feel free to connect with me on LinkedIn. Let's learn and grow together!

[Connect with me on LinkedIn](https://www.linkedin.com/in/devsandeepsharma/)