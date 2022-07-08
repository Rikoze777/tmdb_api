# tmdb_api
Упражнение на чтение кода. Фильмы с TMDB

## tmdb_helpers.py

Отвечает за взаимодействие с API сервисом TMDB.

*Вызывается другими скриптами*

- Отправляет запросы на themoviedb.org для создания БД
- Получает уникальный ключ
- Загружает JSON-ответы от сервисов

## make_own_db.py

Создает json-базу `MyFilmDB.json`, в котором хранится информация о 1000 фильмах.

### Использование

```bash
python3 make_own_db.py
Enter your api key v3:
please, wait, this operation may take smth like 15-20 minutes
0.0 percent complete
...
100.0 percent complete
```

## search_in_db.py

По ключевому слову ищет фильмы, в которых встречается ключевое слово.

### Использование
```bash
python3 search_in_db.py
Enter path to DataBase: ./MyFilmDB.json
Enter film to search for: Matrix
The Matrix
The Matrix Reloaded
The Matrix Revolutions
```

## own_db_helpers.py
Используется `search_in_db.py` и `find_similar.py`, чтобы получать информацию о фильмах.

## hello_api_TMDB.py
Проверяет работу `tmdb_helpers.py`, скачивает информацию о бюджете фильма под номером 215.

## find_similar.py

Ищет схожие фильмы, по следующим критериям:
- Бюджет
- Жанр
- Язык
- Коллекция

Выводит 8 совпадений.

### Использование
```bash
python3 find_similar.py
Enter path to DataBase: ./MyFilmDB.json
Enter film to search for: The Matrix
```
