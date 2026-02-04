## CI/CD Pipeline
### Стек:
 - poetry: управление зависимостями и виртуальным окружением
 - ruff: линтер и форматтер
 - pytest: юнит-тесты
 - docker: финальная упаковка

### Jobs:
 - code-quality (CI): проверка кода
 - docker-build (CD): упаковка кода

### Локальный CI
```bash
# 1. Установка зависимостей
poetry install

# 2. Форматирование кода
poetry run ruff format .

# 3. Линтинг
poetry run ruff check . --fix

# 4. Запуск тестов
poetry run pytest
```