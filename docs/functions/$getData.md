# $getData
Получает значение свойства в объекте json запроса(если присутствует).

## Использование:
```
$getData[свойство]
```

### Example:
```js
$getData[data.something] 
$request[...] // нужно для использования данной функции 

// Пример кода:
$send[$getData[data.translated]] // returns: Bonjour le monde
$request[https://api.miduwu.ga/json/translate?source=auto&target=fr&text=Hello+world]
```

<br/>

__ __
<br/>
<br/>

  Ссылка переведена в json
```json
{
 "status": 200,
 "data": {
  "translated": "Bonjour le monde",
  "source": "en",
  "target": "fr"
 },
 "success": true
}
```
  Так что вы можете выбрать объект и потом его значение, например: 
```js
data.source // выводит: en
status // выводит: 200
```
