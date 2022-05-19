<p align="center">
  <a href="https://aoi.js.org">
    <img width="200" src="https://cdn.discordapp.com/attachments/804813961190572093/924765606056701952/aoits.png">
  </a>
</p>

<h1 align="center">aoi.js</h1>

<div align="center">

**Продвинутый и мощный инструмент для создания вашего бота.**

[![NPM version][npm-image]][npm-url]
[![AoiJS Server][aoijs-server]][aoijs-server-url]
[![NPM downloads][download-image]][download-url]


[npm-image]: http://img.shields.io/npm/v/aoi.js.svg?style=flat-square
[npm-url]: http://npmjs.org/package/aoi.js
[download-image]: https://img.shields.io/npm/dt/aoi.js.svg?style=flat-square
[download-url]: https://npmjs.org/package/aoi.js
[aoijs-server]: https://img.shields.io/discord/773352845738115102?color=5865F2&logo=discord&logoColor=white
[aoijs-server-url]: https://aoi.js.org/invite

[Preview](https://aoi.js.org/docs/example.md)

</div>

## Возможности

- Мощные функции с лёгким использованием!
- Написано на TypeScript для удобства находить ошибки в функциях.
- Обновлено с поддержкой других расширений от [Akarui Development](https://github.com/AkaruiDevelopment/). 
- Структура и функционал взят из [dbd.ts](https;//npmjs.org/package/dbd.ts)

## Установка

```bash
npm install aoi.js
```

```bash
yarn add aoi.js
```

## Пример

```javascript
const { AoiClient } = require("aoi.js");

const bot = new AoiClient({
    token: "ТОКЕН",
    intents: ["Guilds", "GuildMessages", "MessageContent"],
    prefix: "ПРЕФИКС"
})

bot.addEvent("onMessage")

bot.commands.add("basicCommand", {
    name: "ping",
    code: `Понг! $pingms`
})

bot.start()
```
