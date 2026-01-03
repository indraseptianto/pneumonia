FROM python:3.11-slim

WORKDIR /app

COPY requirements.txt /app/requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Create directory for MLflow backend store
RUN mkdir -p /app/mlruns

EXPOSE 1709

CMD ["mlflow", "server", "--host", "0.0.0.0", "--port", "1709", "--backend-store-uri", "sqlite:///mlflow.db"]