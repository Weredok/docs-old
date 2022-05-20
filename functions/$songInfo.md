# $songInfo

## Описание
Выдаёт информацию о треке. Для использования необходим дополнительный пакет [@akarui/aoi.music](https://npmjs.org/@akarui/aoi.music) с версией не ниже 1.2.0

## Использование
```js
$songInfo[опция;позиция]
```

### Опции
  - `Опция` - Опция информации, которую должен выдать бот

      - `thumbnail` - превью видео (только для youtube / soundcloud / spotify)
            
      - `title` - название видео
       
      - `description` - описание видео (только для youtube / soundcloud)
      
      - `url` - ссылка на трек
      
      - `authorUrl` - ссылка на автора трека (только для youtube / soundcloud / spotify)
      
      - `likes` - количество лайков под треком (только для youtube / soundcloud)
      
      - `views` - количество просмотров видео (только для youtube)
      
      - `duration` - длительность трека в миллисекундах
      
      - `path` - путь к файлу трека (только для localfile)
      
      - `dir` - папка с файлов трекаи (только для localfile)
      
          
- `Позиция` - позиция трека, информацию о котором нужно получить
- 
## Пример использования
```js
Название трека: $songInfo[title]
Описание трека: $if[$songInfo[description]!=;$songInfo[description];не найдено]
Ссылка на трек: $songInfo[url]
```
