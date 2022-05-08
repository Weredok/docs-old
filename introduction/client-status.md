---
description: Как настроить статус бота
---


# Статус бота

## Использование:

```javascript 
bot.status({
  text: "ТЕКСТ",
  type: "PLAYING",
  time: 12
})
```

### Добавление мульти-статусов бота:

```javascript
bot.status({
  text: "ТЕКСТ1",
  type: "PLAYING",
  time: 12
})

bot.status({
  text: "ТЕКСТ2",
  type: "WATCHING",
  time: 12
})
```

### Доступные типы статусов:

* PLAYING `Играет в`
* WATCHING `Смотрит`
* LISTENING `Слушает`
* STREAMING `Стримит`
* COMPETING `Соревнуется в`

### Опции для настройки статуса:


```javascript
bot.status({
  text: "ТЕКСТ",
  type: "PLAYING",
  status: "idle",
  time: 12
})
```

### Доступные статусы:

* idle `Не активен`
* dnd `Не беспокоить`
* online `Онлайн`
* invisible `Не в сети`

### Дополнительные опции для стримингового статуса:

```javascript
bot.status({
text: "ТЕКСТ", 
type: "STREAMING", 
url: "ССЫЛКА" //Поддерживаются ссылки на Twich каналы и Youtube видео / стримы
})
```



### Мобильный статус

```javascript
const aoijs = require("aoi.js")

const bot = new aoijs.Bot({
token: "ТОКЕН", 
prefix: "ПРЕФИКС", 
mobile: true //True или false
})
```

