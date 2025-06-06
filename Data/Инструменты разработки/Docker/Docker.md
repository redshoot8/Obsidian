**Docker** - это платформа, которая позволяет упаковать в контейнер приложение со всем окружением и зависимостями, а затем доставить и запустить его в целевой системе.

![[Docker.png]]

Приложение, упакованное в контейнер, изолируется от операционной системы и других приложений. Поэтому разработчики могут не задумываться, в каком окружении будет работать их приложение, а инженеры по эксплуатации — единообразно запускать приложения и меньше заботиться о системных зависимостях.

## Устройство и принцип работы Docker

Виртуализация в **Docker** реализуется на уровне ОС. Виртуальная среда запускается прямо из ядра основной операционной системы и использует её ресурсы.

В поставку **Docker** входят следующие компоненты:

- **Docker host** — это операционная система, на которую устанавливают Docker и на которой он работает.

- **Docker daemon** — служба, которая управляет Docker-объектами: сетями, хранилищами, образами и контейнерами.

- **Docker client** — консольный клиент, при помощи которого пользователи взаимодействуют с Docker daemon и отправляют ему команды, создают контейнеры и управляют ими.

- **Docker image** — это неизменяемый образ, из которого разворачивается контейнер.

- **Docker container** — развёрнутое и запущенное приложение.

- **Docker Registry** — репозиторий, в котором хранятся образы.

- **[[Dockerfile|Dockerfile]]** — файл-инструкция для сборки образа.

- **Docker Compose** — инструмент для управления несколькими контейнерами. Он позволяет создавать контейнеры и задавать их конфигурацию.

- **Docker Desktop** — GUI-клиент, который распространяется по GPL. Бесплатная версия работает на Windows, macOS, а с недавних пор и на Linux. Это очень удобный клиент, который отображает все сущности Docker и позволяет запустить однонодовый Kubernetes для компьютера.

## Основные команды

**Просмотр всех образов:**

```Shell
docker images
```

**Построение образа на основе [[Dockerfile|Dockerfile]]:**

```Shell
docker build -t my_image
```

**Запуск контейнера на основе образа:**

```Shell
docker run --name=my_container -p 8000:8000 my_image
```

**Подключение к консоли контейнера:**

```Shell
docker exec -it my_container bash
```

**Удаление контейнера:**

```Shell
docker rm my_container
```

