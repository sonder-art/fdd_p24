# Usa una imagen base de Python
FROM python:3.9-slim

# Establece el directorio de trabajo en /app
WORKDIR /app

# Copia el archivo de requisitos al contenedor
COPY requirements.txt .

# Instala las dependencias
RUN pip install --no-cache-dir -r requirements.txt

# Copia todo el código al contenedor
COPY . /app

#RUN touch archivo_imagen_docckerfile.txt

# Define el comando por defecto para ejecutar la aplicación
# Termina el Dockerfile, debes de agregar las lineas necesarias
# para que al momento de dat `docker run -it {contenedor}` se imprima lo pedido