# $timeoutMember

## Описание
Выдаёт указанному пользователю тайм-аут

## Использование
```js
$timeoutMember[сервер;пользователь;время;послеОкончания;причина]
```

### Опции
- `сервер` - айди сервера, на котором нужно выполнить это действие
- `пользователь` - айди пользователя, которого нужно отправить в тайм-аут
- `время` - время тайм-аута
- `послеОкончания` - ожидаемые команды, которые выполнятся после того как закончится тайм-аут
- `причина` - причина тайм-аута в журнале аудита

## Пример использования
```javascript
$timeoutMember[$guildID;$mentioned[1;no];365d;aaaa;Пользователь $username отправил подумать о своём поведении пользователя $username[$mentioned[1;no]] на 365 дней]
```
