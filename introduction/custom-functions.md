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
