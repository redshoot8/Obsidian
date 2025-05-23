**Pip** - это официальный менеджер пакетов для [[Python|Python]]. Он позволяет легко устанавливать, обновлять и управлять библиотеками [[Python|Python]], что делает разработку намного эффективнее.

**Основные возможности pip:**

- Позволяет легко устанавливать и обновлять библиотеки [[Python|Python]].

- Управляет зависимостями между пакетами.

- Обеспечивает изоляцию проектов через виртуальные среды.

- Предоставляет доступ к огромному репозиторию PyPI (Python Package Index).

![[pip.png]]

**Установка/обновление pip:**

```Shell
python -m pip install --upgrade pip
```

**Проверка версии pip:**

```Shell
pip --version
```

## Основные команды pip

### Установка

**Установка одного пакета:**

```Shell
pip install package_name
```

**Установка конкретной версии:**

```Shell
pip install package_name==1.0.0
```

**Установка из файла зависимостей:**

```Shell
pip install -r requirements.txt
```

### Удаление

**Удаление пакета:**

```Shell
pip uninstall package_name
```

**Принудительное удаление пакета:**

```Shell
pip uninstall package_name -y
```

### Просмотр установленных пакетов

**Просмотр установленных пакетов:**

```Shell
pip list
```

**Создание файла зависимостей:**

```Shell
pip freeze > requirements.txt
```

**Просмотр информации о конкретном пакете:**

```Shell
pip show package_name
```

## Расширенные возможности

### Виртуальные среды

Создание [[Виртуальные окружения|виртуальных окружений]].

### Поиск пакетов

**Поиск пакетов:**

```Shell
pip search search_term
```

**Загрузка пакетов без установки:**

```Shell
pip download package_name
```

**Установка из локального архива:**

```Shell
pip install /path/to/package_name.whl
```

### Разрешение конфликтов

**Проверка конфликтов зависимостей:**

```Shell
pip check
```

**При возникновении проблем с правами доступа:**

```Shell
python -m pip install --user package_name
```

## Лучшие практики

- Лучше использовать `python -m pip` вместо просто `pip` для предотвращения проблем с путями.

- [[Виртуальные окружения|Виртуальные окружения]] следует использовать для каждого проекта.

- Регулярно обновлять **pip** до последней версии.

- Создавать файлы requirements.txt для повторяемости окружения.

- Проверять зависимости перед установкой новых пакетов.