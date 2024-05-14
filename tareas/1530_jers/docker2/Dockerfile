# Use an official Python runtime as a parent image
FROM python:3.9-slim AS base

# Set the working directory in the container
WORKDIR /app

COPY environment.yml /app/environment.yml

RUN conda env create -f /app/environment.yml

# Install Python and Jupyter packages
RUN pip install --no-cache-dir notebook jupyterlab

# Make port 8888 available to the world outside this container
EXPOSE 8888

# Run JupyterLab
CMD ["jupyter", "lab", "--ip='*'", "--port=8888", "--no-browser", "--allow-root"]
