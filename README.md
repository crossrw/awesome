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

## GIT

```
# Создание новой ветки и переход в нее
git checkout -b <name>

# Создание новой ветки
git branch <name>

# Просмотр списка веток
git branch

# Переключение в другую ветку
git checkout <name>

# Текущий статус изменений
git status

# Слияние указанной ветки с текущей
git merge <name>

```
