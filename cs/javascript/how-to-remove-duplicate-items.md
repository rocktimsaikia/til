# How to remove duplicate items from an array in JS?

```js
const arr = [1,2,2,1,3,4,5]

// 1. Converting to array with spread operator `...`
const newArr = [...new Set(arr)]

// 2. Converting to array with `Array.from`
const newArr = Array.from(new Set(arr))
```

1. Create a new Set from the existing array, which automatically removes duplicates.

2. Use the spread operator `...` or `Array.from` method to convert the Set to Array.

