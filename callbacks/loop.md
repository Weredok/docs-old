# bot.onLoop

## Описание 
Выполняет код каждые **x** миллисекунд.

## Использование
```javascript
bot.loopCommand({
channel: "",
executeOnStartUp: true/false,
every: 1000,
code: `код`
})
```
## Опции
- `executeOnStartUp` - будет ли бот начинать выполнение кода сразу после включения бота
- `every` - промежуток времени, через которое бот будет выполнять код.

## Тип в загрузчике команд
```javascript
type: "loop",
```
