# $registerFont
Регистрирует кастомный шрифт из заданного путя

### Использование:
```
$registerFont[путь;имя шрифта]
```

> ⚠️: **Разрешённые типы файлов: `.ttf`, `.otf`**

### Example:

```js
$drawText[...]
$font[30;Any name] // Теперь мы можем использовать это
$createCanvas[512;512]
$registerFont[./assets/myfont.ttf;Any name] // Мы регистрируем шрифт со своим именем
```
