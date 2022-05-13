# Интерактивные взаимодействия
Использование интерактивных взаимодействий с пользоателем - **слэш команды, кнопки, меню выбора**
Для начала создадим ивент в главном файле, чтобы начать работу с интерактивами: `bot.onInteractionCreate()`.

## Слэш-команды
Теперь, создадим слэш-команду на сервере. Для этого нам понадобится функция `$createApplicationCommand`.
Создаём команду с ней: 
```js
module.exports = {
  name: "c-slash",
  code: `$createAppllicationCommand[$guildid;hello;Привет, мир!;true;slash]`
```
Прописав эту команду, вы создадите слэш-команду `hello` на своём сервере с описанием `Привет, мир!`

Теперь нужно создать сам слэш в коде. 
```js
module.exports = {
name: "hello", //Название слэш-команды
type: "interaction", 
prototype: "slash",
code: `$interactionReply[Привет!] `
}
```

**Чтобы не было "Ошибки взаимодействия", для ответов нужно использовать функцию $interactionReply.**

## Кнопки

Теперь создадим сообщение с кнопкой:
```js
module.exports = {
name: "button",
code: ` Нажми на кнопку! $addButton[1;Кнопка;2;mtrx] `
}
```
И саму кнопку в коде:
```js
module.exports = {
name: "mtrx", // Название кнопки
type: "interaction",
prototype: "button",
code: `$interactionReply[wokin is cool]`
}
```
**Доступные стили кнопки**
* `primary` - синяя кнопка
* `secondary` - серая кнопка
* `danger` - красная кнопка 
* `success` - зелённая кнопка
* `link` - серая кнопка, нажав на которую можно попасть на сайт указанный вместо названия кнопки.

## Функции для интерактивных взаимодействий 
- `$interactionReply` - ответ на сообщение без ошибки взаимодействия
- `$interactionUpdate` - обновляет сообщение при взаимодействии
- `$interactionEdit` - изменяет сообщение при взаимодействии
- `$interactionDelete` - удаляет сообщение, сделаное при помощи функции `$interactionReply`


### Взаимодействие только для автора (пример для кнопки)

```js
module.exports = [{
name: "ban",
code: `$addButton[1;Да!;3;wokinban_$authorID] //В названии функции нужно указать название кнопки и функцию $authorID
Забанить вокина?
$onlyIf[$hasPerms[$guildID;$authorID;admin]==true;]`
}, {
//Название не нужно указывать
type: "interaction",
prototype: "button",
code: `$ban[373838708673347584] //Код

$onlyIf[$advancedTextSplit[$interactionData[customId];_;2]==$interactionData[author.id];Вы не можете забанить вокина, потому что не являетесь автором кнопки!] //Проверка айди, который указан в названии кнопки + ошибка.
$onlyIf[$advancedTextSplit[$interactionData[customId];_;1]==wokinban;] //Проверка названия кнопки
