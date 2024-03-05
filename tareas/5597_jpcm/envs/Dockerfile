# Usa una imagen base de Python
FROM python:3.9-slim

# Establece el directorio de trabajo en /app
WORKDIR /app

# Codigo para manejar ambientes y el codigo necesario
# Instala virtualenv
RUN pip install virtualenv

# Crea un entorno virtual dentro del contenedor
RUN virtualenv venv
COPY requirements_pandas.txt .
COPY app.py .
RUN pip install -r requirements_pandas.txt
# Define el comando por defecto para ejecutar la aplicación
CMD ["python", "app.py"]