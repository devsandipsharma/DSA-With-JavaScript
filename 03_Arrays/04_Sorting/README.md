# Sorting Algorithms 🔄🔄

`Sorting` is a `fundamental` operation in `computer science`, where the `elements` of a `list` or `array` are `arranged` in a `specific order`, usually in `ascending` or `descending order`. `Sorting algorithms` are `key` to `optimizing data processing` and are often used in `searching`, `data analysis`, and `various applications`.

## Common Sorting Algorithms

### 1. Bubble Sort 🫧

* Concept: `Repeatedly compares` adjacent `elements` and `swaps` them if they are in the wrong order.

* Use Case: `Simple to implement` but `inefficient` for large datasets.

### 2. Selection Sort 🔍

* Concept: `Selects the smallest (or largest)` element from the `unsorted part` of the `array` and `swaps` it with the first unsorted element.

* Use Case: `More predictable` than `Bubble Sort` but still `inefficient` for large arrays.

### 3. Insertion Sort 📝

* Concept: Builds the final `sorted array` one `element` at a `time by repeatedly inserting` the `next element` into its `correct position`.

* Use Case: `Efficient for small datasets` or nearly `sorted data`.


## Assignment Questions

### 1. Sort the Array Using Bubble Sort

**Task**: Write a program to `sort an array` in `descending order` using the `Bubble Sort` algorithm. After `sorting, return the array`.

**Example**:
- **Input**: `[4, 3, 2, 5, 1]`
- **Output**: `[5, 4, 3, 2, 1]`

**Solution**: 
To solve this problem, we use the `Bubble Sort` algorithm, where we `repeatedly compare` adjacent `elements and swap them` if they are in the `wrong order` (for descending order, swap if the first element is smaller than the second).

```javascript
function bubbleSortDescending(arr) {
    let n = arr.length;
    for (let i = 0; i < n - 1; i++) {
        for (let j = 0; j < n - i - 1; j++) {
            // Swap if the current element is smaller than the next element
            if (arr[j] < arr[j + 1]) {
                let temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
    return arr;
}
```

**Explanation:**

* Outer Loop: Runs n-1 times where n is the length of the array. Each pass through the array places the next largest element in its correct position.

* Inner Loop: Compares each pair of adjacent elements. If the current element is smaller than the next, they are swapped.

* Descending Order: The algorithm sorts in descending order by swapping when the current element is smaller than the next one.

### 2. Sort the Array Using Insertion Sort

**Task**: Write a program to `sort an array` in `ascending order` using the `Insertion Sort` algorithm. After sorting, `return the array`.

**Example**:
- **Input**: `[4, 3, 2, 5, 1]`
- **Output**: `[1, 2, 3, 4, 5]`

**Solution**: 
To solve this problem, we use the `Insertion Sort` algorithm, which `builds the sorted array` one `element at a time` by `repeatedly inserting` the next `element` into its `correct position`.

```javascript
function insertionSortAscending(arr) {
    for (let i = 1; i < arr.length; i++) {
        let key = arr[i]; // The element to be positioned
        let j = i - 1;
        
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key; // Insert the key into its correct position
    }
    return arr;
}
```

**Explanation:**

* Outer Loop: Starts from the second element and goes through each element in the array.

* Key: The current element (at index i) that needs to be inserted into the sorted portion of the array (from index 0 to i-1).

* Inner Loop: Shifts elements that are greater than the key one position to the right to make space for inserting the key into its correct position.

* Insertion: After shifting elements, the key is inserted at its correct position in the sorted portion of the array.

### 3. Sort the Array Using Selection Sort

**Task**: Write a program to `sort an array` in `descending order` using the `Selection Sort` algorithm. After sorting, `return the array`.

**Example**:
- **Input**: `[4, 3, 2, 5, 1]`
- **Output**: `[5, 4, 3, 2, 1]`

**Solution**: 
To solve this problem, we use the `Selection Sort` algorithm, where we `repeatedly find the maximum element` from the `unsorted portion` of the `array` and `swap` it with the `first unsorted element`.

```javascript
function selectionSortDescending(arr) {
    let n = arr.length;

    for (let i = 0; i < n - 1; i++) {
        // Find the index of the maximum element in the unsorted part
        let maxIndex = i;
        for (let j = i + 1; j < n; j++) {
            if (arr[j] > arr[maxIndex]) {
                maxIndex = j;
            }
        }

        // Swap the found maximum element with the first unsorted element
        if (maxIndex !== i) {
            let temp = arr[i];
            arr[i] = arr[maxIndex];
            arr[maxIndex] = temp;
        }
    }

    return arr;
}
```

**Explanation:**

* Outer Loop: Iterates through each element of the array, treating the portion of the array after the current index as unsorted.

* Find Maximum: The inner loop finds the maximum element in the unsorted portion of the array.

* Swap: The maximum element is swapped with the first element of the unsorted portion, placing it in its correct position for descending order.

* Descending Order: The array is sorted in descending order by repeatedly placing the largest remaining element at the beginning of the unsorted portion.

## Connect with me 🎉🎉

Hey there! I'm Sandeep Sharma, currently deep into learning Data Structures and Algorithms (DSA). If you're interested in connecting, discussing, or sharing insights about DSA and more, feel free to connect with me on LinkedIn. Let's learn and grow together!

[Connect with me on LinkedIn](https://www.linkedin.com/in/devsandeepsharma/)