# git-test

Test project
Мы продолжаем работать с GIT

# 1. Внесли изменения из интерфейса GitHub + локально

```
echo "locale changes" >> README.md
git add README.md
git commit -m "locale changes in readme.md"
```

## Пытаемся запушить

```
git push origin main
```

# 2. Тренируемся работать с stash

## Делаем изменения без коммита

```
echo "Незавершенная работа" >> file.txt
```

## Внезапно нужно переключиться на fix

```
git status # покажет измененные файлы
```

## Сохраняем изменения в stash

```
git stash push -m "WIP: незавершенная работа над фичей"
```

или

```
git stash
```

## Проверяем что рабочая директория чистая

```
git status
```

## Переключаемся на другую ветку, делаем правки

```
git checkout -b hotfix
```

## ... делаем срочные правки ...

```
git add .
git commit -m "Срочный фикс"
git checkout develop
```

## Возвращаем наши изменения из stash

```
git stash list # смотрим список stash
git stash pop # возвращаем последний stash и удаляем его из списка
```

## Или если хотите просто применить без удаления:

```
git stash apply
```

# 3. Изменили файл в ветке develop

## Переключаемся на develop

```
git checkout develop
```

## Вносим изменения

```
echo "Create a new featute" >> feature.txt
git add feature.txt
git commit -m "added new feature in develop branch"
```
