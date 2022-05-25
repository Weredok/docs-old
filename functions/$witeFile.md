# $writeFile

## Описание
Создаёт файл в указанном пути с указанным кодом внутри. Если файл уже существует - бот его перезапишет.

## Использование
```js
$writeFile[путь;код]
```

### Опции
- `путь` - путь где находится файл
- `код` - код внутри файла

## Пример использования
```javascript
$writeFile[commands/ping.js;module.exports = { name: "ping", code: `$pingмс` }]
```