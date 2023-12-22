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
>1. **Carga del Archivo CSV:** Se cargó los archivos CSV correspondientes a los diferentes cultivos DataFrames utilizando la biblioteca pandas.
>
>2. **Sanitización de los DataFrame:** Para asegurar la calidad de los datos, se aplicó la función `sanitizar_dataframe` a todos estos DataFrames para manejar posibles valores NaN y otras prácticas de saneamiento.
>
>### Exploración de Datos
>
>3. **Tipos de Datos:** Se verificaron los tipos de datos de las columnas de los DataFrames para garantizar la coherencia en el análisis.
>
>### Visualización de Tendencias
>
>4. **Gráfico de Tendencia de Características del Cultivo:**
>   - Se utilizó Plotly Express para crear un gráficos lineales que muestrna la tendencia de las características de los diferentes cultivos a lo largo del tiempo.
>   - Se graficaron las variables 'superficie_sembrada_ha', 'superficie_cosechada_ha' y 'produccion_t'.
>   - El eje X representa el tiempo (Año), y el eje Y representa los valores de las variables.
>   - Se asignaron colores distintivos para cada variable ('superficie_sembrada_ha': azul, 'superficie_cosechada_ha': naranja, 'produccion_t': verde).
>
>5. **Gráfico de Rendimiento de Cultivo por Año:**
>   - Se creó otro gráfico lineal para visualizar la tendencia del rendimiento del cultivo por año.
>   - El eje x representa el tiempo (Año), y el eje y representa el rendimiento en kg/ha ('rendimiento_kgxha').
>   - Se utilizó Plotly Express para la creación del gráfico lineal.
>
>### Generalización del Proceso
>
>Estos pasos de carga, sanitización y visualización de datos se aplicaron de manera similar a varios cultivos, como avena, girasol, trigo, soja y centeno. Los DataFrames resultantes para cada cultivo, como `df_avena`, `df_girasol`, `df_trigo`, `df_soja`, y `df_centeno`, permitieron un análisis comparativo de las tendencias de producción y rendimiento a lo largo de los años en Argentina.
>
>Este enfoque sistemático proporciona una visión integral de las características agrícolas en Argentina, permitiendo la identificación de patrones, análisis de tendencias y toma de decisiones informadas en el sector agrícola.
>## 3. Análisis Exploratorio de Datos (Continuación)
>
>Investigando la estimación de produccion de trigo y soja a fondo, desde un DataSet que contiene la producción de todos los cultivos, discriminando por provincia, departamento y más características de todo el territorio Argentino
> ### Proceso de Preparación de Datos para Análisis Exploratorio
>
>En esta sección, llevamos a cabo una serie de pasos para preparar y organizar el conjunto de datos de estimación de producción.
>
>1. **Organización de Datos:** Utilizamos una función personalizada (`organizar_datos`) para reestructurar el DataFrame y facilitar su manipulación.
>
>2. **Exploración Inicial:** Mostramos el DataFrame resultante y observamos sus dimensiones (153889 filas y 12 columnas).
>
>3. **Manipulación de Tipos de Datos:** Verificamos los tipos de datos de las columnas y notamos que todos son del tipo 'Object' ('O'). Convertimos las columnas relevantes a tipos numéricos para facilitar análisis futuros, tratando posibles valores no numéricos.
>
>4. **Saneado de Datos:** Aplicamos un proceso de saneado para abordar posibles valores nulos ('NaN') y asegurar la calidad de los datos.
>
>5. **Ajuste de Tipos de Datos:** Finalmente, convertimos las columnas numéricas a tipos de datos enteros para representación precisa y evitar posibles errores.
>
>###  Análisis y Filtrado de Datos Relevantes
>
>6. **Selección de Columnas Relevantes:**
>   - Identificamos las columnas críticas para nuestro análisis, incluyendo información sobre la provincia, departamento, cultivo, superficie sembrada, superficie cosechada, producción y rendimiento.
>
>7. **Exploración de Columnas Seleccionadas:**
>   - Mostramos el nuevo DataFrame resultante después de la selección de columnas y examinamos las columnas disponibles.
>
>8. **Tipos de Datos de Columnas Seleccionadas:**
>   - Verificamos que las columnas relevantes ahora tienen tipos de datos numéricos adecuados para facilitar su manipulación y análisis.
>
>9. **Exploración de Valores Únicos en Columnas:**
>   - Identificamos los valores únicos en las columnas 'cultivo' y 'provincia' para comprender la variedad de cultivos y las provincias disponibles en el conjunto de datos.
>
>10. **Filtrado por Cultivo - Trigo:**
>    - Seleccionamos y mostramos datos específicos para el cultivo de trigo a nivel nacional ('Trigo total').
>
>11. **Filtrado por Cultivo - Soja:**
>    - Seleccionamos y mostramos datos específicos para el cultivo de soja a nivel nacional, incluyendo todas las filas donde el nombre del cultivo contiene la palabra "soja".
>
>Estos pasos nos permiten centrarnos en datos específicos relevantes para el análisis exploratorio de la producción agrícola de trigo y soja en Argentina, facilitando la comprensión y la interpretación de resultados.
>
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
