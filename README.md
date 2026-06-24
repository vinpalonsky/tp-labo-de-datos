## ¿Cómo arrancar proyecto por primera vez?

1. Instalar venv (si usas linux): sudo apt install python3-venv -y (ubuntu)

2. Crear ambiente de python:
   1. Cambiar al directorio del proyecto
   2. python3 -m venv .venv

3. Instalar dependecias en el ambiente:
   1. Cambiar al directorio del proyecto
   2. Activar ambiente:
      1. source .venv/bin/activate (linux)
      2. .venv\Scripts\Activate.ps1 (windows)
   3. Instalar dependencias:
      1. pip install -r requirements.txt

4. Elegir nuevo ambiente como kernel:
   1. Entrar al notebook
   2. Arriba a la derecha cambiar kernel al .venv

5. Instalar nuevas dependencias:
   1. Cambiar al directorio del proyecto
   2. Activar ambiente:
      1. source .venv/bin/activate (linux)
      2. .venv\Scripts\Activate.ps1 (windows)
   3. Instalar dependencia necesaria:
      1. pip install {dependencia}
   4. Actualizar requirements.txt:
      1. pip freeze > requirements.txt


## Consultas

Probar con los datos centrados.

### Limpieza y Procesamiento de Datos

Repasar lipmieza y preguntar si el proceso es correcto

### Análisis exploratorio

Agregar boxplot de precio valores en el mercado europeo

Promedio edades por confederacion

Añadir graficos

### PCA y Clustering


### Regresión y clasificación


### El 11 ideal de Argentina y Brasil

me quedaron solo dos mediocampistas para brasil en el once ideal, como hago? cambiar formacion