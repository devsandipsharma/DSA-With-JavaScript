# Subarrays 📋📋

`A subarray` is a contiguous part of `an array`. It can be obtained by selecting a `starting index` and an `ending index` within the `array`. `Subarrays` can vary in `size` from `a single` element to the `entire array`.

## What is a Subarray?

* Definition: `A subarray` is a `contiguous segment` of an `array`. For an `array` arr, a `subarray` can be defined by two indices: `start` and `end`, where `start ≤ end`.

* Example: For the `array [1, 2, 3, 4]`, the subarray from index `1` to `3` is `[2, 3, 4]`.

## Assignment Questions

### 1. Print All Subarrays

**Task**: Print all possible `subarrays` of a given `array`. Each `subarray` should be `printed` on a `new line`.

**Example**:
- **Input**: `[1, 2, 3, 4, 5]`
- **Output**: 
```javascript
>> 1
>> 12
>> 123
>> 1234
>> 12345
>> 2
>> 23
>> 234
>> 2345
>> 3
>> 34
>> 345
>> 4
>> 45
>> 5
```

**Solution**: 
To solve this problem, we will use `nested loops`. The `outer loop` will set the `starting point` of the `subarray`, and the `inner loop` will `generate` and `print` all `subarrays` starting from that point.

```javascript
function printAllSubarrays(arr) {
    for (let start = 0; start < arr.length; start++) {
        let subarray = '';
        for (let end = start; end < arr.length; end++) {
            subarray += arr[end];
            console.log(subarray);
        }
    }
}
```

**Explanation:**

* Outer Loop: Iterates over each possible starting index of the subarray.

* Inner Loop: Constructs the subarray from the current starting index to the end of the array, then prints it.

* Subarray Construction: The subarray string is built by appending elements from the array in each iteration of the inner loop.

### 2. Maximum Sum Subarray

**Task**: Given an `array`, find the `maximum sum` of any `subarray`. `Return` this `maximum sum`.

**Example**:
- **Input**: `[5, 2, -4, -5, 3, -1, 2, 3, 1]`
- **Output**: `8`
- **Reason**: The subarray `[3, -1, 2, 3, 1]` has the maximum sum of `8`.

**Solution**: 
To solve this problem, we use `Kadane's Algorithm`, which maintains the `maximum sum` of the `subarray` ending at the current position and `updates` the global `maximum sum`.

```javascript
function maxSumSubarray(arr) {
    let maxSoFar = arr[0]; // Initialize to the first element
    let maxEndingHere = arr[0]; // Initialize to the first element
    
    for (let i = 1; i < arr.length; i++) {
        // Update the maximum sum of the subarray ending at the current index
        maxEndingHere = Math.max(arr[i], maxEndingHere + arr[i]);
        // Update the global maximum sum
        maxSoFar = Math.max(maxSoFar, maxEndingHere);
    }
    
    return maxSoFar;
}
```

**Explanation:**

* Initialization:

    * maxSoFar: Keeps track of the maximum sum found so far.

    * maxEndingHere: Tracks the maximum sum of the subarray ending at the current index.

* Loop:

    * For each element in the array, decide whether to start a new subarray with the current element or to continue the existing subarray by adding the current element.

    * Update maxEndingHere with the maximum of starting a new subarray or extending the existing one.

    * Update maxSoFar with the maximum of itself or maxEndingHere.

* Return:

    * The function returns maxSoFar, which contains the maximum sum of any subarray.

## Connect with me 🎉🎉

Hey there! I'm Sandeep Sharma, currently deep into learning Data Structures and Algorithms (DSA). If you're interested in connecting, discussing, or sharing insights about DSA and more, feel free to connect with me on LinkedIn. Let's learn and grow together!

[Connect with me on LinkedIn](https://www.linkedin.com/in/devsandeepsharma/)