# API для социальной сети блогеров Yatube.
Yatube позволяет публиковать посты и картинки. Комментировать посты других пользователей. Подписываться на любимых авторов и отслеживать их обновления.

### Технологии используемые в проекте:
- Python 3.9
- Django
- Django Rest Framework
- Simple JWT
- Djoser

Необходимые для работы проекта зависимости описаны в файле requirements.txt

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/Mariooooo37/api_final_yatube
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python -m venv env
```

```
source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```

### Примеры API запросов и ответов:
GET - запрос на эндпоинт http://127.0.0.1:8000//api/v1/posts/

Вернет JSON со списком всех публикаций с пагинацией, доступны параметры limit и offset.

POST - запрос на эндпоинт http://127.0.0.1:8000//api/v1/posts/{post_id}/comments/

Создаст новый комментарий к выбранному посту.

DELETE - запрос на эндпоинт http://127.0.0.1:8000//api/v1/posts/{post_id}/comments/{id}/

Удалит выбранный комментарий, если вы являетесь автором поста.

Пример ответа API при GET - запросе на эндпоинт http://127.0.0.1:8000//api/v1/posts/{id}/
```
{
  "id": 0,
  "author": "string",
  "text": "string",
  "pub_date": "2023-03-01T21:22:23.263Z",
  "image": "string",
  "group": 0
}
```

Полный список эндпоинтов, с примерами запросов и ответов доступен по адресу:

http://127.0.0.1:8000/redoc/

## Об авторе:
Иванов Роман - студент Яндекс Практикум по курсу Python-разработчик.
