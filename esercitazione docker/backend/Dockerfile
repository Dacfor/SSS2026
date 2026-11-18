FROM python:3.11-slim
WORKDIR /app

# Copia ed installa le dipendenze
COPY ./requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copia tutto il codice dell'applicazione (non solo main.py)
COPY . .

EXPOSE 8000

# Comando di avvio fisso (come da slide 30)
ENTRYPOINT ["python", "-m", "uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]