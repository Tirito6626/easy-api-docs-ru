# Советы

Полезные советы для улучшения вашего опыта кодирования.

## Обработчик

Загрузите маршруты с обработчиком.

**Пример (установка):**
```js
import { API } from "easy-api.ts";

const api = new API({...})

api.routes.load('./routes').then(() => {
    api.connect() // We're starting the API when the source is ready.
})
```

**пример (маршрут):**
```js
// path: './routes/../../../route.js'
module.exports = {
    path: '/endpoint/name',

    code: `
    $send[200;json;{
        success: true
    }]
    `
}
```

## Использования базы данных.

Сохранение, получение и удаление переменных из базы данных

**Пример (настройка):**
```js
import { API } from "easy-api.ts";

const api = new API({
    port: process.env.PORT || 3000,
    database: {
        enabled: true, // ОЧЕНЬ ВАЖНАЯ СТРОЧКА (ХД ТАК И НАПИСАНО)!!
        type: 'replit', // Вы можете использовать: 'replit' | 'default' | 'mongo'
        // mongoUrl: '...'
    }
})

api.connect()
```

**Функции:**

`$deleteVar[var name]` [доки здесь.](functions/$deleteVar.md)

`$getVar[var name]` [доки здесь.](functions/$getVar.md)

`$setVar[var name;value]` [доки здесь.](functions/$setVar.md)

## Создание своей функции

Добавьте свою собственную функцию, используя класс `<API>.interpreter`.

**Пример:**
```js
import { API, FunctionBuilder, Utils } from "easy-api.ts";

const api = new API({...})

api.interpreter.addFunction({
    data: new FunctionBuilder()
    .setName('test'),
    code: async d => {
        const unpacked = d.unpack(d)
        if(!unpacked.inside) return Utils.Warn('Invalid inside provided in:', d.func)
        return {
            code: d.code.resolve(`${d.func}[${unpacked.inside}]`, unpacked.inside + '< was a test.')
        }
    }
})

api.connect()
```
### эффекты:
- **`blur`** размытие по гаусу. Если поставить  `0` то ничего не изменится.
- **`brightness`** Применяет линейный множитель к чертежу, делая его ярче или темнее. Если поставить `100` то ничего не изменится .
- **`contrast`** Регулировка контрастности рисунка. Значение `100` оставляет рисунок без изменений.
- **`grayscale`** Преобразует рисунок в оттенки серого. Значение `100` полностью в оттенках серого. Значение `0` оставляет чертеж без изменений.
- **`invert`** Инвертирует рисунок. Значение '100' означает полную инверсию. Значение `0` оставляет чертеж без изменений.
- **`saturate`** Насыщает рисунок. Значение `0` означает совершенно ненасыщенное. Значение `100` оставляет рисунок без изменений.
- **`sepia`** Преобразует рисунок в сепию. Значение `100` означает полностью сепию. Значение `0` оставляет чертеж без изменений.
