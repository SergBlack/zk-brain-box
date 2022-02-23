202202232235
Tags: #javascript 

--- 
# Hoisting
Интерпретатор JavaScript всегда незаметно перемещает ("поднимает" - hoisting) объявление функций и переменных в начало области видимости:

```js
// Это значит, что такой код:
function foo() {
	if (false) {
		var x = 1;
	}
	return;
	var y = 1;
}

// на самом деле интерпретируется так:
function foo() {
	var x, y;
	if (false) {
		x = 1;
	} 
	return;
	y = 1;
}
```

--- 
### Links
- [[Области видимости]]