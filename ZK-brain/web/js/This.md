202201192341
Tags: #javascript 

--- 
# this
this является указателем объекта на самого себя.
this в JavaScript не фиксированный (в отличии от других языков), мы можем привязать контекст к функции через встроенные методы функции `call, apply, bind`

this это объект перед точкой :
```js
const person = {
	firstname: 'John',
	lastname: 'Black',
	getFullname() {
		return `${this.firstname} ${this.lastname}`
	}
};
```

## Источник
https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Operators/this
https://learn.javascript.ru/object-methods

--- 
### Links
- [[Контекст вызова функции]]