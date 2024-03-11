# Virtualenv
Debes crear un virtualenv en tu local siguiendo las siguientes instrucciones. Investiga las instrucciones y adaptalas al repositorio actual. 

## Ejercicio
Crea un pyenv para este repo y anota las instrucciones en formato de codigo de markdown en este README (abajo), tanto para instalar el env como para activarlo. La idea es que si se te olvida o alguien mas descarga este repo puedas copiar y pegarlas sin ningun problema. No hagas `add` o `commit` por que falta crear los `ignores` (instrucciones mas adelante).  

Para asegurarte que funciono correctamente debe ser capaz de ejecutar `python app.py` sin problemas.

### Instrucciones
#### Instalacion
`pip install ....`
`pip install virtualenv`
#### crear virtualenv
`virtualenv venv1`
`virtualenv -p python3.9 venv3.9`
para especificar una versión de python específica
#### Activar virtualenv
`activate .... `
`source venv3.9/bin/activate`

# Conda
Instrucciones para crear un ambiente de conda `environment.yml.` Adapta las instrucciones al repositorio actual, no son exactas.

## Ejercicio
Crea un conda env para este repo y anota las instrucciones en formato de codigo de markdown en este README (abajo), tanto para instalar el env como para activarlo. La idea es que si se te olvida o alguien mas descarga este repo puedas copiar y pegarlas sin ningun problema. No hagas `add` o `commit` por que falta crear los `ignores` (instrucciones mas adelante).  

Para asegurarte que funciono correctamente debe ser capaz de ejecutar `python app.py` sin problemas.

Con virtual env o conda:
'pip install -r requirements_pandas.txt'
'python app.py'

### Instrucciones
#### Instalacion
`conda  ....`
`conda create --name condaenv python=3.12`
decir la version o 3.x si no sw necesita una version
#### Activar conda env
`conda activate condaenv`

# .gitignore
Algunos ambientes virtuales como `pyenv` pueden crear carpetas, asegurate de no subir estas carpetas. Esto lo puedes lograr omitiendo el add a estas careptas y aregandolas al .gitignore.  
No se aceptaran tareas que traigan archivos binarios de python, solo debe subirse el codigo. Tambien debe evitarse subir tus archivos `.env` o claves en general por ello es necesario incluir estos archivos en el gitignore, pero agregar un ejemplo al github para que se pueda replicar en el local en este caso lo llamos `.env_ejemplo`.

## Ejercicio
Crea tu `.gitignore` en tu copia de esta carpeta en tu folder de tareas verifica como funciona el wild card notation para lograr que aplique a todas tus subcarpetas.
*Tienes que investigar, inferir, googlear que carpetas son creadas para agregarlas al .gitignore*
Asegurate de agregar todas las cosas necesarias a tu `.gitignore` para que no suba archivos de los envs de python ni de conda a github

# .dockerignore
Igual que git, docker tiene su archivo .gitignore. Y dado que el punto de construir `build` un contenedor es hacer replicable todo dentro del mismo por lo que copiar estos archivos es mala practica por que peude provocar errores o aumentar la memoria.  Por lo mismo es necesario crear un  `.dockerignore`
## Ejercicio
Crea tu `.gitignore` en tu copia de esta carpeta en tu folder de tareas verifica como funciona el wild card notation para lograr que aplique a todas tus subcarpetas.
*Tienes que investigar, inferir, googlear que carpetas son creadas para agregarlas al .dockerignore*
Asegurate de agregar todas las cosas necesarias a tu `.gitignore` para que no suba archivos de los envs de python ni de conda a tu imagen de dockerhub.

# Docker
Ahora tienes que crear un docker que utilice `virtualenv` (no pipenv sino virtual env) para instalar los paquetes. Modifica el `Dockerfile.ejemplo` para que instale las cosas correspondientes y pueda ejecutar `python app.py` sin problemas. 
`docker build -t penv3.9:1.0.0 .`
`docker run penv3.9:1.0.0`

`docker tag penv3.9:1.0.0 jero110/envs:latest`
`docker push jero110/envs:latest`

# Entrega de Ejercicios
Una vez que esten los ejercicios listos, sube tu imagen de docker a tu repositorio de docker hub y agrega la liga de ese co sntenedor aqui:  
## Docker
[liga de docker](https://hub.docker.com/repository/docker/jero110/envs/general)  
## Github
Pide un pull request con las modificaciones necesarias.