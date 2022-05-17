# $interactionDefer

## Описание
Получает запрос на ответ после отсрочки для интерактивного ответа, на случай если ответ будет более чем через 3 секунды.

## Использование
```js
$interactionFollowUp
```

### Опции
Отсутствуют

## Пример использования
```js
$interactionReply[Сейчас играет - $songInfo[title]]
$interactionFollowUp
$playTrack[youtube;$slashOption[track]]
$interactionDefer
```
