# Кастомные функции

## Описание
Вы можете создавать собственные функции, задавая им нужный функционал.

## Использование
```javascript
bot.functionManager.createCustomFunction({
name: "$название",
params: ["параметры"],
type: "тип",
code: `код`
})
```

## Опции
- `name` - название функции, указывайте с $
- `params` - параметры, которые нужно указывать. Если их нету - просто укажите [""]
- `type` - тип кода функции. Доступно только aoi.js и djs
- `code` - код функции

## Пример создания и использования
```javascript
bot.functionManager.createCustomFunction({
name: "$developer",
params: ["option"],
type: "aoi.js",
code: ` $if[{option}==tag;$user[$botOwnerID;tag];] $if[{option}==mention;<@$botOwnerID>;] $if[{option}==avatar;$userAvatar[$botOwnerId];] `
})
```
