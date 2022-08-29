# $addEffect
Добавляет эффект к контексту холста

### использование:
```js
$addEffect[эффект; качество пременения]
```
> [`CanvasRenderingContext2D/filter`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/filter)

> 💡: Удаление эффекта смотри здесь [`$removeEffect`](functions/$removeEffect.md)

### пример:
```js
...
$addEffect[grayscale;50]
$createCanvas[512;512]
```
