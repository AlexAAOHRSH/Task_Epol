```sh
pip install pipenv
pipenv shell
pipenv install
python app.py
```
Локальный сервер
http://127.0.0.1:5000/

GET:

/api/tasks
#Получить все таски

/api/tasks/items
#Получить элементы тасков

/api/tasks/name=<значение>
#Получить все таски, в name которых есть значение

/api/tasks/status=<значение>
#Получить все таски, status которых равен значению

/api/tasks?start_date_from=<значение>
#Получить все таски, start_date которых больше или равен значения(ю) (дату прописывать в формате %Y-%m-%d)

/api/tasks?end_date_to=<значение>
#Получить все таски, end_date которых меньше или равен значения(ю) (дату прописывать в формате %Y-%m-%d)

/api/tasks/items?value=<значение>
#Получить все элементы тасков, value которых содержит значение

/api/tasks/items?task_id=<значение>
#Получить все элементы таска с id равным зачению

POST:

/api/tasks
#Создать задачу

/api/tasks/items
#Создать элемент задачи (id задачи, к которой нужно привязать, прописывается в task_id)

PUT:

/api/tasks/<int:task_id>
#Изменить задачу

/api/tasks/items/<int:task_item_id>
#Изменить элемент задачи

DELETE:

/api/tasks/<int:task_id>
#Удалить такс со всеми элементами

/api/tasks/items/<int:task_item_id>
#Удалить элемент
