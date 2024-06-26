**GeoPy** - модуль для [[Python|Python]], который предоставляет различные инструменты работы с географическими данными.

![[GeoPy.png]]

**Установка через cmd или terminal:**

```Python
pip install geopy
```

**Подключение в проект:**

```Python
import geopy
```

## Геокодирование

**Геокодирование:** Этот процесс преобразует текстовые адреса или названия мест в географические координаты. Геокодирование позволяет ассоциировать данные с конкретными местами на карте.

**Пример геокодирования при помощи GeoPy:**

```Python
geolocator = geopy.geocoders.Nominatim(user_agent="geoapiExercises")
address = "1600 Amphitheatre Parkway, Mountain View, CA"

location = geolocator.geocode(address)

print("Адрес:", address)
print("Широта:", location.latitude)
print("Долгота:", location.longitude)
```

## Пространственный анализ

**Пространственный анализ:** Это основной компонент геоаналитики, включающий в себя анализ пространственных паттернов, взаимосвязей и распределения. Методы включают в себя расчет расстояний, плотности, геокластеризацию и многое другое.

**Пример пространственного анализа при помощи GeoPy:**

```Python
cords1 = (41.49008, -71.312796)
cords2 = (41.499498, -81.695391)
print(geopy.distance.distance(cords1, cords2).km)
print(geopy.distance.great_circle(cords1, cords2).km)
```

**Конвертация и сравнение единиц измерения:**

```Python
print(geopy.distance.Distance(miles=10).km)
print(geopy.distance.Distance(kilometers=2) > geopy.distance.Distance(miles=1))
```
## Визуализация данных

**Визуализация данных:** Геоданные можно визуализировать на картах, используя различные инструменты и библиотеки. Визуализация делает информацию более наглядной и понятной.

**Пример визуализации данных при помощи GeoPy:**

```Python

```