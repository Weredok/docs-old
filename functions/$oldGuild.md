# $oldGuild

## Описание
Выдаёт информацию о свойствах сервера до его обновления. Работает только в обратном вызове (guildUpdate)[callbacks/guildUpdate]

## Использование
```js
$oldGuild[опция]
```

### Опции
- `Опция` - свойство сервера, которое должна вывести функция:
         - `name` - Название
         - `ownerId` - Айди владельца
         - `icon` - Иконка 

## Пример использования
```javascript
Название сервера изменено с $oldGuild[name] на $newGuild[name] 
$onlyIf[$oldguild[name]!=$newGuild[name];]
```
