# $tryIf
Выполняет код если условие верное.
Обычный иф=)
### использование:
```
$tryIf[условие;код]
```
> **Правильный синтаксис:** `@function(inside;more;splits)`

> **Пример:** `@send(200;json;{})`

### пример:
```js
$tryIf[$getQuery[image]==undefined;
    @break
    @ignore(перестанет исполнять код (из за $tryIf,т.к он в конце кода).)
    @log(There is not provided image.)
    @send(400;json;{
        error: 'Missing image.'
    })
]
```
