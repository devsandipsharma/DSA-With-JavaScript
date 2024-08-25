# Pattern-Based Questions 🔢🔲

`Pattern-based questions` are a common type of problem in programming that involve `generating` and `printing patterns` based on certain `rules` or `sequences`. They are useful for improving our understanding of `loops` and `control structures`.

## Trick to Solve Any Pattern-Based Question

* Identify the Number of Rows: Determine how many rows the pattern will have. This often corresponds to the outer loop in the pattern generation.

* Identify the Number of Columns and Their Arrangement: Determine how many columns are needed for each row and how they are structured. This helps in setting up the inner loop(s).

* Determine What to Print: Understand what needs to be printed in each row and column. This could be numbers, stars, spaces, or other characters.

* Find the Formula or Relationship Between Rows and Columns: Establish any formula or relationship between the rows and columns to simplify the logic of your loops and printing.

## Assignment Questions

### 1. Simple Square Pattern

**Task**: A `square pattern` where each row contains the same character.

**Example**:
- **Input**: `size = 4`
- **Output**: 
```
> ****
> ****
> ****
> ****
```

**Solution**: 
Use nested `for loops` to print a `square pattern`. The `outer loop` iterates over each `row`, while the `inner loop` generates the characters for each `column`.

```javascript
function printSquare(size) {
    for (var i = 0; i < size; i++) {
        var pattern = "";
        for (var j = 0; j < size; j++) {
            pattern += "*";
        }
        console.log(pattern);
    }
}
```

**Explanation**:

* Rows: The outer loop (i) runs from 0 to size - 1, creating each row of the pattern.
* Columns: The inner loop (j) runs from 0 to size - 1, adding the character * for each column in the row.
* Print: Each completed row pattern is printed after the inner loop finishes.

### 2. Right-Angle Triangle Pattern

**Task**: A `right-angle triangle` where the number of characters increases with each row.

**Example**:
- **Input**: `height = 4`
- **Output**: 
```
> *
> **
> ***
> ****
```

**Solution**: 
Use a `for loop` to iterate through each `row`, and in `each row`, use another `for loop` to print the increasing number of characters.

```javascript
function printRightAngleTriangle(height) {
    for (var i = 1; i <= height; i++) {
        var pattern = "";
        for (var j = 0; j < i; j++) {
            pattern += "*";
        }
        console.log(pattern);
    }
}
```

**Explanation**:

* Rows: The outer loop (i) runs from 1 to height, creating each row of the triangle.
* Columns: The inner loop (j) runs from 0 to i - 1, adding the character * for each column in the current row.
* Print: Each completed row pattern is printed after the inner loop finishes.

### 3. Pyramid Pattern

**Task**: A `pyramid` where the number of characters increases in each `row` and `is centered`.

**Example**:
- **Input**: `height = 4`
- **Output**: 
```
>    *
>   ***
>  *****
> *******
```

**Solution**: 
Use a `for loop` to iterate through each `row`, and within `each row`, use nested `for loops` to print `spaces` and `characters` to achieve the centered effect.

```javascript
function printPyramid(height) {
    for (var i = 1; i <= height; i++) {
        var pattern = "";

        // Print leading spaces
        for (var j = height - i; j > 0; j--) {
            pattern += " ";
        }

        // Print the stars
        for (var k = 0; k < (2 * i - 1); k++) {
            pattern += "*";
        }

        console.log(pattern);
    }
}
```

**Explanation**:

* Rows: The outer loop (i) runs from 1 to height, creating each row of the pyramid.
* Spaces: The first inner loop (j) adds leading spaces before the stars to center the pyramid.
* Stars: The second inner loop (k) adds the * characters, with the number of stars increasing by 2 for each row.
* Print: Each completed row pattern is printed after the inner loop finishes.

### 4. Diamond Pattern

**Task**: A `diamond` where the pattern `grows` and then `shrinks` symmetrically.

**Example**:
- **Input**: `size = 3`
- **Output**: 
```
>   *
>  ***
> *****
>  ***
>   *
```

**Solution**: 
Use nested `for loops` to handle the `growing` and `shrinking` parts of `the diamond`. The `upper half` of the `diamond` `grows` in `width`, and the `lower half` `shrinks symmetrically`.

```javascript
function printPyramid(height) {
    function printDiamond(size) {
    // Upper half of the diamond
    for (var i = 1; i <= size; i++) {
        var pattern = "";

        // Print leading spaces
        for (var j = size - i; j > 0; j--) {
            pattern += " ";
        }

        // Print stars
        for (var k = 0; k < (2 * i - 1); k++) {
            pattern += "*";
        }

        console.log(pattern);
    }

    // Lower half of the diamond
    for (var i = size - 1; i > 0; i--) {
        var pattern = "";

        // Print leading spaces
        for (var j = size - i; j > 0; j--) {
            pattern += " ";
        }

        // Print stars
        for (var k = 0; k < (2 * i - 1); k++) {
            pattern += "*";
        }

        console.log(pattern);
    }
}
}
```

**Explanation**:

* Upper Half:
    * Rows: The first for loop (i) runs from 1 to size, creating each row of the top part of the diamond.
    * Spaces: The first inner loop (j) adds leading spaces to center the stars.
    * Stars: The second inner loop (k) adds the * characters, increasing by 2 for each row.

* Lower Half:
    * Rows: The second for loop (i) runs from size - 1 to 1, creating each row of the bottom part of the diamond.
    * Spaces: The first inner loop (j) adds leading spaces to center the stars.
    * Stars: The second inner loop (k) adds the * characters, decreasing by 2 for each row.
    
* Print: Each completed row pattern is printed after the inner loops finish.

### 5. Hollow Pyramid Star Pattern

**Task**: Create a `hollow pyramid` pattern where the pyramid has stars `*` on the borders and spaces in between. The pattern should be centered and the number of rows determines the height of the pyramid.

**Example**:
- **Input**: `size = 4`
- **Output**: 
```
>    *
>   * *
>  *   *
> *******
```

**Solution**: 
Use nested for loops to handle the pyramid structure, and print * for the borders and spaces in between.

```javascript
function printHollowDiamond(height) {
    for (var i = 1; i <= height; i++) {
        var pattern = "";

        // Add leading spaces
        for (var j = 1; j <= height - i; j++) {
            pattern += " ";
        }

        // Add stars and spaces
        for (var k = 1; k <= 2 * i - 1; k++) {
            if (i === height) {
                pattern += "*"; // Fully filled last row
            } else if (k === 1 || k === 2 * i - 1) {
                pattern += "*"; // Edges of the diamond
            } else {
                pattern += " "; // Hollow center
            }
        }

        console.log(pattern);
    }
}
```

**Explanation**:

* Outer Loop: Iterates through each row of the pyramid from 1 to size.
* Leading Spaces: Added to center the pyramid. The number of spaces decreases as we move down the pyramid (size - i spaces).
* Stars and Spaces:
    * For the last row (i === size), the entire row is filled with *.
    * For other rows, * is printed at the first (k === 1) and last (k === 2 * i - 1) positions, with spaces in between.

## Connect with me 🎉🎉

Hey there! I'm Sandeep Sharma, currently deep into learning Data Structures and Algorithms (DSA). If you're interested in connecting, discussing, or sharing insights about DSA and more, feel free to connect with me on LinkedIn. Let's learn and grow together!

[Connect with me on LinkedIn](https://www.linkedin.com/in/devsandeepsharma/)