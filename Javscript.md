# JS
### Const
A javascript const is not a constant in the traditional sense. A JS const does not mean the variable is immutable, rather it means the variable binding is.

What this is means is that you can call functions to change the state of the variable but cannot redeclare.

### Objects
##### Looping over javascript objects (ES6)
Objects are like maps but they can't be enumerated over normally. To do so you you need to convert the object property keys into an array and loop over like so:

```
const obj = {
  a: 1
  b: 2
  c: 3
}

Object.keys(obj).forEach((key) => {
  console.log(key)
})

Should output:
1
2
3
```

**Note that `Object.keys` will not include properties from Javascript Prototype object**

##### Object order property
Javascript automatically sorts properties (at least in chrome), they are sorted in the following order.
[More info here](https://www.stefanjudis.com/today-i-learned/property-order-is-predictable-in-javascript-objects-since-es2015/)

1. Integers
  - Integer indices are sorted numerically in asending order (lowest first)
1. Strings
  - Properties not included as integers indices come next and are sorted in chronological order (the order they are inserted)
1. Symbol
  - Same as strings
