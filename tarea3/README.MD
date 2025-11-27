

# Predicción de temperatura
Se realiza la predicción de temperatura utilizando técnicas de machine learning de una serie temporal

# Modelos_DT_KNN.ipynb
Enfocarse en los modelos de ML usados.
- DT
- KNN
- Gráfico de curva de aprendizje
- Análisis de Bias y Varianza
- Uso de K-means


# Analisis de Outliers

En cada archivo se reptiten cosas dado a que la investigación salió larga. Sin embargo
Se señala a qué debe prestarse atención en cada archivo ipynb

## notebook_1.ipynb

En este archivo se debe prestar atención a :
-  Interpolación de NA (las cuales fueron contabilizadas en archivos de predicción de temperatura)
- tendencia global de la temperatura sin MA12 + incertidumbre
- Tendencia de temperatura por cada país (5 x gráfico) sin MA12
- Gráfico interactivo de la evolución de la temperatura a través de los años ubicables en el mapa mundial interactivo
- Ranking de temperaturas gráfico final. Como ver este gráfico:
    - Cada columna es un mes
    - cada fila es contiene años para cada mes
    - Cada columna es de un largo de 10
    - En cada columna sea hace un top-10 de los años más calurosos ese mes, ordenados de mayor a menor.
    - Los años marcados en amarillo son los años superiores al año `2000` con el fin de ver el avance de los últimos en el ranking de aumento de temperaturas por mes

## outliers.ipynb
El primer análisis de ``outliers``. Se elige para explorar si existen relaciones con los volcanes en la temperatura mundial o local.

- Se elige todos los volcanes de categoría VEI 6 y 7  desde 1800 en adelante. El analisis de los datos igual es desde 1800 en adelante
- Calculo de la temperatura con media movil de 12 meses MA12
- Gráfico de temperatura MA12 con eventos de volcanes
- Descommposición de la temperatura en tendencia + ruido + estacionalidad
- calculo de ``z-score`` para comparar otros métodos para calcular los outliers
- Analisis de outliers del residuo que se observa que tiene algunas estructuras interesantes, usando Isolation forest.
- Gráfico de outliers del ruido


## outliers2.ipynb

- Se hace cruce de datos de las ciudades con un dataset de continentes + completado de NA finales de ciudades sin asignar a contnentes
- Preparación de features para pasarlo a los modelos de isolation forest y hdbscan
- Análisis de outliers usando una ciudad target 'Luanda' del país de 'Angola'
- Gráfico de tendencia de tempreatura + outliers marcados por isolation forest
- Gráfico de los volcanes que erupcionaron de clasificación de VEI mayor a 6 en el mundo
- Análisis de la temperatura del continente Oceanía usando u top 700 outliers (ya que cada ciudad tiene outliers, se llenaría de puntos) + marca de volcanes activos en oceanía (por tener tantos volcanes de categoría alta que erupcionaron)
- Lo mismo pero gráfico usando HDBSCAN
