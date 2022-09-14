202209142135
Tags: #fundamentals 

--- 
# FP. Currying
Currying is a transformation of functions that translates a function from `f(a, b, c)` into `f(a)(b)(c)`.
Currying doesn't call a function, just transforms it.

```js
function curry(f) { 
	// curry(f) does the currying transform
	return function curried(...args) {
		if (args.length >= func.length) {
			return func.apply(this, args);
		} else {
			return function(...args2) {
				return curried.apply(this, args.concat(args2));
			}
		}
	};
}

// usage
function sum(a, b, c) {
	return a + b + c;
}

let curriedSum = curry(sum);

console.log(curriedSum(1, 2)); // 3
console.log(curriedSum(1)(2)); // 3
console.log(curriedSum(1)(2, 3)); // 6
```

## Source
https://javascript.info/currying-partials