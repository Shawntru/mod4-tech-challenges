# Problem - Array Flattener
![recursion](https://media.giphy.com/media/3GuP496Wrkos8/giphy.gif)

Imagine you have a deeply nested array, or multi-dimensional array, like this:

```rb
 array_of_ints = [1, 2, 3, [[4], 5], [[[6]]]]
 array_of_strings = ["hi", "this is", [[["string"], "that is very"], [[[["nested"]]]]]]
```
the contents of the array aren't important.

In Ruby and JS, we have built in methods and functions to `flatten` arrays into one dimension.  For example, in JS:

```js
> arr1
[ 0, 1, 2, [ 3, 4 ] ]
> arr1.flat()
[ 0, 1, 2, 3, 4 ]
```
If we look at the docs for either of these, we notice that they are _recursive_ by nature. Your goal is to recreate this functionality by writing a recursive function to accomplish this same thing. For example:

In JS:

```js
> arr1
  [ 0, 1, 2, [ 3, 4 ] ]
> flatten(arr1)
  [ 0, 1, 2, 3, 4 ]
```

## What assumptions will you make about this problem if you cannot ask any more clarifying questions? What are your reasons for making those assumptions?
- Array elements will always be integers (although this shouldn't affect the solution if they are not)
- These will always be arrays, nested or otherwise

## What are your initial thoughts about this problem? (high level design, 2-3 sentences)
- Using recursion, continuously cycle through the array, removing elements one at a time and pushing them into an accumulator array.

## How would you identify the elements of this problem?

- [x] Searching of Data
- [ ] Sorting of Data
- [ ] Pattern Recognition
- [ ] Build/Navigate a Grid
- [ ] Math
- [ ] Language API knowledge
- [ ] Optimization


## Which data structure(s) do you think you'll use? What pros/cons do you see with that choice?
- Recursion

## Write out a few lines of initial pseudocode: (mid-level design, NOT REAL CODE)

## Write out any implementation code OR link to repl

## What is the Big O complexity of your solution?
