# Tutorial Flask - Capitulo 1

## Objetivo

Generar un "hello world" paso a paso para crear una aplicación web basado en lenguaje de programación Python sobre el Framework Flask.

## Pre-requisitos

- Tener instalado Python 3
- Tener configurado Python por medio de línea de comando
- Tutorial realizado sobre sistema operativo Windows 10

## Comencemos

Creamos un ambiente virtual de Python con el siguiente comando.

```
>python -m venv myvenv  
``` 

Para activar este nuevo ambiente virtual, es necesario ejecutar el archivo activate.bat que se encuentra en la carpeta myvenv creada por Python.

```
>cd myvenv/Scripts
>activate.bat
```

Una vez que se activa el ambiente virtual, el prompt cambiará y quedará de la siguiente manera.

```
(myvenv) C:\workspace\flask-login>
```

Luego debemos instalar las dependencias de Flask dentro del ambiente virtual que hemos creado y para ello utilizamos el siguiente comando.

```
pip install flask
``` 

Con un editor de texto, crear los siguientes tres archivos.

```
1. app.py
3. requirements.txt
4. .gitignore
```

Las dependencias que vayamos agregando, debemos configurarlas en nuestro archivo requirements.txt, para ello ejecutamos el comando pip freeze, cuya salida la volcaremos en el archivo requirements.txt.

```
pip freeze > requirements.txt
```

Luego configuramos el archivo .gitignore para ignorar los archivos de Python que no formaran parte del proyecto, para ello agregamos el siguiente contenido en el archivo.

```
myvenv/

*.pyc
__pycache__/

instance/

.pytest_cache/
.coverage
htmlcov/

dist/
build/
*.egg-info/
```

Agregar el siguiente código fuente en el archivo app.py

```
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello, World!'
```
