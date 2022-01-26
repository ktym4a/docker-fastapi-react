FROM python:3.10-slim

WORKDIR /app

COPY /api/requirements.txt .

RUN pip install --no-cache-dir --trusted-host pypi.python.org -r requirements.txt

COPY /api/main.py .
EXPOSE 8000

CMD ["uvicorn", "main:app", "--reload", "--host", "0.0.0.0", "--port", "8000"]
