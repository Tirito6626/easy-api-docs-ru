# $measureText
Измеряет текст по заданным параметрам.

### Использование:
```
$measureText[Текст для измерения;параметр (width/height/object)]
```
### Пример:
```js
$drawText[Привет;...]
$font[50;Arial]
$createCanvas[$get[width];$get[height]] // Теперь мы создали холст по размерам нашего текста

$let[height;$measureText[Hello;height]]
$let[width;$measureText[Hello;width]]
$font[50;Arial] // Устанавливаем размер текста, который измерим
$createCanvas[10;10] // Необязательный холст, мы сделаем новый холст
```

**Если тип `object` то оно выведет по типу:**
```json
{
    "width": число,
    "height": число
}
```
