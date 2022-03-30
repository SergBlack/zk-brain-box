202203302251
Tags: #javascript 

--- 
# Class. Вызов new
Когда вызывается `new User("Иван")`:
1.  Создаётся новый объект.
2.  `constructor` запускается с заданным аргументом и сохраняет его в `this.name`.

```js
class User {
	constructor(name) { this.name = name; }
	sayHi() { console.log(this.name); }
}

// Использование:
const user = new User("Иван");
user.sayHi();

// класс - это функция
console.log(typeof User); // function

// ...или, если точнее, это метод constructor
console.log(User === User.prototype.constructor); // true

// Методы находятся в User.prototype, например:
console.log(User.prototype.sayHi); // console.log(this.name);

// в прототипе ровно 2 метода
console.log(Object.getOwnPropertyNames(User.prototype)); // constructor, sayHi
```

Вот что на самом деле делает конструкция `class User {...}`:
1.  Создаёт функцию с именем `User`, которая становится результатом объявления класса. Код функции берётся из метода `constructor` (она будет пустой, если такого метода нет).
2.  Сохраняет все методы, такие как `sayHi`, в `User.prototype`.

При вызове метода объекта `new User` он будет взят из прототипа, как описано в главе [[Function.prototype]]. Таким образом, объекты `new User` имеют доступ к методам класса.

![[Pasted image 20220330224844.png]]