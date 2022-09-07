# $addEffect
Добавляет эффект к контексту холста

### Использование:
```js
$addEffect[эффект; качество пременения]
```
> [`CanvasRenderingContext2D/filter`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/filter)

> 💡: Удаление эффекта смотри здесь [`$removeEffect`](functions/$removeEffect.md)

> Все эффекты можно посмотреть в [`Советах`](https://weredokgang.github.io/easy-api-docs-ru/#/tips)
### Пример:
```js
...
$addEffect[grayscale;50]
$createCanvas[512;512]
```
