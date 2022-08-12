# $escape
Превращает текст в "знаки"

> **Эта функция была сделана для предотвращения багов**

### Использование:
```
$escape[текст]
```

### Пример:
```js
$condition[$escape[==]==$escape[==]] // => '@equal@equal==@equal@equal' (Правда)
$condition[======] // Это не может быть использовано.

$condition[$escape[<:v]==$escape[<;v]] // => '@lower@colonv==@lower@semiv' (Правда)
$condition[<:v==<;v] // Это не может быть использовано.
```

> Посмотрите знаки в: **[Знаки](escapers.md)**
