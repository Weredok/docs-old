# $playTrack

## Описание
Проигрывает заданный трек на заданной платформе. Выдаёт "Added (название трека) to queue". Для использования необходим дополнительный пакет [@akarui/aoi.music](https://npmjs.org/@akarui/aoi.music) с версией не ниже 1.2.0

## Использование
```js
$playTrack[платформа;трек/ссылка/путь]
```

### Опции
- `Платформа` - Платформа, на которой будет запрашиваться трек: youtube, soundcloud, spotify, localfile, url

## Пример использования
```js
$playTrack[youtube;Nightcore - Pheonix]
```
