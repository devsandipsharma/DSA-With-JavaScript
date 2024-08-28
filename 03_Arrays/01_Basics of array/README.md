# Basics of Arrays 🧩🧩

`Arrays` are a fundamental data structure used to store multiple elements in a single variable. They are ordered collections where each element is accessible via an `index`.

## Creating Arrays

`Arrays` can be created using `square brackets []` or the `Array constructor`.

```javascript
let arr = [1, 2, 3, 4, 5]; // Using array literal
let arr2 = new Array(10); // Using the Array constructor (creates an array with 10 empty slots)
```

## Accessing Array Elements
Elements in an `array` are accessed using their ``index, with indexing starting at `0`.

```javascript
let firstElement = arr[0]; // Accesses the first element (1)
arr[2] = 10; // Modifies the third element (now the array is [1, 2, 10, 4, 5])
```

## Array Operations

Common operations include `adding`, `removing`, and `modifying` elements.

* Adding Elements:

    * push(): `Adds` an element to the `end of the array`.

        ```javascript
        arr.push(6); // [1, 2, 10, 4, 5, 6]
        ```
    * unshift(): `Adds` an element to the `beginning of the array`.

        ```javascript
        arr.unshift(0); // [0, 1, 2, 10, 4, 5]
        ```

* Removing Elements:

    * pop(): `Removes` the `last element`.

        ```javascript
        arr.pop(); // [1, 2, 10, 4, 5]
        ```
    * shift(): `Removes` the `first element`.

        ```javascript
        arr.shift(); // [1, 2, 10, 4, 5]
        ```

## Find Array Length

The `length` property indicates the number of elements in an array.

```javascript
let length = arr.length; // 5
arr.length = 3; // Trims the array to [1, 2, 10]
```

## Assignment Questions

### 1. Storing Elements in Array

**Task**: Write a program to `declare an array` of `size n` and store the numbers `1`,`2`,`3`,`4` ...`n` in the `array` and `return` the `array`.

**Example**:
- **Input**: `n = 10`
- **Output**: `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`

**Solution**: 
To solve this problem, we will `initialize an empty array` and `use a for loop` to `store numbers` from 1 to n in the `array`.

```javascript
function storeElementsInArray(n) {
    let arr = [];
    for (let i = 1; i <= n; i++) {
        arr.push(i);
    }
    return arr;
}
```

### 2. Maximum in an Array

**Task**: Given an `array` find the `maximum` in it and `return it`. 

**Example**:
- **Input**: `let arr = [5, 4, 7, 2, 6]`
- **Output**: `7`

**Solution**: 
To solve this problem, we can `iterate` through the `array` using a `for loop` and keep track of the `maximum` value found.

```javascript
function findMaximum(arr) {
    let max = arr[0]; // Assume the first element is the maximum
    for (let i = 1; i < arr.length; i++) {
        if (arr[i] > max) {
            max = arr[i]; // Update max if the current element is greater
        }
    }
    return max;
}
```

### 3. Store Prime numbers in an array

**Task**: Write a program to store first `n` `prime numbers` in an `array`. After `storing` `return` the `array`.

**Example**:
- **Input**: `n = 5`
- **Output**: `2, 3, 5, 7, 11`

**Solution**: 
To solve this problem, we need to `check numbers sequentially` to determine if they are `prime` and `store` them in an `array` until we have `n` `prime numbers`.

```javascript
function isPrime(num) {
    if (num <= 1) return false;
    for (let i = 2; i <= Math.sqrt(num); i++) {
        if (num % i === 0) return false;
    }
    return true;
}

function storePrimeNumbers(n) {
    let primes = [];
    let num = 2; // Start with the first prime number
    while (primes.length < n) {
        if (isPrime(num)) {
            primes.push(num); // Add prime number to the array
        }
        num++; // Check the next number
    }
    return primes;
}
```

## Connect with me 🎉🎉

Hey there! I'm Sandeep Sharma, currently deep into learning Data Structures and Algorithms (DSA). If you're interested in connecting, discussing, or sharing insights about DSA and more, feel free to connect with me on LinkedIn. Let's learn and grow together!

[Connect with me on LinkedIn](https://www.linkedin.com/in/devsandeepsharma/)