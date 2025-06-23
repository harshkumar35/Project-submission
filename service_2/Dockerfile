FROM python:3.11-slim

WORKDIR /app

COPY pyproject.toml .
RUN pip install --upgrade pip && pip install flask

COPY app.py .

EXPOSE 8002

CMD ["python", "app.py"]
