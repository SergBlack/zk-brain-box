202204062252
Tags: #react 

--- 
# Purpose of useCallback
После создания компонента и объявления внутри него callback `handleClick`, то на каждый последующий рендер будет создаваться новая функция. Причина проста - компонент это функция и после её вызова она удаляется и следующий рендер вызывает функцию `App` с чистого листа.

```js
const App = () => {
	const handleClick = () => {
		console.log('click');
	};
	// ...
}
```
Исходя из этого следует, что для того чтобы сохранить какие-то данные между ререндерами мы должны использовать другой хук `useRef`.

Но бывают случаи, когда надо сохранять экземпляр функции-callback между рендерами:
1. Дочерний компонент обернут в `React.memo()` и принимает в качестве пропсов callback.
2. Когда callback является зависимостью других хуков, например `useMemo`, `useEffect`.
3. Когда функция имеет какое-то внутреннее состояние, например `debounce` и `throttle`.

```js
const App = () => {
	const handleClick = useCallback(() => {
		console.log('click');
	}, []);
	// передавая пустой массив, мы получим на выходе всегда одну и ту же функцию
}
```

Использовать во всех случаях `useCallback` когда через props передается callback плохая идея.