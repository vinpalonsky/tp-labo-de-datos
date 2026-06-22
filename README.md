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

Las selecciones no son necesariamente eficaces por sus modos de juegos, simplemente tienen un estilo y ya

CAF y AFC mucho mas defensivo que ataque diria, la mayora estan sobre el 0 de ataque pero positivo en defensa

### PCA y Clustering

Hay que hacerlo con el dataframe df_selecciones no? (me quedaron 46 selecciones y 43 variables numericas, esta ok?)

2. Cómo deberia interpretar a z1 y z2?

3. Para kmeans vimos algun método de elección del hiperparámetro K? Tengo que justificar por que elegimos kmeans?

4. Está bien el análisis del gráfico y los clusters?
Igualmente considero que las primeras dos componentes principales no resumen bien la info

5. No entiendo muy bien la consigna. Sería describir qué explica cierto cluster segun los pesos de z1 y z2? Por ejemplo, en mi caso diría que los equipos naranjas son los de peor rendimiento

### Regresión y clasificación

1. No esta clara la consigna. Este df_jugadores_regresion lo tengo que usar par 2. y 3.? O para que lo estamos armando?
De que me sirve estimar el total de partidos de la liga con el maximo de partidos jugados por los jugadores de cada confederacion?

2. "(excluir todas las variables de cantidad de partidos jugados y minutos jugados)" refiere a las que usamos para armar la nueva variable "partidos_liga" o a todas las que incluyan cualquier tipo de esa métrica (como "caps", "standard_playing_time_starts" o "shooting_90s"). Cuando saco mas variables funciona mucho peor el modelo (lo cual tiene sentido), es esa la idea?
arme un modelo lineal multivariado y otro Ridge. El ridge funciono claramente mejor. Basta con esto?
Puedo buscar el alpha optimo utilizando GridSearchCV/RidgeCV o tengo que hacerlo a mano? Igual me da mejor resultado probando a mano, tiene sentido esto?
El grafico de los alpha no me esta dando bien, por qué es?
Qué hago con todos los warnings de las filas mal condicionadas? Si hago un escalamiento previo de los datos se arregla, pero me empeoran los resultados

3. El KNN a mano (es decir con leave_one_out) funciona mejor que KNeighborsClassifier, tiene sentido esto? Yo pense que quiza si porque para KNeighborsClassifier estamos separando en X_train y X_test y entonces el rendimiento solo se basa en un porcentaje de nuestros datos, no con todos como en leave_one_out
Puede que sea porque uno utiliza NearestNeighbors y el otro KNeighborsClassifier?
Usando posiciones_tm funciona todo mucho peor, eso lo incluimos o nos quedamos directo con posicion?

### El 11 ideal de Argentina y Brasil

No le veo mucho sentido a predecir las posiciones con los datos que entrenamos al mismo clasificador, ya que es la misma informacion. Estaraia bien hacer, una vez encontrado el mejor K, una especie de leave_one_out pero para clasificar las nuevas posiciones en vez de testear el modelo?

La verdad no predijo muy bien la seleccion titular jajajaj era esperado esto?
Viendo los RECM y accuracy tiene sentido, pues ninguo superaba el 0.7