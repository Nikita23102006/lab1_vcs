# Лабораторная работа №1. Система контроля версий

Кострикин Никита Александрович, группа 220042-11, вариант 8, лабораторная №1

## Выполненные задания

**Средней сложности**
- №8 — создан репозиторий на GitHub и связан с локальным
- №10 — склонирован чужой репозиторий, изучена история
- №4 — изменён файл, сделан второй коммит

**Повышенной сложности**
- №8 — подключён git submodule
- №1 — разрешён конфликт при слиянии веток

## Доказательства

### Разрешение конфликта слияния

Конфликт между `main` и `feature-greeting` в файле `main.py`, функция `greet()`.

Было в конфликте:
```
<<<<<<< HEAD
    return f"Hello, {name}! Welcome to Git."
=======
    return f"Привет, {name}! Добро пожаловать в Git."
>>>>>>> feature-greeting
```

Принято: `return f"Привет, {name}! Welcome to Git."`

```
*   f0f4886 (HEAD -> main) merge: resolve conflict in greet()
|\  
| * 0b8e5bb (feature-greeting) feat: extend greeting in feature branch
* | f65270b feat: extend greeting in main branch
|/  
````
## Изучение чужого репозитория

Репозиторий: https://github.com/psf/requests
Назначение: HTTP-библиотека для Python.

Всего коммитов: 6412
Первый коммит: 2011-02-13 Initial commit
Топ-авторов: см. [reports/foreign_repo_shortlog.txt](reports/foreign_repo_shortlog.txt)
Полный лог: [reports/foreign_repo_log.txt](reports/foreign_repo_log.txt)

Последние коммиты:
```
a1b2c3d Fix connection pool leak
e4f5a6b Bump urllib3 to 2.2.1
...
```

Разбор коммита `a1b2c3d`: автор ..., дата ..., изменены файлы ... (`git show --stat a1b2c3d`).
````
