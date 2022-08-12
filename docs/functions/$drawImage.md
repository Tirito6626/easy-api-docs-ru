# $drawImage
Рисует картинку на холсте.

### Использование:
```
$drawImage[айди картинки;x позиция;y позиция;ширина;высота]
```

> **Вам нужно загрузить картинку используя [`$loadImage`](functions/$loadImage)**

### Пример:

```js
$drawImage[myCoolId;0;0;512;512]
$loadImage[myCoolId;link;https://i.imgur.com/upR5GuS.png] // Нужно для использования данной функции.
$createCanvas[512;512] // Нужно для использования данной функции
```
