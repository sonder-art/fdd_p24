# Virtualenv
Debes crear un virtualenv en tu local siguiendo las siguientes instrucciones. Investiga las instrucciones y adaptalas al repositorio actual. 

## Ejercicio
Crea un pyenv para este repo y anota las instrucciones en formato de codigo de markdown en este README (abajo), tanto para instalar el env como para activarlo. La idea es que si se te olvida o alguien mas descarga este repo puedas copiar y pegarlas sin ningun problema. No hagas `add` o `commit` por que falta crear los `ignores` (instrucciones mas adelante).  

Para asegurarte que funciono correctamente debe ser capaz de ejecutar `python app.py` sin problemas.

### Instrucciones
#### Instalacion
```
# Instalar pyenv utilizando Homebrew en macOS:
brew upgrade
brew install pyenv

# Agrega esto al final de tu archivo .bashrc, .bash_profile, o .zshrc:
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init --path)"

# Instalar versión de python
pyenv install 3.9  
```
#### Activar virtualenv
```
cd tareas/1530_jers
pyenv local 3.9  # Especifica la versión de Python que acabas de instalar
git clone https://github.com/pyenv/pyenv-virtualenv.git $(pyenv root)/plugins/pyenv-virtualenv
pyenv virtualenv 3.9 fdd_jers  # Elige un nombre para tu entorno virtual
pyenv activate fdd_jers # Activar el entorno virtual
```

# Conda
Instrucciones para crear un ambiente de conda `environment.yml.` Adapta las instrucciones al repositorio actual, no son exactas.

## Ejercicio
Crea un conda env para este repo y anota las instrucciones en formato de codigo de markdown en este README (abajo), tanto para instalar el env como para activarlo. La idea es que si se te olvida o alguien mas descarga este repo puedas copiar y pegarlas sin ningun problema. No hagas `add` o `commit` por que falta crear los `ignores` (instrucciones mas adelante).  

Para asegurarte que funciono correctamente debe ser capaz de ejecutar `python app.py` sin problemas.


### Instrucciones
#### Instalacion
`conda conda create --name fuentes_env python=X.Y
`
#### Activar conda env
`conda activate fuentes_env `


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

# Entrega de Ejercicios
Una vez que esten los ejercicios listos, sube tu imagen de docker a tu repositorio de docker hub y agrega la liga de ese contenedor aqui:  
## Docker
[https://hub.docker.com/repository/docker/elcachorrohumano/intro_docker_jers/general](url)  
## Github
Pide un pull request con las modificaciones necesarias.