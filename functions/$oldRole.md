# $oldRole

## Описание
Выдаёт свойства роли до её обновления. Paботает только в обратном вызове [roleUpdate](callbacks/roleUpdate).

## Использование
```js
$oldRole[опция]
```

### Опции
- `Oпция` - то, что нужно получить из свойств роли: 
 
    - `name` - Название 
     
    - `hexColor` - Цвет 
          
    - `position` - Позиция 
          
    - `permissions` - Права  
         
    - `members` - Участники
          
    - `membersCount` - Количество участников
    
    - `creatednAt` - Дата создания
    
    - `createdTimestamp` - Дата создания в миллисекундах 
     
        
## Пример использования
```javascript
Название роли $oldRole[name] было изменено на $newRole[name]
$onlyIf[$oldRole[name]!=$newRole[name];]
```
