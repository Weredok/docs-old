# bot.onMessageDelete

## Описание 
Бот может реагировать на удаление сообщение - выдавать автора, контент и время удаления.

## Использование
```javascript
bot.onMessageDelete({
channel: "$channelID",
code: `Пользователь $userTag удалил своё сообщение. Сообщение - $message. Канал - <#$channelID>`
})
```

## Тип в загрузчике команд
```js
type: "messageDelete",
```
