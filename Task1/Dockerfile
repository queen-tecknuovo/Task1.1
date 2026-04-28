FROM python:3.10-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY app.py .

ENV YOUR_NAME=Queen

EXPOSE 5500

CMD ["python", "app.py"]
