FROM python:3.10-slim

WORKDIR /app

COPY requirements.txt .
RUN pip config set global.timeout 100 && \
    pip install --no-cache-dir -r requirements.txt -i https://pypi.org/simple/ --retries 5

COPY . .

CMD ["python","app.py"]