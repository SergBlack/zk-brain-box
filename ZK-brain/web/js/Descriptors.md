202203272246
Tags: #javascript 

--- 
# Descriptors
### data descriptors:
- `value` - где хранится само значение;
-  `writable` – если `true`, свойство только можно перезаписывать, иначе только для чтения;
-  `enumerable` – если `true`, свойство перечисляемое в циклах;
-  `configurable` – если `true`, свойство можно удалить, а атрибуты `writable` и `enumerable` можно изменять, иначе этого делать нельзя.

### accessor descriptors:
-  `getter` – функция без аргументов, которая сработает при чтении свойства,
-  `setter` – функция, принимающая один аргумент, вызываемая при присвоении свойства,
-  `enumerable` - см. выше
-  `configurable` - см. выше

```js
let obj = {
	// геттер, срабатывает при чтении obj.propName
	get propName() {},
	
	// сеттер, срабатывает при записи obj.propName = value
	set propName(value) {},
};
```

Определяя свойство через Object.defineProperty() для accessor-property мы не можем использовать `value` и `writable`, что логично, для этого есть геттер и сеттер.