# Usa la imagen base de Jupyter DataScience
FROM jupyter/datascience-notebook:latest

# Cambia al usuario root para instalar herramientas adicionales
USER root

# Instala git, wget, y otras herramientas necesarias
RUN apt-get update && apt-get install -y \
    git \
    wget \
    curl \
    vim \
    && rm -rf /var/lib/apt/lists/*

# Cambia al usuario jupyter para ejecutar el contenedor
USER $NB_UID

# Expone el puerto para Jupyter Notebook
EXPOSE 8888

# Inicia Jupyter Notebook por defecto
CMD ["start-notebook.sh"]
