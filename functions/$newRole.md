# $newRole

## Описание
Выдаёт свойства роли после её обновления. Paботает только в обратном вызове [roleUpdate](callbacks/roleUpdate)

## Использование
```js
$newRole[опция]
```

### Опции
- `опция` - то, что нужно получить из свойств: 
          - `name` - Название роли
          - `color` - Цвет роли
          - `position` - Позиция роли
          - `perms` - Права роли 

## Пример использования
```javascript
Название роли $oldRole[name] было изменено на $newRole[name]
$onlyIf[$oldRole[name]!=$newRole[name];]
```
