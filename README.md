# API для социальной сети YaTube

## Описание
*Реализован функционал дающий возможность:*
- Подписываться на пользователя.
- Просматривать, создавать новые, удалять и изменять посты.
- Просматривать и создавать группы.
- Комментировать, смотреть, удалять и обновлять комментарии.
- Фильтровать по полям.

*Ключевые моменты:*
- Применяйте вьюсеты (viewsets)
- Для аутентификации используйте JWT-токены.
- У неаутентифицированных пользователей доступ к API только на чтение.
- Исключение — эндпоинт /follow/.
- Аутентифицированным пользователям разрешено изменение и удаление своего контента; в остальных случаях доступ предоставляется только для чтения.

## Установка
1. Клонируйте репозиторий

```git clone git@github.com:Dron-71/api_final_yatube.git```


2. Переходите в проект ```cd api_final_yatube```


3. Cоздать и активировать виртуальное окружение: 

```python3 -m venv venv```

```source venv/bin/activate```


4. Установить зависимости из файла requirements.txt: 

```pip install -r requirements.txt```

```pip install django-filter```


5. Выполнить миграции 

```python3 manage.py migrate```


6. Перейти в директорию ```cd yatube_api```


7. Запустить проект

```python3 manage.py runserver```


8. Получить токен для доступа к API.


Делаем POST-запрос на ```http://127.0.0.1:8000/api/v1/token/```

передав поля username и password


9. Передавайте токен(access) в Hearders:

```Authorization: Bearer <токен>.```


### *Документация для API Yatube*

```http://127.0.0.1:8000/redoc/```
