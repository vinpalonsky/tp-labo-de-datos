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

### Limpieza y Procesamiento de Datos

4. las reemplazaria por 0 porque significa que no hubo tiros

5. se me ocurre que se podría reemplazar los valores por 0 excepto aquellos donde exista alguna variable similar en otro grupo (como partidos como titular o minutos jugados). Esto generaría correlación entre las variables?

6. En los puntos 4 y 5 se me pregunta cómo resolvería sin eliminar columnas, pero en este punto me dicen que deben quedar aprox 850 jugadores y 30 variables numericas. Entonces, los puntos anteriores son solo teóricos? En esta parte limpio a criterio propio?
Estaría correcto eliminar las variables de keeper_?
Reseteo el index antes o despues de borrar filas? Digo porque las filas se borran por indice
Está bien esto de ir iterando para limpiar los datos? (por ej: borro las variables con menor del 60% de cobertura y el resto las manejo de manera más detallada)
Me quedaron 45 variables numericas y 920 jugadores, esta bien?

Hay que usar graficos para la limpieza de datos? (como plotbox)

### Análisis exploratorio


### PCA y Clustering

Hay que hacerlo con el dataframe df_selecciones no? (me quedaron 46 selecciones y 43 variables numericas, esta ok?)

2. Cómo deberia interpretar a z1 y z2?

3. Para kmeans vimos algun método de elección del hiperparámetro K?

4. Está bien el análisis del gráfico y los clusters?
Igualmente considero que las primeras dos componentes principales no resumen bien la info

5. No entiendo muy bien la consigna. Sería describir qué explica cierto cluster segun los pesos de z1 y z2? Por ejemplo, en mi caso diría que los equipos naranjas son los de peor rendimiento
