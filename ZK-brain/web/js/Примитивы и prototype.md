202203282324
Tags: #javascript 

--- 
# Примитивы и prototype
Примитивы не объекты. Но мы можем получить доступ к их  методам, тогда создаётся временный объект-обёртка с использованием конструкторов `String`, `Number` и `Boolean`, который предоставит методы и после удалится. Методы этих объектов также находятся в прототипах, доступных как `String.prototype`, `Number.prototype` и `Boolean.prototype`.

Значения `null` и `undefined` не имеют объектов-обёрток и прототипов, поэтому у них нет никаких методов.

--- 
### Источник
https://learn.javascript.ru/native-prototypes#object-prototype