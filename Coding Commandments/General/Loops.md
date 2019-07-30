Loops over arrays are another commonly used operation within any language. Here is how you'd typically iterate an array:

```
for ( var i = 0; i < array.length; i++ ) {
    console.log(array[i])
}
```

Although this is a pretty standard looping method, but the problem with it is that you have to keep track of an incrementing index value. That value becomes another moving part in the machinery. The more moving parts, greater are the chances of error.

Fortunately, we have a bunch of different methods in JavaScript that reduce those moving parts. Simple for loops like above should be avoided in favor of methods described below.

# `forEach`

You can iterate an array with `forEach` method, if you only need to read each value of the array.

```
array.forEach(item => {
    console.log(item)
})
```

# `map`

You can iterate an array with `map` method, if for every item of the array, you need another item.

```
const array = [1, 2, 3, 4, 5]

const arrayIncremented = array.map(n => {
    return n + 1
})

console.log('incremented values: ', arrayIncremented)
```

# `reduce`

You can iterate an array with `reduce` method, if for all items of an array, you need a single value.

```
const array = [1, 2, 3, 4, 5]

const sum = array.reduce((n, memo) => {
    return n + memo
}, 0)

console.log('sum: ', sum)
```

These three methods sufficiently cover bulk of the array iteration problems you face day to day. Mastering them will give you great mileage in improving code quality. 