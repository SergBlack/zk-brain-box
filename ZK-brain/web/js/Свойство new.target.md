202203132246
Tags: #javascript 

--- 
# Свойство new.target
Используя специальное свойство `new.target` внутри функции, мы можем проверить, вызвана ли функция при помощи оператора `new` или без него.

В случае, если функция вызвана при помощи `new`, то в `new.target` будет сама функция, в противном случае `undefined`.

```js
function User() { 
	console.log(new.target);
} 

// без "new": 
User(); // undefined

// с "new": 
new User(); // function User { ... }
```