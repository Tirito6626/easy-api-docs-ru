# $ternary
Проверяет указанное условие, и затем исполняет код

### Использование:
```
$ternary[условие;если правдивое;если ложное]
```
### Пример:
```js
$ternary[$get[b]==true||$get[b]==false;true;false] // Ложь, оно не равно!
$ternary[$get[a]==true||$get[a]==false;true;false] // Правда, оно равно!
$var[b;yes]
$var[a;true]

$ternary[$getQuery[image]==undefined;No provided.;Provided.]
```
