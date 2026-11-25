FROM python:3.10-slim
WORKDIR /app

# 1. Поставить пакеты из скачанной папки wheels
COPY wheels/ wheels/
RUN pip install --no-index --find-links=wheels grpcio protobuf typing-extensions

# 2. Скопировать всё остальное и запустить
COPY . .
CMD ["python", "-u", "main.py"]