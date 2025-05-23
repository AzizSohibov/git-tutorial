---
title: Полное руководство по Git
author: Aziz Sokhibov (created using DeepSeek AI)
date: 2025-19-04
---

# 🚀 Полное руководство по Git 
_Для начинающих и не только_

![Git Logo](https://git-scm.com/images/logo@2x.png)

---

## Содержание
1. [Основные команды](#-основные-команды)
2. [Работа с ветками](#-работа-с-ветками)
3. [Слияние и конфликты](#-слияние-и-конфликты)
4. [Отмена изменений](#-отмена-изменений)
5. [Работа с удалёнными репозиториями](#-работа-с-удалёнными-репозиториями)
6. [Полезные советы](#-полезные-советы)

---

## 🔧 Основные команды

### Инициализация репозитория
```bash
git init
git add .
git commit -m "Первый коммит"
```
### Просмотр изменений
```bash
git status       # Показать статус
git diff         # Сравнить рабочую директорию и индекс
git diff --staged # Сравнить индекс и последний коммит
```
---

## 🌿 Работа с ветками

### Создание и переключение
```bash
git branch new-feature    # Создать ветку
git checkout new-feature  # Переключиться
```
# Или сокращённо:
```bash
git checkout -b hotfix    # Создать и переключиться
```
### Удаление веток
```bash
git branch -d old-branch  # Удалить локальную ветку
git push origin --delete old-branch # Удалить ветку на сервере
```
---

## 🔄 Слияние и конфликты

### Быстрое слияние (Fast-Forward)
```bash
git checkout main
git merge feature
```
### Решение конфликтов
1. Найдите конфликтующие участки в файлах:
  ```bash
   <<<<<<< HEAD
   Ваш код
   =======
   Код из ветки
   >>>>>>> feature
   ```
2. Исправьте и сохраните файл.
3. Завершите слияние:
  ```bash
   git add .
   git commit -m "Исправление конфликтов"
   ```
---

## ⏪ Отмена изменений

### Отмена в рабочей директории
```bash
git restore file.txt      # Вернуть к последнему коммиту
git restore --staged file # Убрать из индекса
```
### Исправление коммита
```bash
git commit --amend -m "Новое сообщение"
```
---

## ☁️ Работа с удалёнными репозиториями

### Настройка
```bash
git remote add origin https://github.com/user/repo.git
git push -u origin main  # Первый пуш
```
### Синхронизация
```bash
git pull                # Получить изменения
git fetch               # Скачать без слияния
git push                # Отправить изменения
```
---

## 💡 Полезные советы

1. **.gitignore** – создайте файл чтобы игнорировать:
  ```bash
   node_modules/
   *.log
   .env
   ```
2. **Короткие статусы**:
  ```bash
   git status -s  # Компактный вывод
   ```
3. **Визуализация истории**:
  ```bash
   git log --graph --oneline --all
   ```
---

## Пример рабочего процесса

# 1. Начать новую фичу
```bash
git checkout -b feature/login
```
# 2. Редактировать файлы
```bash
nano login.html
```
# 3. Добавить изменения
```bash
git add login.html
git commit -m "Добавлена форма входа"
```

# 4. Отправить на сервер
```bash
git push -u origin feature/login
```
# 5. Создать Pull Request на GitHub
---

    
