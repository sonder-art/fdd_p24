# Usa una imagen base de Python
FROM python:3.9-slim

# Establece el directorio de trabajo en /app
WORKDIR /app

# Codigo para manejar ambientes y el codigo necesario


# Instala las dependencias
Run pip install virtualenv
Run virtualenv -p python3.9 venv3.9
COPY requirements_pandas.txt .
COPY app.py .
Run . venv3.9/bin/activate
RUN pip install --no-cache-dir -r requirements_pandas.txt


# Define el comando por defecto para ejecutar la aplicación
CMD ["python", "app.py"]