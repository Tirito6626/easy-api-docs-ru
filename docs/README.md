### EASY-API.TS
Создайте свой собственный API с легкостью.

![изображение](https://camo.githubusercontent.com/1b637c74e2bcd2feb02d7a3ca3d61263bed5d673dfd472ee663157db1d2000f6/68747470733a2f2f692e696d6775722e636f6d2f326b735a5342792e6a7067)

## настройка апи

```js
import { API } from "easy-api.ts"; //используйте 'const { API } = require("easy-api.ts")' для JavaScript

const api = new API({
    port: process.env.PORT || 3000
})

api.routes.add({
    path: '/color',
    code: `
    $ignore[Посмотрите документацию для того чтобы узнать как работает эта функция]
    $send[200;canvas;$default]
    $drawRect[0;0;512;512]
    $color[$getQuery[hex]]
    $createCanvas[512;512]
    $if[$isValidHex[$getQuery[hex]]==false;400;{
        error: "Вы ввели неправильный hex цвет"
    }]
    $if[$getQuery[hex]==undefined;400;{
        error: "Не обнаружен hex параметр."
    }]
    `
})

// Используйте загрузчик...
api.routes.load('./routes').then(() => {
    console.log('АПИ загружено.')
    api.connect() // Мы подключаемся к API, когда все загрузилось.
})
```

## Вы должны знать...
- Для использования вам нужен Nodejs версия которого выше или равна 14
- Код читается снизу вверх.
- Это оболочка express, расширенная пользовательскими функциями, такими как канвас, объекты, HTML и подобные.
- У библиотеки есть баги.(отправь репорт если нашел)
- Эта библиотека была сделана используя JavaScript и TypeScript.
