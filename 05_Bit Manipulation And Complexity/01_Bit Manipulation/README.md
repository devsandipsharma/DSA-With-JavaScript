# Bit Manipulation 🧩💻

`Bit manipulation` involves performing operations on the binary representations of numbers. It’s a powerful technique for optimizing performance and solving problems efficiently by working directly with bits.

## Convert Decimal to Binary

To convert a `decimal number` to `binary`, repeatedly divide the number by `2` and record the `remainder`. The `binary representation` is the `sequence of remainders` read in `reverse order`.

- **Example**:

    - **Decimal**: `13`

    - **Binary**: `1101`

- **Explanation:**
    ```
    >> 13 ÷ 2 = 6, remainder = 1
    >> 6 ÷ 2 = 3, remainder = 0
    >> 3 ÷ 2 = 1, remainder = 1
    >> 1 ÷ 2 = 0, remainder = 1
    ```
Read the remainders from bottom to top: `1101`.

## Convert Binary to Decimal

To convert a `binary number` to its `decimal form`, we can `multiply each bit by 2` raised to the `power of its position` and then `sum the results`.

- **Example:**

    * **Binary**: `1010`

    * **Decimal**: `10`

- **Explanation** : 
    ```
    >> 1 * 2^3 + 0 * 2^2 + 1 * 2^1 + 0 * 2^0
    >> 8 + 0 + 2 + 0
    >> 10
    ```

## Binary Arithmetic

### Addition of Binary Numbers

Adding `binary numbers` follows the same principle as decimal addition, but it carries over `1` whenever the sum of two bits exceeds `1`.

- **Example:**

    - **Binary Addition**: `1011` + `1101`

    - **Steps**:
        ```
        >> 1 + 1 = 0 (carry 1)
        >> 1 + 0 + 1 = 0 (carry 1)
        >> 0 + 1 + 1 = 0 (carry 1)
        >> 1 + 1 = 1 (carry 1)
        >> Result : 11000
        ```

### Subtraction of Binary Numbers

`Binary subtraction` can be efficiently performed using the `2's` complement method. This method is a clever way to handle subtraction by converting the number to be subtracted (the subtrahend) into its `2's` complement form and then adding it to the number we are subtracting from (the minuend).

- **Example:** Subtract `5` `(0101₂)` from `12` `(1100₂)`

- **Steps:**

    * Find the `1’s` complement of the subtrahend `(5)`:

        * Subtrahend: 0101₂

        * 1’s Complement: 1010₂

    * Add 1 to get the 2’s complement:

        * 1010₂ + 1₂ = 1011₂

    * Add the 2’s complement of the subtrahend to the minuend:

        * Minuend: 1100₂

        * 2’s Complement: 1011₂

        * 1100₂ + 1011₂ = 10111₂

    * Result:

        * Ignore the carry (leftmost 1), leaving the result as 0111₂.

    * Convert the result back to decimal:

        * 0111₂ = 7
        
        * So, 12 - 5 = 7 using binary subtraction with 2's complement.

## Bitwise Operators

`Bitwise operators` perform operations directly on the `binary representations` of numbers. These include:

### AND (&) 

The `AND operator` compares each bit of two numbers and returns 1 if both bits are `1`; otherwise, it returns `0`.

- **Example:**

    ```javascript
    let a = 5;  // Binary: 0101
    let b = 3;  // Binary: 0011

    let result = a & b;  // Result: 0001 (Decimal: 1)
    ```

### OR (|)

The `OR operator` compares each bit of two numbers and returns `1` if at least one of the bits is `1`; otherwise, it returns `0`.

- **Example:**

    ```javascript
    let a = 5;  // Binary: 0101
    let b = 3;  // Binary: 0011

    let result = a | b;  // Result: 0111 (Decimal: 7)
    ```

### XOR (^)
The `XOR operator` compares each bit of two numbers and returns `1` if the bits are different, and `0` if they are the same.

- **Example:**

    ```javascript
    let a = 5;  // Binary: 0101
    let b = 3;  // Binary: 0011

    let result = a ^ b;  // Result: 0110 (Decimal: 6)
    ```

### NOT (~)

The `NOT operator` inverts each bit of the number, turning `1s` into `0s` and `0s` into `1s`. This operation returns the two's complement of the number.

- **Example:**

    ```javascript
    let a = 5;  // Binary: 0101

    let result = ~a;  // Result: 1010 (Decimal: -6)
    ```

### LEFT SHIFT (<<)

The `LEFT SHIFT` operator shifts the bits of a number to the left by a specified number of positions, filling the vacant positions with `0s`.

- **Example:**

    ```javascript
    let a = 5;  // Binary: 0101

    let result = a << 1;  // Result: 1010 (Decimal: 10)
    ```

### RIGHT SHIFT (>>)
The `RIGHT SHIFT` operator shifts the bits of a number to the right by a specified number of positions.

- **Example:**

    ```javascript
    let a = 5;  // Binary: 0101

    let result = a >> 1;  // Result: 0010 (Decimal: 2)
    ```

## Assignment Questions

### 1. Find Odd and Even Numbers

**Task**: Write a program to determine if `numbers` in an `array` are `odd` or `even` using bit manipulation.

**Example**:
- **Input**: `[4, 3, 2, 5, 1]`
- **Output**: `[4, 2]` for even numbers and `[3, 5, 1]` for odd numbers

**Solution**: 
To solve this problem using bit manipulation, we will use the bitwise `AND operator (&)` to check if a number is odd or even. The least significant bit of an integer determines if it is odd or even. If the least significant bit is `1`, the number is odd; if it is `0`, the number is even.

```javascript
function findOddEvenNumbers(arr) {
    var evenNumbers = [];
    var oddNumbers = [];
    
    for (var i = 0; i < arr.length; i++) {
        // Use bitwise AND with 1 to check if the number is odd
        if (arr[i] & 1) {
            oddNumbers.push(arr[i]); // Number is odd
        } else {
            evenNumbers.push(arr[i]); // Number is even
        }
    }
    
    console.log("Even Numbers:", evenNumbers);
    console.log("Odd Numbers:", oddNumbers);
}
```

### 2. Swap Two Numbers

**Task**: Write a program to `swap two numbers` using bit manipulation.

**Example**:
- **Input**: `a = 5, b = 9`
- **Output**: `a = 9, b = 5` 

**Solution**: 
To swap two numbers using bit manipulation, we can use the `XOR bitwise operator (^)`. `XOR` can be used to swap values without needing a temporary variable.

```javascript
function swapNumbers(a, b) {
    // Print initial values
    console.log("a = " + a + ", b = " + b);
    
    // Step 1: XOR a and b and store in a
    a = a ^ b;
    
    // Step 2: XOR the result with b to get the original value of a
    b = a ^ b;
    
    // Step 3: XOR the result with the new value of b to get the original value of b
    a = a ^ b;
    
    // Print swapped values
    console.log("a = " + a + ", b = " + b);
}
```

## Connect with me 🎉🎉

Hey there! I'm Sandeep Sharma, currently deep into learning Data Structures and Algorithms (DSA). If you're interested in connecting, discussing, or sharing insights about DSA and more, feel free to connect with me on LinkedIn. Let's learn and grow together!

[Connect with me on LinkedIn](https://www.linkedin.com/in/devsandeepsharma/)