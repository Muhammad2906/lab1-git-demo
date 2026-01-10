# Быстрый старт - Что делать дальше?

## ✅ Что уже сделано:

1. ✅ Создан локальный Git репозиторий
2. ✅ Добавлены файлы и сделано несколько коммитов
3. ✅ Продемонстрирована работа команд git add, git commit, git status

## 📋 Что нужно сделать вам:

### Шаг 1: Зарегистрируйтесь на GitHub
1. Перейдите на https://github.com/
2. Нажмите "Sign up"
3. Заполните форму регистрации
4. Подтвердите email

### Шаг 2: Создайте репозиторий на GitHub
1. Войдите в свой аккаунт GitHub
2. Нажмите кнопку "+" в правом верхнем углу → "New repository"
3. Заполните форму:
   - Repository name: `lab1-git-demo` (или любое другое имя)
   - Description: "Лабораторная работа №1 по Git"
   - Выберите "Public"
   - **НЕ** ставьте галочки на "Add a README file", "Add .gitignore", "Choose a license"
4. Нажмите "Create repository"

### Шаг 3: Подключите локальный репозиторий к GitHub
После создания репозитория GitHub покажет инструкции. Выполните в терминале:

```bash
# Перейдите в папку репозитория
cd lab1_git_demo

# Добавьте удаленный репозиторий (замените YOUR_USERNAME на ваше имя)
git remote add origin https://github.com/YOUR_USERNAME/lab1-git-demo.git

# Проверьте подключение
git remote -v

# Отправьте код на GitHub
git push -u origin main
```

**Важно:** Если GitHub попросит авторизацию, используйте Personal Access Token вместо пароля:
- Settings → Developer settings → Personal access tokens → Generate new token
- Выберите срок действия и права (repo)
- Скопируйте токен и используйте его как пароль

### Шаг 4: Проверьте результат
1. Обновите страницу вашего репозитория на GitHub
2. Вы должны увидеть все файлы
3. Скопируйте URL репозитория (например: https://github.com/YOUR_USERNAME/lab1-git-demo)

### Шаг 5: Сделайте скриншоты для отчета
Сделайте скриншоты:
1. Терминал с выполнением команд git status, git add, git commit
2. Терминал с выполнением git push
3. Страница вашего репозитория на GitHub
4. История коммитов (git log --oneline)

### Шаг 6: Подготовьте отчет
1. Откройте файл `REPORT_TEMPLATE.md`
2. Заполните все поля
3. Вставьте скриншоты
4. Укажите URL вашего репозитория на GitHub

### Шаг 7: Отправьте отчет
Отправьте отчет на email: a.vybornova@gmail.com

**Тема письма:**
```
Лаб 1. ПО ЦОД [ВАША_ГРУППА] [ВАША_ФАМИЛИЯ]
```

Например:
```
Лаб 1. ПО ЦОД ИКПИ-61 Иванов И.И.
```

---

## 🆘 Если что-то пошло не так:

### Проблема: Git не установлен
```bash
# macOS
brew install git

# Ubuntu/Debian
sudo apt-get install git
```

### Проблема: Ошибка при git push
Возможные причины:
1. Не настроен remote: `git remote add origin [URL]`
2. Нужна авторизация: используйте Personal Access Token
3. Конфликт веток: попробуйте `git pull origin main` перед push

### Проблема: Забыли настроить имя и email
```bash
git config --global user.name "Ваше Имя"
git config --global user.email "your.email@example.com"
```

---

## 📚 Полезные ссылки:

- Документация Git: https://git-scm.com/book/ru/v2
- GitHub Guides: https://guides.github.com/
- Интерактивный туториал: https://learngitbranching.js.org/?locale=ru_RU

---

**Удачи с выполнением лабораторной работы! 🚀**
