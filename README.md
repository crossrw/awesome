# Некоторые полезные команды

## Удаление старых ядер:

```
sudo apt autoremove --purge
```

## Преобразование CRLF-> LF

```
perl -pi -e 's/\r\n/\n/g' input.file
```

## Обновление Node.js на Ubuntu

```
# Using Ubuntu
curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
sudo apt-get install -y nodejs
```

## Поиск самых больших файлов

```
find . -type f -printf '%s %p\n' | sort -nr | head -10
```

## GIT

### Инициализация локального репозитария

```
git init
```

### Глобальные настройки

```
git config --global user.name "Ivan Petrov"
git config --global user.email "ivan@petrov.ru"
```

### Просмотр URL удаленного репозитария

```
git remote -v
```

### Установка URL удаленного репозитария

```
git remote add origin http://xxx.xxxxxxxxx.xx/xx/xxxx.git
```

### Изменение URL удаленного репозитария

```
git remote set-url origin http://xxx.xxxxxxxxx.xx/xx/xxxx.git
```

### Добавление всего

```
git add .
```

### COMMIT в локальный репозитарий

```
git commit -m "text message"
```

### Перенос в удаленный репозитарий

```
git push -u origin master
```

### Создание новой ветки и переход в нее

```
git checkout -b <name>
```

### Создание новой ветки

```
git branch <name>
```

### Просмотр списка веток

```
git branch
```

### Переключение в другую ветку

```
git checkout <name>
```

### Текущий статус изменений

```
git status
```

### Слияние указанной ветки с текущей

```
git merge <name>
```

## CVS

### Создание нового проекта
1. Создать пустую папку по имени проекта, пойти в нее и...
2. cvs import <имя прроекта> a1 a2
3. Удалить созданную папку
4. cvs co <имя_проекта>

### Добавление модуля для WinCVS
1. Получаем папку CVSROOT: cvs co CVSROOT
2. Правим файл modules
3. cvs ci

### Получение проекта с сервера

```
cvs co -d <имя проекта>
```

### Создание среза проекта (тега)

```
cvs tag <имя тега>
```

### Создание ветки в проекте

```
cvs tag -b <имя ветки>
```

### Удаление тэга или ветки

```
cvs tag -dB <имя_тега>
```

Команда rtag - делает то же но с указанием имени модуля (проекта)

### Получение проекта определенного тэга или ветки

```
cvs co -r <имя тэга> <имя проекта>
```

### Откат изменений в одном файле
1. Удаляем файл
2. cvs update

### Откат одного файла к более ранней ревизии (к ревизии 1.3)

```
cvs update -j 1.5 -j 1.3 file.c
```

## Windows

### Получение путей и PID-ов сервисов

```
wmic process get ProcessID,ExecutablePath
wmic process where "name='name.exe'" get ProcessID, ExecutablePath
```

