# Usar una imagen base oficial de Python
FROM python:3.8-slim

# Establecer el directorio de trabajo en el contenedor
WORKDIR /app

# Copiar los archivos de requisitos primero para aprovechar la caché de capas de Docker
COPY requirements_pandas.txt .

# Instalar virtualenv en el contenedor
RUN pip install --no-cache-dir virtualenv

# Crear un entorno virtual dentro del contenedor
RUN virtualenv venv

# Activar el entorno virtual
ENV PATH="/app/venv/bin:$PATH"

# Instalar las dependencias usando el entorno virtual
RUN pip install --no-cache-dir -r requirements_pandas.txt

# Copiar el resto del código fuente de la aplicación en el contenedor
COPY . .

# Comando para ejecutar la aplicación
CMD ["python", "app.py"]

