## Описание:
Проект предназначен для работы с API социальной сети Yatube. 
Регистрация, создание, редактирование и удаление постов, группы, подписки и комментарии.

## Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:
```
git clone git@github.com:Absent-kai/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```
Зайти в папку джанго-проекта:

```
cd yatube_api
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

## Примеры запросов к API:

*http://127.0.0.1:8000/api/v1/posts/*

 **POST:**

 - Request samples

 `{
  "text": "string",
  "image": "string",
  "group": 0
}`

 - Response samples

`{
  "id": 0,
  "author": "string",
  "text": "string",
  "pub_date": "2019-08-24T14:15:22Z",
  "image": "string",
  "group": 0
}`

*http://127.0.0.1:8000/api/v1/posts/{id}/*

**PUT:**
 - Request samples

 `{
  "text": "string",
  "image": "string",
  "group": 0
}`

 - Response samples

`{
  "id": 0,
  "author": "string",
  "text": "string",
  "pub_date": "2019-08-24T14:15:22Z",
  "image": "string",
  "group": 0
}`

*http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/*

**GET:**
 - Response samples

`[
  {
    "id": 0,
    "author": "string",
    "text": "string",
    "created": "2019-08-24T14:15:22Z",
    "post": 0
  }
]`

*http://127.0.0.1:8000/api/v1/follow/*

**POST:**
 - Request samples

 `{
  "following": "string"
}`

 - Response samples

`{
  "user": "string",
  "following": "string"
}`
