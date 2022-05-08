# Интерактивные взаимодействия
Использование интерактивных взаимодействий с пользоателем - **слэш команды, кнопки, меню выбора**
## Слэш-команды 
Для начала создадим ивенты в главном файле, чтобы начать работу с интерактивами: `bot.onInteractionCreate()`, `bot.onInteractionDelete()` и `bot.onInteractionUpdate()`.
Теперь, создадим слэш-команду на сервере. Для этого нам понадобится функция `$createApplicationCommand`.
Создаём команду с ней: 
```js
module.exports = {
  name: "c-slash",
  code: