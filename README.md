# О пакете
aoi.js это пакет с настриваемыми и готовыми функциями, позвляющий с легкостью создавать ботов для Discord. 

* Поддержка интерактивных взаимодействий
* Поддержка музыкальных функций
* Доступно более 600 функций!

## Установка
```js
npm i aoi.js
```
```js
yarn add aoi.js
```

## Пример
```js
const aoijs = require("aoi.js")

const bot = new aoijs.Bot({
token: "token",// Токен бота
prefix: "!", // Префикс бота
intents: ["GUILDS", "GUILD_MESSAGES"] // Интенты
})

//Ивенты
bot.onMessage()

//Пример команды для проверки пинга
bot.command({
name: "ping",
code: `Понг! $pingms`
})

//Команда при запуске
bot.readyCommand({
    channel: "",
    code: `$log[$userTag[$clientID] запущен!]`
})
```

## Ссылки
* [Веб-cайт](https://aoi.js.org/)
* [Гитхаб](https://github.com/akaruidevelopment/aoi.js)
* [Дискорд](https://discord.gg/psgxGqZCm8)
