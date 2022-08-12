# $opacity
изменяет прозрачность текста на холсте.

### использование:
```
$opacity[значение]
```
> **значение может быть от `1` до `100`**

### пример:

```js
$drawImage[image;0;0;512;512] // this image will be with 50% opacity.
$opacity[50]
$loadImage[image;https://i.imgur.com/upR5GuS.png]
$createCanvas[512;512] // required to use this function
```
