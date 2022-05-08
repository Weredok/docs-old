---
description: Как настроить статус бота
---


### Настройка статуса:

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

### ---
description: How to setup a Bot Status
---

# Client Status

### Setting a Client Status:

{% hint style="danger" %}
You need to enter the following, in your main index.
{% endhint %}

### Usage:

```javascript 
bot.status({
  text: "TEXT",
  type: "PLAYING",
  time: 12
})
```

### Adding multiple Client Status:

```javascript
bot.status({
  text: "TEXT1",
  type: "PLAYING",
  time: 12
})

bot.status({
  text: "TEXT2",
  type: "WATCHING",
  time: 12
})
```

### Different Types:

* PLAYING
* WATCHING
* LISTENING
* STREAMING
* COMPETING

### Client Status Method:

{% hint style="info" %}
If you want to change the bot's discord status use the following
{% endhint %}

```javascript
bot.status({
  text: "TEXT",
  type: "PLAYING",
  status: "idle",
  time: 12
})
```

### Different Status:

* idle
* dnd
* online
* invisible

### Streaming URL Method:

{% hint style="info" %}
Streaming-Status supports YouTube-Video-URL or Twitch-Channel-URLs.

If you want to enter an URL, Enter the following
{% endhint %}

```javascript
bot.status({
text: "TEXT", 
type: "STREAMING", 
url: "URL"
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

