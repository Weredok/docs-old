# bot.onRoleUpdate

## Описание 
Реагирует на любое обновление роли. Для получения новых свойств роли используйте функцию [$newRole](functions/usdnewrole). Для старых свойств - [$oldRole](functions/usdoldrole)

## Использование
```javascript
bot.onRoleUpdate({
channel: "",
code: `код`
})
```

## Тип в загрузчике команд
```javascript
type: "roleUpdate",
```
