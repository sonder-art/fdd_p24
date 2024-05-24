# Use an official Python runtime as a parent image
FROM python:3.10-slim AS base

# Set the working directory in the container
WORKDIR /app

COPY requirements.txt /app/requirements.txt
RUN pip install --no-cache-dir -r requirements.txt


FROM base AS development

COPY requirements_dev.txt /app/requirements.txt
RUN pip install --no-cache-dir -r requirements_dev.txt
COPY . /app/
EXPOSE 8888
ENTRYPOINT ["jupyter", "lab", "--ip='*'", "--port=8888", "--no-browser", "--allow-root"]

FROM base AS production 
COPY . /app/
ENTRYPOINT ["python", "app.py"]