## Спринт 9. API Yatube.
Yatube - прототип социальной сети, функционал которого позволяет публиковать новые записи, комментировать их, подписываться на авторов и отписываться от них и тд.
## Разворачиваем проект.
Клонируем репозиторий.
```
git clone https://github.com/qitoplu/api_final_yatube.git
```
Устанвливаем и активируем виртуальное окружение.
```
python -m venv venv
```
```
. venv/Scripts/activate
```
Устанавливаем зависимости.
```
pip install -r requirements.txt
```
Переходим в директорию проекта yatube_api.
```
cd yatube_api
```
Выполняем миграции.
```
python manage.py migrate
```
Запускаем проект.
```
python manage.py runserver
```
Готово.
## Примеры ответов API.
POST /api/v1/posts
```
{
"text": "string",
"image": "string",
"group": 0
}
```
GET /api/v1/posts/{id}/
```
{
"id": 0,
"author": "string",
"text": "string",
"pub_date": "2019-08-24T14:15:22Z",
"image": "string",
"group": 0
}
```
POST /api/v1/follow/
```
{
"user": "string",
"following": "string"
}
```
