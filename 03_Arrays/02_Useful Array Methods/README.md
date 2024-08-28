# Useful Array Methods 🛠️🛠️

`Arrays` in `JavaScript` come with a variety of built-in methods that help in `manipulating` and `accessing array` data efficiently. Below are some of the most commonly used `array methods`:

## 1. push()

* Purpose: `Adds` one or more `elements` to the `end of an array` and `returns` the `new length` of the `array`.

* Syntax: array.push(element1, element2, ...)

```javascript
let arr = [1, 2, 3];
arr.push(4, 5); // [1, 2, 3, 4, 5]
```

## 2. pop()

* Purpose: `Removes` the `last element` from an `array` and `returns that element`.

* Syntax: array.pop()

```javascript
let arr = [1, 2, 3, 4];
let last = arr.pop(); // last = 4, arr = [1, 2, 3]
```

## 3. shift()

* Purpose: `Removes` the `first element` from an `array` and `returns that element`.

* Syntax: array.shift()

```javascript
let arr = [1, 2, 3, 4];
let first = arr.shift(); // first = 1, arr = [2, 3, 4]
```

## 4. unshift()

* Purpose: `Adds` one or more elements to the `beginning of an array` and `returns the new length of the array`.

* Syntax: array.unshift(element1, element2, ...)

```javascript
let arr = [2, 3, 4];
arr.unshift(1); // [1, 2, 3, 4]
```

## 5. concat()

* Purpose: `Merges two or more arrays` into a `new array`.

*Syntax: array.concat(array2, array3, ...)

```javascript
let arr1 = [1, 2];
let arr2 = [3, 4];
let combined = arr1.concat(arr2); // [1, 2, 3, 4]
```

## 6. slice()

* Purpose: `Returns a shallow copy` of a `portion` of an `array` into a `new array` selected from start to end (end not included).

* Syntax: array.slice(start, end)

```javascript
let arr = [1, 2, 3, 4, 5];
let sliced = arr.slice(1, 3); // [2, 3]
```

## 7. splice()

* Purpose: Changes the `contents` of `an array` by `removing` or `replacing` existing `elements` and/or `adding` new elements `in place`.

* Syntax: array.splice(start, deleteCount, item1, item2, ...)

```javascript
let arr = [1, 2, 3, 4];
arr.splice(1, 2, 5, 6); // arr = [1, 5, 6, 4]
```

## 8. find()

* Purpose: `Returns the first element` in the `array` that `satisfies the provided testing` function.

* Syntax: array.find(callback(element, index, array))

```javascript
let arr = [4, 9, 16];
let found = arr.find(x => x > 9); // 16
```

## 9. map()

* Purpose: `Creates a new array` with the `results` of calling a `provided function` on every element in the `array`.

* Syntax: array.map(callback(element, index, array))

```javascript
let arr = [1, 2, 3];
let doubled = arr.map(x => x * 2); // [2, 4, 6]
```

## 10. filter()

* Purpose: `Creates a new array` with `all elements that pass the test` implemented by the provided function.

* Syntax: array.filter(callback(element, index, array))

```javascript
let arr = [1, 2, 3, 4, 5];
let even = arr.filter(x => x % 2 === 0); // [2, 4]
```

## 11. reduce()

* Purpose: `Executes a reducer function` (that you provide) on each `element of the array`, resulting in a `single output value`.

* Syntax: array.reduce(callback(accumulator, currentValue, index, array), initialValue)

```javascript
let arr = [1, 2, 3, 4];
let sum = arr.reduce((acc, curr) => acc + curr, 0); // 10
```

## 12. reverse()

* Purpose: `Reverses` the elements of an `array` in place.

* Syntax: array.reverse()

```javascript
let arr = [1, 2, 3];
arr.reverse(); // [3, 2, 1]
```

## 13. sort()

* Purpose: `Sorts the elements of an array` in place and `returns the sorted array`.

* Syntax: array.sort([compareFunction])

```javascript
let arr = [3, 1, 2];
arr.sort(); // [1, 2, 3]
```

## Connect with me 🎉🎉

Hey there! I'm Sandeep Sharma, currently deep into learning Data Structures and Algorithms (DSA). If you're interested in connecting, discussing, or sharing insights about DSA and more, feel free to connect with me on LinkedIn. Let's learn and grow together!

[Connect with me on LinkedIn](https://www.linkedin.com/in/devsandeepsharma/)