# $interactionUpdate

## Описание
Обновляет сообщение при нажатии на кнопку / меню выбора

## Использование
```js
$interactionUpdate[контент;эмбеды;компоненты;файлы]
```

### Опции
Контент - контент сообщения
Эмбеды - эмбеды в виде {newEmbed:}
Компоненты - строка компонентов в виде {actionRow:}
Файлы - файлы, прикрепленные к сообщению

## Пример использования
```js
$interactionUpdate[Текст;{newEmbed:{description:Текст}};{actionRow:{button:Текст:2:customID}}]
```