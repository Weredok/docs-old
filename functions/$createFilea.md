# $createFile

## Описание
Отправляет файл с указанным названием и кодом внутри.

## Использование
```js
$createFile[код;название]
```

### Опции
- `код` - код, находящийся внутри файла.
- `название` - название файла.

## Пример использования
```javascript
$createFile[module.exports = {
name: "eval",
code: ` $eval[$message]
$onlyForIds[$botOwnerID;]`
};eval.js]
```
