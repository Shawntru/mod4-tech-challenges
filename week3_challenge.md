# Problem - The Snail
![Snail](https://media.giphy.com/media/n17GyE4DbZfbO/giphy.gif)
Given an n x n array, write a method that returns the array elements arranged from outermost elements to the middle element, traveling clockwise.

A good way to visualize this is to picture the spiral shell of a snail! 

## JS Example
```js
const arrayMatrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

snail(arrayMatrix) #=> [1, 2, 3, 6, 9, 8, 7, 4, 5]
```

## What assumptions will you make about this problem if you cannot ask any more clarifying questions? What are your reasons for making those assumptions?

- The arrays will always be symmetrical, given n x n. 
- The array elements will be defined
- The arrays will all contain equal lengths

## What are your initial thoughts about this problem? (high level design, 2-3 sentences)

Should be able to collect the length of the first array and determine the dimensions of the total array. We will store the number of passes through the array as well as a reduced array containing the output. If `n` is 3, for example, we will accumulate forward through the array at overall index 0. We will then acc the element at the last index position (n-1) for each array until we reach the array in the overall arrays last index position. Using the reverse() method, this array will then be acc. Process repeats in reverse. 

## How would you identify the elements of this problem?

- [X] Searching of Data
- [X] Sorting of Data
- [ ] Pattern Recognition
- [ ] Build/Navigate a Grid
- [X] Math
- [ ] Language API knowledge
- [ ] Optimization


## Which data structure(s) do you think you'll use? What pros/cons do you see with that choice?


## Write out a few lines of initial pseudocode: (mid-level design, NOT REAL CODE)

## Write out any implementation code OR link to repl

## What is the Big O complexity of your solution?
