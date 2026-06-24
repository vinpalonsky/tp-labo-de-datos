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

Esta bien el nombre del notebook

Probar con minmax scaler. O con los datos centrados.

### Limpieza y Procesamiento de Datos

2. El rango etario se agrega al df original?

5. se me ocurre que se podría reemplazar los valores por 0 excepto aquellos donde exista alguna variable similar en otro grupo (como partidos como titular o minutos jugados). Esto generaría correlación entre las variables?

6. Reseteo el index antes o despues de borrar filas? Digo porque las filas se borran por indice
No puedo reemplazar los NA en misc_ y standard_ por 0 en vez de eliminar filas? No le veo mucho sentido a borrar filas
con la segunda opcion de dataframe me da raro los alfa de ridge, por que?

1. esta bien el promedio de keeper_?

Repasar lipmieza y preguntar si el proceso es correcto

### Análisis exploratorio

Las selecciones no son necesariamente eficaces por sus modos de juegos, simplemente tienen un estilo y ya
Revisar de vuelta las conclusiones

### PCA y Clustering

1. Escale con minmax en vez de standardscaler para que quede todo positivo y poder interpretar mejor z1 y z2. Está bien?

2. Intente hacer el promedio de los arqueros aparte pero tanto z1 como z2 igual le dan peso a las variables de arquero. Está tomando si son eficientes o por cantidad?

3. Deberia usar standardscaler en vez de minmax?
hace falta el +1 en NearestNeighbors? esta bien el codigo y los indices?

4/5. cómo los puedo leer ahora que estan las variables de keeper?
Me está dando 0.89 de varianza acumulada ahora, es por minmax?

### Regresión y clasificación

2. es multivariado el modelo lineal no? que diferencia tiene polinomial de multivariado?
cambia si escalamos con standardscaler o minmax? hay alguno correcto?
para ridge hay que escalar no? esta bien si escalo todo el X?
con la segunda opcion de dataframe me da raro los alfa de ridge, por que?
para el modelo multivariado no tiene sentido hacer validacion cruzada no?

### El 11 ideal de Argentina y Brasil

me quedaron solo dos mediocampistas para brasil en el once ideal, como hago?