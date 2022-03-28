202203282312
Tags: #javascript 

--- 
# Object.prototype
Когда вызывается `new Object()` (или создаётся объект с помощью литерала `{...}`), свойство `[[Prototype]]` этого объекта устанавливается на `Object.prototype`:

```js
let obj = {};

console.log(obj.__proto__ === Object.prototype); // true

// obj.toString === obj.__proto__.toString === Object.prototype.toString
```

Согласно спецификации наверху иерархии встроенных прототипов (таких как `Array.prototype`,` Function.prototype`, `Date.prototype` и другие) находится `Object.prototype`. Поэтому все в JavaScript наследуется от объектов:

![[Pasted image 20220328232030.png]]

--- 
### Источник
https://learn.javascript.ru/native-prototypes#object-prototype