# $oldRole

## Описание
Выдаёт свойства роли после до обновления. Paботает только в обратном вызове [roleUpdate](callbacks/roleUpdate).

## Использование
```js
$oldRole[опция]
```

### Опции
- `Oпция` - то, что нужно получить из свойств роли: 
 
    - `name` - Название 
     
    - `hexColor` - Цвет 
          
    - `position` - Позиция 

    - `rawPosition` - Позиция, полученная от Discord API
          
    - `permissions` - Права  
    
    - `hoist` - Отображаемость

    - `mentionable` - Разрешено ли упоминать роль

    - `editable` - Может ли бот изменить эту роль
    
    - `managed` - Управляет ли этой ролью DiscordAPI (роль интеграции / бустера сервера)
    
    - `deleted` - Удалена ли роль
    
    - `members` - Участники
          
    - `membersCount` - Количество участников
    
    - `createdAt` - Дата создания
    
    - `createdTimestamp` - Дата создания в миллисекундах 
     
        
## Пример использования
```javascript
Название роли $oldRole[name] было изменено на $newRole[name]
$onlyIf[$oldRole[name]!=$newRole[name];]
```
