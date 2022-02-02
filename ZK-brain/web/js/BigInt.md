202201132252
Tags: #javascript 

--- 
# BigInt
BigInt нужен тогда, когда число не влезает в 64 бита обычного числа (это 2^53 для положительного или отрицательного числа).

Способы объявления:
- добавив в конце числа 'n'
- используя функцию BigInt() и передав ей аргумент ввиде строки или числа

```js
// символ "n" в конце означает, что это BigInt 
const bigint = 1234567890123456789012345678901234567890n; 

const sameBigint = BigInt("1234567890123456789012345678901234567890"); 

const bigintFromNumber = BigInt(10); // то же самое, что и 10n
```

## Источник
https://learn.javascript.ru/bigint