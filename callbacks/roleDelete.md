# bot.onRoleDelete

## Описание 
Реагирует на удаление роли. Для получения её свойств роли используйте функцию [$newRole](functions/usdnewrole). Для старых свойств - [$oldRole](functions/usdoldrole)

## Использование
```javascript
bot.onRoleDelete({
channel: "",
code: `код`
})
```

## Тип в загрузчике команд
```javascript
type: "roleDelete",
```
