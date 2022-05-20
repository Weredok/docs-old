# bot.onMessageUpdate

## Описание 
Выполняет код, когда кто-то обноляет свойства сообщения. Чтобы получить контент сообщения до его обновления существует функция $oldMessage.
Чтобы получить айли канала в котором это произошло - $channelUsed.


## Использование
```javascript
bot.onMessageUpdate({
channel: "$channelID",
code: `
Пользователь $userTag изменил своё сообщение. Старое содержимое - $oldMessage. Новое содержимое - $message.
$onlyIf[$oldMessage!=$message;]

## Тип в загрузчике команд
```js
type: "messageUpdate",
```
