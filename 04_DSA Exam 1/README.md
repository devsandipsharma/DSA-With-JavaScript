# DSA Exam 1 📊✏️

This exam consisted of 4 questions, each worth 250 marks. Below are the questions, my answers, and the points I received for each question from Sharpner.

## Q. 1 Find the Wealth of the Richest Customer 💰

You are given an `m` `x` `n` integer grid `accounts` where `accounts[i][j]` is the amount of money the `i​​​​​​​​​​​th`​​​​ customer has in the `j​​​​​​​​​​​th`​​​​ bank. Return the wealth that the richest customer has.

A customer's wealth is the amount of money they have in all their bank accounts. The richest customer is the customer that has the maximum wealth.

**Example:**

- **Input** : `accounts = [[1,2,3],[3,2,1]]`

- **Output**: `6`

- **Explanation**: Both customers have a wealth of 6, so the richest customer's wealth is 6.

- **Points Earned**: `250/250`

```javascript
var maximumWealth = function(arr) {
    var i = 0;
    var richestCustomer = 0;
    while (i < arr.length) {
        var j = 0;
        var totalIncome = 0;
        while (j < arr[i].length) {
            totalIncome += arr[i][j];
            j++;
        }
        if (richestCustomer < totalIncome) {
            richestCustomer = totalIncome;
        }
        i++;
    }
    return richestCustomer;
};
```

## Q. 2 Count the Number of Bad Pairs 🔢

Given an `array` of integers nums, write a function to count the number of bad pairs. A pair (i, j) is called bad if `nums[i]` > `nums[j]` and `i` > `j`.

**Example:**

- **Input** : `[1, 2, 3, 1, 2, 3]`

- **Output**: `9`

- **Explanation**: The following pairs are bad: `(0, 3)`, `(0, 4)`, `(0, 5)`, `(1, 3)`, `(1, 4)`, `(1, 5)`, `(2, 3)`, `(2, 4)`, `(2, 5)`.

- **Points Earned**: `250/250`

```javascript
function count_bad_pairs(nums) {
    var badPairs = [];
    for (var i = 0; i < nums.length; i++) {
        for (var j = 0; j < nums.length; j++) {
            if (nums[i] > nums[j] && i > j) {
                badPairs.push(nums[j]);
            }
        }
    }
    return badPairs.length;
}
```

## Q. 3 Find the Missing Number for Divisibility by 69 ➗

Write a program to find the `missing number` that when `added` to a `given number` makes it `divisible by 69`.

**Example:**

- **Input** : `69`

- **Output**: `0`

- **Explanation**:  If we add `69` + `0`, it becomes divisible by `69`.

- **Points Earned**: `250/250`

```javascript
function isDivisible(num) {
    var baseValue = 69;
    var outputValue = 0;
    var i = 1;
    var flag = Math.floor(Math.sqrt(num));

    if (num <= baseValue) {
        var newValue = baseValue - num;
        outputValue = newValue;
    }

    while (i < flag) {
        var newValue = i * 69; 
        if (num <= newValue) {
            outputValue = newValue - num;
            break;
        }
        i++;
    }
    return outputValue;
}
```

## Q. 4 Find the Absent Student 🎓

There are `N` students in a classroom. The students who are present are represented by an array `present[]`. One student is absent. Find and return the number of the student who is absent.

**Example:**

- **Input** : `present = [3, 0, 1]`

- **Output**: `2`

- **Explanation**:  Since there are `3` students, all numbers should be in the range `[0, 3]`. The number `2` is missing, so `2` is the absent student.

- **Points Earned**: `250/250`

```javascript
var absent = function (arr) {
    var length = arr.length;
    var actualTotal = 0;
    var expectedTotal = length * (length + 1) / 2;

    for (var i = 0; i < length; i++) {
        actualTotal += arr[i];
    }

    var absentStudent = expectedTotal - actualTotal;

    return absentStudent;
};
```

## Connect with me 🎉🎉

Hey there! I'm Sandeep Sharma, currently deep into learning Data Structures and Algorithms (DSA). If you're interested in connecting, discussing, or sharing insights about DSA and more, feel free to connect with me on LinkedIn. Let's learn and grow together!

[Connect with me on LinkedIn](https://www.linkedin.com/in/devsandeepsharma/)