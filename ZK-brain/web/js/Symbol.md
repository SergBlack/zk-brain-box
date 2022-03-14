202201142254
Tags: #javascript 

--- 
# Symbol
Тип Symbol используется для создания уникальных идентификаторов в объектах:

```js

const id = Symbol('id');
```

Символом можно создавать скрытые поля объекта, к которым нельзя нечаянно обратиться и изменить их незаметно, а так же не перебираются циклом `for..in` или `Object.keys`:

```js
const obj = {};

const id = Symbol("id");

obj[id] = "value 1";
obj.id = "value 2";

console.log(obj); // выведется только {id: "value 2"}
console.log(obj[id]);// но доступ к "value 1" есть
```

А вот `Object.assign`, в отличие от цикла `for..in`, копирует и строковые, и символьные свойства.

## Источник
https://learn.javascript.ru/symbol

--- 
### Links
- [[Глобальные символы]]