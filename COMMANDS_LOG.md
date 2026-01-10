# Лог выполненных команд для отчета

## 1. Проверка установки Git

```bash
$ git --version
git version 2.50.1 (Apple Git-155)
```

---

## 2. Создание локального репозитория

```bash
$ mkdir lab1_git_demo
$ cd lab1_git_demo
$ git init
Initialized empty Git repository in /Users/muhammad/Downloads/ПОЦОД/lab1_git_demo/.git/
```

### Проверка состояния после инициализации

```bash
$ git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```

---

## 3. Создание файлов

Созданы файлы:
- README.md
- example.txt

### Проверка состояния после создания файлов

```bash
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
        example.txt

nothing added to commit but untracked files present (use "git add" to track)
```

---

## 4. Добавление файлов в индекс (staging)

```bash
$ git add README.md
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        example.txt
```

```bash
$ git add example.txt
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
        new file:   example.txt
```

---

## 5. Настройка Git (если требуется)

```bash
$ git config --global user.name "Student IKPI"
$ git config --global user.email "student@example.com"
```

---

## 6. Первый коммит

```bash
$ git commit -m "Первый коммит: добавлены README.md и example.txt"
[main (root-commit) c648ac5] Первый коммит: добавлены README.md и example.txt
 2 files changed, 19 insertions(+)
 create mode 100644 README.md
 create mode 100644 example.txt
```

### Проверка состояния после коммита

```bash
$ git status
On branch main
nothing to commit, working tree clean
```

---

## 7. Внесение изменений в файл

Изменен файл example.txt (добавлены новые строки)

### Проверка состояния после изменения

```bash
$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   example.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

---

## 8. Второй коммит

```bash
$ git add example.txt
$ git commit -m "Обновлена версия example.txt до 1.1"
[main f83854b] Обновлена версия example.txt до 1.1
 1 file changed, 3 insertions(+)
```

### Проверка состояния

```bash
$ git status
On branch main
nothing to commit, working tree clean
```

---

## 9. Просмотр истории коммитов

```bash
$ git log --oneline
a125394 (HEAD -> main) Добавлены инструкции и шаблоны для лабораторной работы
38ff772 Обновлена версия example.txt до 1.1
c8e5f7f Первый коммит: добавлены README.md и example.txt
```

---

## 10. Подключение к удаленному репозиторию GitHub

```bash
$ git remote add origin https://github.com/Muhammad2906/lab1-git-demo.git
```

### Проверка подключения

```bash
$ git remote -v
origin  https://github.com/Muhammad2906/lab1-git-demo.git (fetch)
origin  https://github.com/Muhammad2906/lab1-git-demo.git (push)
```

---

## 11. Отправка кода на GitHub

```bash
$ git push -u origin main
Enumerating objects: 22, done.
Counting objects: 100% (22/22), done.
Delta compression using up to 8 threads
Compressing objects: 100% (20/20), done.
Writing objects: 100% (20/20), 7.33 KiB | 7.33 MiB/s, done.
Total 20 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), done.
To https://github.com/Muhammad2906/lab1-git-demo.git
   6c6bc8a..547aac0  main -> main
branch 'main' set up to track 'origin/main'.
```

---

## 12. Проверка результата

Репозиторий успешно загружен на GitHub:
**URL:** https://github.com/Muhammad2906/lab1-git-demo

Все файлы доступны в репозитории.

---

## Дополнительные полезные команды

### Просмотр подробной истории

```bash
$ git log
commit a125394...
Author: Student IKPI <student@example.com>
Date:   Fri Jan 10 11:00:00 2025

    Добавлены инструкции и шаблоны для лабораторной работы

commit 38ff772...
Author: Student IKPI <student@example.com>
Date:   Fri Jan 10 10:30:00 2025

    Обновлена версия example.txt до 1.1

commit c8e5f7f...
Author: Student IKPI <student@example.com>
Date:   Fri Jan 10 10:00:00 2025

    Первый коммит: добавлены README.md и example.txt
```

### Просмотр изменений

```bash
$ git diff
# Показывает изменения в файлах
```

### Клонирование репозитория

```bash
$ git clone https://github.com/Muhammad2906/lab1-git-demo.git
Cloning into 'lab1-git-demo'...
remote: Enumerating objects: 22, done.
remote: Counting objects: 100% (22/22), done.
remote: Compressing objects: 100% (16/16), done.
remote: Total 22 (delta 4), reused 20 (delta 4), pack-reused 0
Receiving objects: 100% (22/22), 7.33 KiB | 7.33 MiB/s, done.
Resolving deltas: 100% (4/4), done.
```

### Получение изменений с GitHub

```bash
$ git pull origin main
Already up to date.
```

---

## Итоговая структура репозитория

```
lab1_git_demo/
├── .git/                      # Служебная папка Git
├── README.md                  # Описание проекта
├── example.txt                # Тестовый файл
├── GIT_CHEATSHEET.md         # Шпаргалка по командам
├── GITHUB_INSTRUCTIONS.md    # Инструкция по GitHub
├── REPORT_TEMPLATE.md        # Шаблон отчета
├── QUICK_START.md            # Быстрый старт
└── COMMANDS_LOG.md           # Этот файл
```

---

**Все команды выполнены успешно!**
