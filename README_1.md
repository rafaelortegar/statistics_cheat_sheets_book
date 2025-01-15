# Python_cheat_sheets_book
This repo contains a jupyter book with things to study if you are a python starter

# Using this repo

The purpose of this repository is to provide an example of using a Dockerfile to create a Jupyter Notebook environment capable of running Python with PySpark, Pandas, and packages specified in a `requirements.txt` file.

# Setting up things

1. Clone this repository.
2. Add your `requirements.txt` file or update the existing one with your desired dependencies.

The folder structure should look like this:
```
github_project_root
├── LICENSE
├── README.md
├── dockerfiles
│   └── Dockerfile_jupyter_python_pyspark
├── notebooks
│   └── testing pyspark.ipynb
└── requirements.txt
```

# How to run the code:

1. Open a terminal.
2. Navigate to the root of this repository.
3. Run the following commands:


```bash
# Build the Docker image
docker build -f dockerfiles/Dockerfile_jupyter_python_pyspark -t jupyter-pyspark .

# Run the Docker container
docker run -p 8888:8888 -v $(pwd):/notebooks -it jupyter-pyspark

# Activate the virtual environment
source /env/bin/activate

# Start Jupyter Notebook
jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser --allow-root
```

4. Open the test notebook located at: `notebooks/testing_pyspark.ipynb`.

pyenv activate python_cheat_sheets_book
pyenv virtualenv 3.10.12 python_cheat_sheets_book
pyenv local


# Jupyter Book Project with Docker

This project combines Jupyter Book, Jupyter Notebook, PySpark, and PostgreSQL in a Dockerized environment.

## Features
- Jupyter Book for creating professional documentation and tutorials.
- Jupyter Notebook for interactive code execution.
- PySpark for big data processing.
- PostgreSQL for database management.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/username/jupyter-book-project.git
   cd jupyter-book-project



######################
Pasos para Actualizar un Paquete
1. Actualizar el Paquete en tu Proyecto
Si estás usando Poetry, actualiza la versión del paquete directamente en el archivo pyproject.toml:

Actualiza el paquete con Poetry:

bash
Copiar código
poetry update numpy
Esto hará lo siguiente:

Actualiza numpy a la versión más reciente compatible (según las restricciones en pyproject.toml).
Regenera el archivo poetry.lock con la versión actualizada.
Si deseas instalar una versión específica:

bash
Copiar código
poetry add numpy@1.1
Verifica que los archivos pyproject.toml y poetry.lock estén actualizados:

bash
Copiar código
git status
2. Probar Localmente
Antes de actualizar el contenedor, asegúrate de que el proyecto funcione con el paquete actualizado:

Instala las dependencias en tu entorno local:

bash
Copiar código
poetry install
Ejecuta tus pruebas unitarias:

bash
Copiar código
pytest
Verifica que todo esté funcionando correctamente.

3. Actualizar el Contenedor de Docker
Reconstruir la Imagen de Docker: Como el contenedor utiliza las dependencias del archivo poetry.lock, necesitas reconstruir la imagen para incluir los cambios:

bash
Copiar código
docker build -t jupyter-dev-environment .
Ejecutar el Contenedor Actualizado: Inicia un nuevo contenedor basado en la imagen reconstruida:

bash
Copiar código
docker run -it -p 8888:8888 -p 8000:8000 -v $(pwd):/app jupyter-dev-environment
Verificar el Contenedor:

Prueba que el contenedor funcione correctamente con la versión actualizada de numpy.
Corre nuevamente las pruebas unitarias dentro del contenedor, si es necesario:
bash
Copiar código
pytest
4. Actualizar el Repositorio
Confirma los Cambios: Asegúrate de incluir los cambios en pyproject.toml y poetry.lock en tu commit:

bash
Copiar código
git add pyproject.toml poetry.lock
git commit -m "Update numpy to 1.1"
Sube los Cambios:

bash
Copiar código
git push origin main
5. Ejecutar las GitHub Actions
Cuando subes los cambios al repositorio, las GitHub Actions configuradas se ejecutarán automáticamente para:

Verificar el código con linters (Black, Flake8, Pre-Commit).
Ejecutar las pruebas unitarias con pytest para garantizar que la actualización no rompió nada.
Reconstruir el Jupyter Book, si es parte de tu flujo.
6. Validar el Entorno de Producción (Opcional)
Si estás usando el contenedor en producción, asegúrate de implementar la nueva imagen correctamente:

Etiqueta y publica la nueva imagen en un registro de contenedores (por ejemplo, Docker Hub):

bash
Copiar código
docker tag jupyter-dev-environment your-docker-repo/jupyter-dev-environment:latest
docker push your-docker-repo/jupyter-dev-environment:latest
Implementa la nueva imagen en tu servidor o infraestructura de despliegue.
