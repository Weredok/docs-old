# bot.onChannelUpdate

## Описание 
Реагирует на обновление канала. Для получения новых свойств канала используйте функцию [$newChannel](https://weredok.gitbook.io/docs/usdnewchanel). Для старых - [$oldChannel](https://weredok.gitbook.io/docs/usdoldchannel).

## Использование
```javascript
bot.onChannelUpdate({
channel: "",
code: `код`
})
```

## Тип в загрузчике команд
```javascript
type: "channelUpdate",
```
