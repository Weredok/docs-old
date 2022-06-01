# Пользовательские функции
В aoi.js существует возможность создания собственных функций, используя скрипты aoi.js или discord.js. Создавать их можно при помощи функции `bot.functionManager.createCustomFunction({})` в главном файле

## Использование
```javascript
bot.functionManager.createCustomFunction({
name: "$function",
type: "тип кода",
params: ["параметры"],
code: `код функции`
})
```

## Опции
- `name` - название функции, используя $
- `type` - тип кода:

    - `aoi.js` - Код на aoi.js

     - `djs` - Код на discord.js
 
- `params` - параметры функции в виде массива. Чтобы получить параметр, просто используйтет {param} в своём коде, где param - название параметра. Если же их не должно быть - просто []
- `code` - код функции

## Пример использования
```javascript
bot.functionManager.createCustomFunction({
name: "$bot",
type: "aoi,js",
params: ["option"],
code: ` $if[{option}==token;$clientToken;]
$if[{option}==developer;$usertag[$botOwnerID];]
$if[{option}==avatar;$userAvatar[$clientID];]`
})
```
