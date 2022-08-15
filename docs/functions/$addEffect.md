# $addEffect
Добавляет эффект к контексту холста

### использование:
```js
$addEffect[эффект; качество пременения]
```
### эффекты:
- **`blur`** размытие по гаусу. Если поставить  `0` то ничего не изменится.
- **`brightness`** Applies a linear multiplier to the drawing, making it appear brighter or darker. Если поставить `100` то ничего не изменится .
- **`contrast`** Adjusts the contrast of the drawing. A value of `100` leaves the drawing unchanged.
- **`grayscale`** Converts the drawing to grayscale. A value of `100` is completely grayscale. A value of `0` leaves the drawing unchanged.
- **`invert`** Inverts the drawing. A value of `100` means complete inversion. A value of `0` leaves the drawing unchanged.
- **`saturate`** Saturates the drawing. A value of `0` means completely un-saturated. A value of `100` leaves the drawing unchanged.
- **`sepia`** Converts the drawing to sepia. A value of `100` means completely sepia. A value of `0` leaves the drawing unchanged.

> [`CanvasRenderingContext2D/filter`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/filter)

> 💡: Удаление эффекта смотри здесь [`$removeEffect`](functions/$removeEffect.md)

### пример:
```js
...
$addEffect[grayscale;50]
$createCanvas[512;512]
```
