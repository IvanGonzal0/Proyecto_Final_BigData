# Proyecto Final Big Data & Machine Learning (UPSO)

Este es el README del Proyecto Final de Big Data & Machine Learning, desarrollado como parte del curso en la UPSO.

> [!NOTE]
>
> ## 1. Inicio
> ## `Introducción`
> El proyecto tiene como objetivo principal realizar un análisis exhaustivo del rendimiento y producción de dos de los cultivos más significativos en Argentina: trigo y soja. La iniciativa trata de proporcionar una comprensión detallada de los patrones de producción a > nivel nacional.
>
>## `Objetivos del proyecto`
>
>Agricultura
>
>● **Análisis de Producción**: Evaluar y comparar el rendimiento anual de diferentes granos, poniendo mayor énfasis y haciendo un análisis mas exhaustivo para el trigo y la soja analizando su nivel de producción en todas las provincias y departamentos de Argentina.
>
>● **Exploración Geoespacial**: Utilizar algoritmos de clustering para identificar diferentes niveles de producción de trigo y soja en las diferentes regiones geográficas Argentinas.
>
>● **Visualización Interactiva**: Generar gráficos y visualizaciones interactivas que permitan a los usuarios explorar los datos de producción y rendimiento de manera intuitiva y amigable.
>
>
>## `Justificación`
>Argentina es un actor clave en la producción agrícola a nivel mundial, y el trigo y la soja son fundamentales para nuestra economía. Entender las variaciones en la producción a nivel regional es esencial para interiorizarse en los niveles de producción de cada región >en nuestro país.
>
>
>## `Alcance del Proyecto`
>El alcance abarca la totalidad del territorio argentino, examinando datos a nivel de provincias y localidades. Se emplearán técnicas de análisis de datos, visualización y algoritmos de clustering para ofrecer una visión integral y detallada de los patrones de >producción de trigo y soja.

> [!IMPORTANT]
>## 2. Análisis Exploratorio de Datos
>
>### Carga y Sanitización de los DataFrames
>
>Sección dedicada al análisis exploratorio de datos para los siguientes cultivos:
>- Avena
>- Maíz
>- Girasol
>- Trigo
>- Soja
>- Centeno
>
>## 3. Análisis Exploratorio de Datos (Continuación)
>
>Esta parte del proyecto aborda la estimación de la producción para los cultivos de Trigo, Soja y Yerba Mate.
>
>## 4. Clustering
>
>Después de una larga investigación de las estimaciones agrícolas argentinas, procedemos con el clustering para la estimación del Trigo por departamento. A continuación, se describen los pasos:
>
>### Estimación del Trigo
>
>- Por departamento
>- Selección de variables de entrada
>
>#### Busqueda del K (Número de clusters) Óptimo
>
>Iteramos sobre un rango de posibles números de clusters (k) y calculamos la suma de errores cuadrados (SSE) para cada k. Los resultados se visualizan en el siguiente gráfico, donde se observa la relación entre el número de clusters y la SSE. Este proceso nos permite >identificar un punto en la curva donde la SSE comienza a estabilizarse, indicando el número óptimo de clusters.
>
>#### Creación del Modelo KMeans
>
>Creamos una instancia del modelo KMeans de la librería SKLearn, especificando el número óptimo de clusters identificado anteriormente, que en este caso puede ser 3 o 4, pero se optó por 4 luego de diferentes pruebas. La inicialización se llevó a cabo con una semilla >aleatoria (random_state=42) para garantizar reproducibilidad.
>
>#### Resultados y Visualización
>
>- Agregamos la etiqueta de clusters al DataFrame
>- Visualización de los resultados
>- Etiquetado de niveles de producción
>
>### Visualización de Resultados por Provincia
>
>Primero reutilizamos el DataFrame filtrado en el punto anterior por cultivo de Trigo y a partir de ese DF reducimos las columnas a las que son de nuestro interés para el modelo. Luego agrupamos el nuevo DataFrame por provincias y hacemos una sumatoria de todas las >columnas numéricas.
>
>### Estimación de la Soja
>
>El proceso para la estimación de la Soja sigue una metodología similar a la del Trigo.
>
>#### Resultados y Visualización
>
>- Agregamos las etiquetas de clusters al DataFrame
>- Visualización de los resultados
>- Etiquetado de niveles de producción
>
>### Visualización de Resultados por Provincia (Soja)
>
>Primero reutilizamos el DataFrame filtrado en el punto anterior por cultivo de Soja y a partir de ese DF reducimos las columnas a las que son de nuestro interés. Luego agrupamos el nuevo DataFrame por provincias y hacemos una sumatoria de todas las columnas numéricas.

> [!TIP]
>## Conclusiones
>
>### Reflexión de la Primera Parte del Proyecto
>Los análisis sobre la producción y rendimiento de granos en Argentina revelan tendencias clave 
>y factores determinantes de su evolución. Se destaca el notorio aumento en la superficie 
>destinada a la siembra de soja y maíz, influenciado por la creciente demanda global, precios 
>históricamente elevados, y políticas gubernamentales de apoyo. En contraste, la disminución 
>de la superficie para centeno y girasol se atribuye a la baja demanda mundial y la competencia 
>con cultivos más rentables como la soja y el maíz. Además, el incremento general del 
>rendimiento de todos los granos se vincula con avances tecnológicos y la expansión de áreas 
>agrícolas
>### Reflexión de la Segunda Parte del Proyecto
>La relación positiva entre la superficie cosechada y la producción de soja en diferentes 
>departamentos es evidente. Este patrón indica que una mayor área dedicada a la cosecha se 
>traduce en una producción más significativa. Asimismo, la relación entre la superficie 
>sembrada y cosechada refleja que un aumento en la siembra generalmente conlleva a una 
>cosecha proporcionalmente mayor. Estos hallazgos respaldan la importancia de la superficie 
>dedicada a la cosecha y siembra en la determinación de los niveles de producción tanto para el 
>trigo como para la soja.
