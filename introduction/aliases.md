# Настройка псевдонимов для команд.

### Использование:

```javascript
aliases: ['TEXT1','TEXT2']
```


```javascript
bot.command({
name: "название",
aliases: ['название2','название3'],
code: `code`
})
```

### Псевдонимы для `command.js` в папке:

### Пример использования
```javascript
module.exports = ({
name: "пинг",
aliases: ['понг','бот'],
code: `$pingms`
})
```
