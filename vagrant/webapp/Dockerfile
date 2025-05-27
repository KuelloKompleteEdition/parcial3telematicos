FROM python:3.10-slim

WORKDIR /app

COPY . /app

RUN apt-get update && apt-get install -y \
    default-libmysqlclient-dev \
    build-essential \
    pkg-config \
    && rm -rf /var/lib/apt/lists/*

RUN pip install --no-cache-dir Flask==2.3.3 flask-cors Flask-MySQLdb Flask-SQLAlchemy

EXPOSE 5000

CMD ["python", "run.py"]