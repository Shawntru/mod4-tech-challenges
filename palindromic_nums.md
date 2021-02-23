# Problem - Palindromic Numbers
![Palindrome](https://media.giphy.com/media/xT5LMYqyIPJtjnjiHm/giphy.gif)

The number 47 has an interesting characteristic.

If you take the number, plus its reverse (47 => 74) and then add them together to a number (47+74=121) the resulting sum is a palindrome

Starting at 0, find the first 25 numbers that have this same characteristic as 47, but limit it to where the palindrome is greater than 1000.

Collect the results in an array. Be sure that you're collecting the interesting numbers like 47, not the palindromic sums.

Bonus points if you can do this without converting numbers to strings/arrays.

Limit your online searches to core language documentation only.

## What assumptions will you make about this problem if you cannot ask any more clarifying questions? What are your reasons for making those assumptions?
- Input with always be a numerical value

## What are your initial thoughts about this problem? (high level design, 2-3 sentences)

Break out into several steps:
- Initial number reverse 
- Sum numbers, ensure sum > 1000
- Check sum, if palindrome push origin num to acc array
- Check length of acc array, return if length == 25

## How would you identify the elements of this problem?

- [ ] Searching of Data
- [ ] Sorting of Data
- [ ] Pattern Recognition
- [ ] Build/Navigate a Grid
- [X] Math
- [X] Language API knowledge
- [ ] Optimization


## Which data structure(s) do you think you'll use? What pros/cons do you see with that choice?

- Most likely a reduce(), starting with an initial empty array. then use array iterator methods split(), reverse(), join().

## Write out a few lines of initial pseudocode: (mid-level design, NOT REAL CODE)
```JavaScript
Have: No input
Want: Output a array (length == 25) of numbers whos reversed sum is a palindrome

Create seperate function used to reverse numbers, by calling str/arr methods:
  parseInt(currentNum.split('').reverse().join(), 10)
Declare array for collecting interesting numbers
Declare currentNum variable, starting at 0
Inside a while loop, while interesting numbers arr length is !== 25:
Declare reverseNum by calling reversing function for currentNum
Declare sum variable as currentNum + reverseNum, 
If the sum <= 1000 then return and increment currentNum by 1. 
If sum === reversed sum using the reversing function, 
  push the number into array of interesting numbers
```

## Write out any implementation code OR link to repl
```JavaScript
const findPalindromes = () => {
  let interestingNums = [];
  let currentNum = 0;

  const reverse = (number) => {
    return parseInt(number.toString(10).split('').reverse().join(''), 10);
  }

  while (interestingNums.length !== 25) {
    let sum = currentNum + reverse(currentNum);
    if (sum === reverse(sum) && sum >= 1000) {
      interestingNums.push(currentNum)
    }
    currentNum++;
  }

  return interestingNums;
}
```
[Repl.it Link](https://repl.it/@bearishparrot/AverageLovingOpen64#index.js)
## What is the Big O complexity of your solution?
