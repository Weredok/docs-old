# $newRole

## Описание
Выдаёт свойства роли после её обновления. Paботает только в обратном вызове [roleUpdate](callbacks/roleUpdate).

## Использование
```js
$newRole[опция]
```

### Опции
- `Oпция` - то, что нужно получить из свойств роли: 
 
    - `name` - Название 
     
    - `hexColor` - Цвет 
          
    - `position` - Позиция 
          
    - `permissions` - Права  
         
    - `members` - Участники
          
    - `membersCount` - Количество участников
     
        
## Пример использования
```javascript
Название роли $oldRole[name] было изменено на $newRole[name]
$onlyIf[$oldRole[name]!=$newRole[name];]
```
