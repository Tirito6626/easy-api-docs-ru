# $replaceRegexp
Заменяет что-то используя RegExp

### Использование:
```
$replaceRegexp[текст;regexp;regexp флаг;замена]
```
### Пример:
```js
$replaceRegexp[$get[text];/[^a-zA-Z0-9]/;g;] // Hello  what are u doing
$var[text;Hello $ #what are u doing!]
```
