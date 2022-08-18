# $send
Отправляет что-то для http ответа

### Использование:
```
$send[статус;тип (json\|safe\|canvas\|file\|redirect\|other);текст(для JSON)/$default]
```

### Пример:
```js
// для JSON
$send[200;json;{
    "data": "Hello!"
}]

// для safe объектов
$send[200;safe;$default]
$setObjectKey[data;Hello!]
$createObject

// для холста
$send[200;canvas;$default]
// more canvas things here...
$createCanvas

// для файлов (json, html, etc...)
$send[200;file;./location/file.ext]

// для редиректа
$send[200;redirect;https://google.com]

// для другого (texts, html, etc...)
$send[200;other;
<h1>Test</h1>
<p>This is a cool HTML test</p>
]
```
