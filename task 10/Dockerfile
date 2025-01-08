# Используем официальный Python образ как базовый
FROM python:3.9-slim

# Устанавливаем рабочую директорию в контейнере
WORKDIR /app

# Копируем requirements.txt в контейнер
COPY requirements.txt /app/

# Устанавливаем зависимости из requirements.txt
RUN pip3 install -r requirements.txt

# Копируем все файлы из текущей директории в контейнер
COPY . /app/

# Открываем порт 8000 для доступа к серверу
EXPOSE 8000

# Команда для запуска приложения
CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000"]
