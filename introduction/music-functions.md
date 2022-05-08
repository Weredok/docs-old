# Музыкальные функции

Для использования музыкальных функций необходимо установить дополнительный пакет `@akarui/aoi.music`

## Установка

```
npm i @akarui/aoi.music
```

## Настройка в aoi.js

После установки aoi.music, нужно настроить отдельный класс для музыки в aoi.js.

```js
const { Voice, LoadCommands, Bot } = require("aoi.js");

const bot = new Bot({
  token: "DISCORD BOT TOKEN",
  prefix: ".",
  intents: ["guilds", "guildMessages", "guildVoiceStates"],
});

const loader = new LoadCommands(bot);

const voice = new Voice(
  bot,
  {
    cache: {
      cacheType: "Memory",//Кэш
      enabled: true,
    }
  },
  true, //для включения pruneMusic 
);

voice.onTrackStart();

loader.load(bot.cmd, "./Commands/commands/"); //загрузчик обычных команд
loader.load(voice.cmd, "./Commands/voice/"); //загрузчик музыкальных команд
```

## Использование пакета после установки и настройки

### play

```js
//Commands/commands/play.js
module.exports = {
  name: "play youtube",
  $if: "v4", //включает старое использование $if
  code: `
    $let[msg;$playTrack[youtube;$message]]

    $if[$hasPlayer==false]
        $joinVc
    $endif

    $onlyif[($voiceId[$clientId]!=)&&($voiceId[$clientId]==$voiceId);присоеденись к голосовому каналу в котором находится бот]
    $onlyif[$voiceId!=;присоеденись к голосовому каналу чтобы слушать музыку]
    `,
};
```

### queue

```js
//Commands/commands/queue.js
module.exports = {
  name: "queue",
  code: `
   $title[1;Очередь]
   $description[1;$queue[$if[$message==;1;$message]]]
   $footer[1;Количество треков в очереди - $queueLength]
   $color[1;RANDOM]
   $addTimestamp[1]
    `,
};
```

### onTrackStart ивент

```js
//Commands/voice/trackStart.js
module.exports = {
  name: "отправляется когда начинает играть новый трек", //необязательно
  type : "trackStart",
  channel : "$channelId",
  code: `
	  $title[1;Сейчас играет]
	  $description[1;$if[$musicEventData[info.description]==;описание не найдено;$musicEventData[info.description]]]
      $color[1;RANDOM]
	  $author[1;$musicEventData[info.title]]
	  $image[1;$musicEventData[info.thumbnail]]
    `,
};
```
