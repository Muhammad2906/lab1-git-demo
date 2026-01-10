# Инструкция по подключению к GitHub

## Шаги для загрузки репозитория на GitHub:

### 1. Зарегистрируйтесь на GitHub
Перейдите на https://github.com/ и создайте аккаунт

### 2. Создайте новый репозиторий на GitHub
- Нажмите кнопку "New repository" или "+"
- Введите название репозитория (например, "lab1-git-demo")
- Выберите "Public" для открытого репозитория
- НЕ добавляйте README, .gitignore или лицензию (у нас уже есть файлы)
- Нажмите "Create repository"

### 3. Подключите локальный репозиторий к GitHub
После создания репозитория GitHub покажет URL. Выполните команды:

```bash
# Добавьте удаленный репозиторий (замените YOUR_USERNAME на ваше имя пользователя)
git remote add origin https://github.com/YOUR_USERNAME/lab1-git-demo.git

# Проверьте, что удаленный репозиторий добавлен
git remote -v

# Отправьте код на GitHub
git push -u origin main
```

### 4. Проверьте результат
Обновите страницу вашего репозитория на GitHub - вы должны увидеть все файлы

## Дополнительные команды:

### Клонирование репозитория с GitHub
```bash
git clone https://github.com/YOUR_USERNAME/lab1-git-demo.git
```

### Получение изменений с GitHub
```bash
git pull origin main
```

### Отправка изменений на GitHub
```bash
git add .
git commit -m "Описание изменений"
git push origin main
```

## Для отчета вам понадобится:
1. URL вашего репозитория на GitHub (например: https://github.com/YOUR_USERNAME/lab1-git-demo)
2. Скриншоты выполнения команд в терминале
3. Скриншот репозитория на GitHub
