**FastAPI** — это мощный и современный фреймворк для создания веб-приложений на [[Python|Python]], который поддерживает [[Асинхронность|асинхронные]] запросы и имеет хорошую производительность.

![[FastAPI.png]]

**FastAPI** позволяет быстро создавать API с высокой производительностью благодаря использованию [[Python|Python]] типов и [[Асинхронность|асинхронных функций]]. Основные особенности **FastAPI**:

1.  **Автоматическая генерация документации**: [[Автоматическая документация FastAPI|автоматическая документация]] благодаря использованию OpenAPI и JSON Schema.

2.  **Поддержка асинхронности**: использование [[Асинхронность|async и await]].

3.  **Валидация данных**: с помощью [[Pydantic|Pydantic]] моделей и [[Аннотации типов|аннотаций типов]].

4.  **Простота и гибкость**: схожесть с [[Flask|Flask]], но с более широкими возможностями.

**Установка через cmd или terminal:**

```Shell
pip install fastapi
```

**Подключение в проект:**

```Python
import fastapi
```

**Для запуска веб-приложений на FastAPI требуется использовать пакет uvicorn:**

```Python
pip install uvicorn
```

*Запуск:*

Команда запуска имеет следующий формат: uvicorn {script_name}:{application_name} other_parameters

```Python
uvicorn main:app --reload
```

Также можно использовать метод run() из данного пакета

```Python
uvicorn.run(app, host='127.0.0.1', port=8000)
```

**Простое веб-приложение на FastAPI:**

```Python
from fastapi import FastAPI

app = FastAPI(title='Simple App')


@app.get("/")  
def read_root():  
    return {'message': 'Hello, World!'}  
  
  
@app.get("/items/{item_id}")
def get_item_id(item_id: int):  
    return {'item_id': item_id,  
            'message': f'Item id is {item_id}'}


if __name__ == '__main__':
    uvicorn.run(app, host='127.0.0.1', port=8000)
```
