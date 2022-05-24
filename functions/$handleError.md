# $handleError

## Описание
Выдаёт свойства ошибки. Работает только если тип команды "functionError".

## Использование
```js
$handleError[опция]
```

### Опции
- `опция` - свойство, которое нужно получить:
      - `function` - функция, в которой произошла ошибка
      - `error` - текст ошибки
      - `command` - название команды, в которой произошла ошибка

## Пример использования
```javascript
$handleError[command]: $handleError[function]: $handleError[error]
```
