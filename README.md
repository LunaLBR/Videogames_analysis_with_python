# PROYECTO “Video Game Sales and Ratings con Python” 🎮

INTEGRANTES, EQUIPO 30: 
- ⭐ Luna Bela Dangú Hernández - lbdan19@gmail.com
- ⭐ Laura Berenice Luna Reyes - lauralunr@gmail.com
- ⭐ Carolina Chi Arceo - carochiar@gmail.com

## 1. Introducción
Los videojuegos son una de las formas más populares de entretenimiento a nivel mundial. 🌍 El éxito de un juego depende de diversos aspectos como la plataforma en la que se juega, su género, las opiniones de los críticos y usuarios, así como las ventas en distintas regiones. A veces no es fácil ver las conexiones entre los datos, pero al analizarlos es posible encontrar patrones que puedan explicar por qué algunos videojuegos tienen más éxito que otros en el mercado. Este proyecto analiza datos mundiales de videojuegos para estudiar cómo la plataforma, el género y las calificaciones influyen en las ventas a nivel global y regional.

## 2. Objetivo general
Procesar un conjunto de datos de videojuegos para explorar la relación entre las ventas globales y regionales, las plataformas, los géneros, las puntuaciones de críticos y usuarios, con el fin de identificar patrones que puedan influir en el éxito comercial de los videojuegos. 📈

## 3. Objetivos específicos
- Limpiar y organizar la base de datos obtenida para garantizar que los datos estén listos para su análisis. 🧹
- Analizar la relación entre las ventas globales y las ventas por región (Norteamérica, Europa, Japón y otras) para determinar si alguna región domina el mercado. 🌐
- Comparar el éxito de diferentes plataformas (PS4, Xbox, PC, etc.) en las ventas globales y regionales. 🕹️
- Evaluar la influencia de las puntuaciones de críticos y usuarios en las ventas totales de los videojuegos. ⭐
- Explorar las tendencias de ventas según el género del videojuego identificando los géneros más exitosos en cada región. 📊

## 4. Planteamiento del problema
La industria de los videojuegos enfrenta un desafío constante: identificar los factores clave que determinan el éxito comercial de un título. 🎮 Si bien elementos como la plataforma y el género de un juego son considerados determinantes, aspectos adicionales como las calificaciones de críticos, las preferencias de diferentes regiones y el momento del lanzamiento también pueden desempeñar un papel crucial. 

En un mercado en constante crecimiento, se espera que las ventas de un videojuego puedan ser predichas en función de las tendencias y las preferencias de los consumidores. 📈 Sin embargo, existe una desconexión frecuente entre las calificaciones y las ventas: un juego altamente valorado no siempre se traduce en grandes ventas, y los títulos más vendidos no necesariamente obtienen las mejores críticas. Este proyecto busca analizar un conjunto de datos de videojuegos con el fin de descubrir qué características tienen mayor influencia en las ventas globales y regionales, y cómo estas variables están interrelacionadas.

## 5. Preguntas de investigación
- ¿Cuántos videojuegos tienen información incompleta o nula en términos de ventas o puntuaciones? ❓
- ¿Cuál es el rango de ventas en las diferentes regiones (Norteamérica, Europa)? 🌍
- ¿Qué plataformas generan mayores ventas globales? 💰
- ¿Qué géneros de videojuegos son los que mayor se venden? 🏆
- ¿Cuál es la distribución de los videojuegos por género y plataforma? 📊
- ¿Qué relación existe entre las puntuaciones de críticos y usuarios y las ventas globales? ⭐
- ¿Podemos usar la puntuación de críticos y usuarios para predecir las ventas globales?
- ¿Existen diferencias significativas en las ventas según el año de lanzamiento de los videojuegos? 📅
- ¿Hay juegos con buenas calificaciones que venden poco? ¿Y juegos mal calificados que venden mucho? 🤔

## 6. Posible solución
La solución consistirá en implementar un proceso de limpieza y procesamiento de datos utilizando Python y las bibliotecas de pandas y numpy. 🐍 Se abordarán tareas como la eliminación de valores nulos, la normalización de las puntuaciones, y el cálculo de las ventas totales por región. Luego, se realizarán análisis estadísticos para identificar patrones en las ventas según las características de los videojuegos. Visualizaciones como gráficos de barras y de líneas serán empleadas para facilitar la interpretación de los resultados y responder las preguntas planteadas. 📊✨

## 7. Pasos y resultados

### ¿Cuántos videojuegos tienen información incompleta o nula en términos de ventas o puntuaciones?
La función `isnull()` busca los valores nulos. La aplicamos inicialmente para la limpieza de datos, y nos muestra la cantidad de datos nulos en cada columna. 🔍

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/1.png)

**Resultados:**

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/2.png)

El resultado de la ejecución fue variado. En ventas, no tenemos valores nulos, por lo tanto, no se modificará. En el caso de las puntuaciones, obtuvimos bastantes valores `NaN`. Nuestra solución fue llenar estos datos nulos con `fillna()`, reemplazando los valores de las puntuaciones con valores generados aleatoriamente en base al promedio de los datos de la columna correspondiente. ⚙️

### ¿Cuál es el rango de ventas en las diferentes regiones (Norteamérica, Europa, Japón)?
El código calcula el rango de ventas de videojuegos en distintas regiones (Norteamérica, Europa, Japón y otras) mediante la diferencia entre las ventas máximas y mínimas registradas en cada área. 📊 Se utilizó un diccionario que asocia las columnas de ventas con nombres reales, se iteró sobre cada región, se calculó el rango de ventas y se imprimió.

**Por Región:**

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/3.png)

**Global:**

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/4.png)

Se utilizó la función `.max()` para encontrar el valor máximo de ventas y la función `.min()` para el valor mínimo. La diferencia entre estos dos valores se almacenó en variables específicas para cada región.

**Resultados:**
- **Por Región:**

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/5.png)

- **Global:**

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/6.png)

Estos resultados indican que hay variaciones significativas en las ventas de videojuegos entre las diferentes regiones. 🌍 La cobertura de ventas en Norteamérica y Europa es particularmente alta en comparación con otras regiones, lo que indica que estas son regiones clave en el mercado de los videojuegos. 

Las ventas globales de **82,52 millones** demuestran el potencial y la diversidad del mercado global de videojuegos, aunque también indican que las ventas pueden variar significativamente entre los diferentes títulos de juegos. 📈

## ¿Qué plataformas generan mayores ventas globales?
Para agrupar los datos de ventas por plataforma se utilizó `groupby()`, además de `sum()` para obtener el total de ventas globales. Posteriormente, se utilizó `sort_values(ascending=False)` para ordenar las plataformas de mayor a menor según lo anterior. 📊

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/7.png)

**Resultados:**

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/8.png)

- **PlayStation 2** es la consola con mayores ingresos globales en la historia de los videojuegos, seguida de **Xbox 360** y **PlayStation 3**.
- Las consolas de **Nintendo**, como **Nintendo Wii** y **Nintendo DS**, también se encuentran entre las consolas más vendidas, lo que demuestra su fuerte presencia en el mercado. 🎮

## ¿Qué géneros de videojuegos son los que mayor se venden?
Se realizó un análisis de las ventas globales totales de cada género de videojuego. Se agruparon los datos por género y luego se sumaron las ventas globales para cada uno de ellos. 🏆

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/9.png)

**Resultados:**
- Los géneros más vendidos son **Action** (1,771.73 millones), **Sports** (1,350.61 millones) y **Shooter** (1,086.67 millones), destacando la popularidad de los juegos dinámicos y competitivos a nivel mundial.

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/10.png)

## ¿Cuál es la distribución de los videojuegos por género y plataforma?
Se realizó un análisis de cómo se agrupan los videojuegos según su género y plataforma. Iniciamos cuantificando los videojuegos según su tipo.

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/11.png)

Luego por plataforma

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/12.png)

Posteriormente ambos (género y plataforma). 

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/13.png)

Finalmente, se ordenaron con el top 10 de los más relevantes. 📈

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/14.png)


**Resultados:**

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/15.png)

- Los resultados muestran que **Action** (3,410), **Sports** (2,380), y **Misc** (1,773) son los géneros con más videojuegos.
- En términos de plataformas, las más populares son **PlayStation 2** (2,188), **Nintendo DS** (2,164), y **PlayStation 3** (1,359).
- Al combinar género y plataforma, se observa que **Sports** en **PlayStation 2** tiene la mayor cantidad de videojuegos (402), seguido de **Misc** en **Nintendo DS** (392) y **Action** en **PlayStation 3** (383).

# ¿Qué relación existe entre las puntuaciones de críticos y usuarios y las ventas globales?
### 🎮 Elaboramos un Pairplot de las Columnas de Interés de Ventas y Scores 📊

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/pairplot.png)

- **Posible correlación positiva** entre las **ventas en diferentes regiones** (NA, EU, JP, etc.) y las **ventas globales**.  
  - Esto sugiere que, si un juego vende bien en una región, es probable que **también lo haga en otras**. 🌎

- **Leve correlación positiva** entre las **puntuaciones de críticos y usuarios** y las **ventas globales**.  
  - Esta relación es un poco **más débil** en comparación con la correlación entre las **ventas regionales**.

- **Correlación positiva entre `critic_score` y `user_score`**.  
  - Esto tiene **sentido**, ya que si un juego es **bueno**, es probable que reciba **buenas reseñas** tanto de **críticos** como de **usuarios**. 🎮✨
  - 
### **Columnas Numéricas Seleccionadas**  
Elegimos las siguientes columnas numéricas de interés:  
- `'na_sales'
- `'eu_sales'
- `'jp_sales'  
- `'other_sales'
- `'global_sales'
- `'critic_score' 
- `'user_score' 

---
### 📊 **Generación de Matriz de Correlación y Heatmap**  
A continuación, generamos una **matriz de correlación** para ver las relaciones entre las diferentes variables. Luego, la representamos visualmente en un **heatmap**.

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/heatmap.png)

### 🌍 Ventas por Región  
- Vemos una **posible correlación positiva** entre las **ventas en diferentes regiones** (NA, EU, JP, etc.) y las **ventas globales**.  
  - Esto nos sugiere que, si un juego **vende bien en una región**, es probable que **también lo haga en otras**.

---

### 🎯 Puntuaciones y Ventas  
- Observamos una **correlación positiva** entre las **puntuaciones de críticos y usuarios** y las **ventas globales**.  
  - Sin embargo, esta relación es **más débil** que la **correlación entre las ventas regionales**.

---

### 📝 Correlación entre `critic_score` y `user_score`  
- Existe una **correlación positiva** entre las puntuaciones de **críticos y usuarios**.  
  - Esto tiene **sentido**, ya que si un juego es **bueno**, es probable que reciba **buenas reseñas** tanto por parte de **críticos** como de **usuarios**. 🎮✨

### 📈 Scatterplot de las Columnas de Interés  

El gráfico de Puntuación de criticos y usuarios muestra un comportamiento esperado, a medidad que aumentan las puntuaciónes de los criticos aumentan las ventas globales:

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/scatterplot1.png)


El siguiente gráfico de dispersión muestra una **relación interesante** entre la **puntuación de los usuarios** y las **ventas globales** de los videojuegos.

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/scatterplot2.png)

- Observamos que **algunos juegos con puntuaciones cercanas a 0** tienen **ventas sorprendentemente altas**.  

---

### 🔍 **Posibles Explicaciones**  
- **Falta de reseñas**: Puede tratarse de juegos recién lanzados o de nicho, con poca retroalimentación de usuarios.  
- **Estrategias de marketing agresivas**: Campañas publicitarias que impulsan las ventas iniciales, independientemente de la calidad del juego.  


# ❓ ¿Podemos Predecir las Ventas Globales Usando Puntuaciones de Críticos y Usuarios?

El **valor de R² promedio** obtenido nos indica que nuestras **variables predictoras** (puntuaciones de críticos y usuarios) explican apenas un **5.44%** de la **variabilidad en las ventas globales**. 📉  

---

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/crossvalidate.png)


### 🔍 **Interpretación**  
- Esto sugiere que las **puntuaciones de críticos y usuarios**, por sí solas, **no son suficientes** para explicar de manera significativa las **ventas globales** de los videojuegos.  
- Es probable que **otras variables importantes** influyan de manera significativa en el éxito comercial, como:

  - **Género del juego** 🎮  
  - **Plataforma de lanzamiento** 🕹️  
  - **Presupuesto de marketing** 📢  
  - **Fecha de lanzamiento** 🗓️

---

### 🧠 **Resultados**  
Aunque las puntuaciones pueden tener cierta **influencia**, es claro que no son los únicos factores que determinan las ventas globales. Un análisis más profundo que considere estas **variables adicionales** podría mejorar la capacidad de **predicción** del modelo y brindar una comprensión más completa de los **factores que impulsan las ventas** en la industria de los videojuegos. 🚀📊  

# Análisis de Clusters de Videojuegos: Relación entre Puntuaciones y Ventas Globales

El clustering permite identificar patrones en las puntuaciones de los críticos y usuarios en relación con las ventas. Esto ayuda a entender qué elementos pueden influir en el éxito comercial de un videojuego.

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/clusters.png)

## Posibles Interpretaciones de los Clusters

Basándonos en la distribución de los puntos en el gráfico, podemos hacer algunas inferencias sobre lo que cada cluster podría representar:

- **Cluster 1 (color morado)**: Videojuegos independientes o de nicho. Estos juegos suelen tener puntuaciones de crítica más bajas y ventas globales más modestas. Podrían ser juegos indie, juegos con temáticas muy específicas o juegos que no han recibido una gran promoción. Otra opción son videojuegos que se volvieron populares debido al marketing.

- **Cluster 2 (color verde)**: Videojuegos de gran éxito comercial. Estos juegos suelen tener puntuaciones de crítica moderadas a altas y ventas globales muy altas. Son los juegos que todos conocemos y que suelen estar en las listas de los más vendidos.

- **Cluster 3 (color amarillo)**: Videojuegos con alta puntuación de crítica pero bajas ventas. Este cluster podría incluir juegos que han sido muy bien recibidos por la crítica, pero que no han logrado alcanzar un gran éxito comercial. Podrían ser juegos con mecánicas de juego innovadoras o con temáticas muy específicas que no han conectado con el público general.



# ¿Hay juegos con buenas calificaciones que venden poco? ¿Y juegos mal calificados que venden mucho?
Se filtran las columnas relevantes para el análisis, seleccionando el año de lanzamiento y las ventas globales. Luego, se ordenan los datos de forma descendente utilizando `sort_values()`. Finalmente, se muestran los 10 años con mayores ventas.

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/18.png)

**Resultados:**
- Los datos muestran que algunos años, como **2006** y **1985**, tuvieron ventas significativamente más altas que otros. 📅

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/19.png)

## 8. Consideraciones futuras
Una vez que los datos estén procesados y limpios, será posible realizar un análisis más profundo. Por ejemplo, se podrían explorar correlaciones avanzadas entre las puntuaciones de los críticos y las ventas globales. Además, este proyecto podría servir como base para crear modelos predictivos que anticipen el éxito comercial de futuros videojuegos basándose en sus características clave. También podría ser interesante analizar el impacto de factores externos como campañas de marketing o lanzamientos simultáneos de consolas. 📈

# 8.1. Implementación

## Bootstrap (validación de sesgos)

### Pasos:
1. Definir n (tamaño de la muestra) y R (número de repeticiones).
![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/sesgos.png)
   
3. Crear histogramas para visualizar la distribución de las medias y medianas calculadas.
   
   ![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/sesgos2.png)

4. Calcular el error estándar de las medias y medianas.

   ![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/sesgos3.png)


En el análisis de bootstrap, los errores estándar obtenidos son 0.0119 para la media y 0.0034 para la mediana. Estos valores bajos indican que las estimaciones de la media y la mediana son precisas, con poca variabilidad en torno a los valores originales. La menor variabilidad en la mediana sugiere que es una medida más robusta y menos afectada por valores extremos, lo que refuerza su confiabilidad para representar el centro de los datos.

   ![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/sesgos4.png)
  
  ![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/sesgos5.png)
      
# 📊 Métrica o estadística a utilizar (Pruebas A/B)

¿Hay juegos con buenas calificaciones que venden poco? 🎮 ¿Y juegos mal calificados que venden mucho? 🤔

¿Existen diferencias significativas en las ventas entre videojuegos con puntuaciones altas y bajas de críticos o usuarios? 📈

## 📏 Métrica
La métrica que utilizaremos para comparar el comportamiento de los grupos será la **media de ventas globales**. Esto nos permitirá evaluar si existe una diferencia significativa en las ventas entre los videojuegos con puntuaciones altas y bajas.

## 🔍 Test de hipótesis

### 💡 Hipótesis:
- **Hipótesis nula (H0)**: No hay diferencia significativa en las ventas medias entre videojuegos con puntuaciones altas y videojuegos con puntuaciones bajas.
- **Hipótesis alternativa (H1)**: Hay una diferencia significativa en las ventas medias entre videojuegos con puntuaciones altas y videojuegos con puntuaciones bajas.

### 📋 Pasos:
1. Clasificar los juegos en grupos según las puntuaciones de críticos. 🏅

  ![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/h1.png)


3. Combinación de grupos y realización del test de permutación. 🔄

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/h2.png)

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/h3.png)

La diferencia observada en medias es de **1.1277**, lo que indica que, en promedio, los videojuegos con puntuaciones críticas altas (mayores a 80) venden **1.1277 millones de unidades** más que aquellos con puntuaciones críticas bajas (80 o menos). Además, el valor p de **0.0000** sugiere una evidencia muy fuerte en contra de la hipótesis nula, lo que implica que hay una diferencia significativa en las ventas entre estos dos grupos. Los resultados respaldan la idea de que los juegos con mejores críticas tienden a vender más que los mal calificados. 📊✨

## 🤖 Rendimiento de un modelo de machine learning
Intenta predecir el éxito o fracaso de un videojuego en función de características específicas, como las puntuaciones de críticos y usuarios.

![1](https://github.com/LunaLBR/Videogames_analysis_with_python/blob/main/imagenes/h4.png)


### 📊 Interpretación de los Valores
- **✅ Verdaderos Positivos (VP)**: 743. Estos son los casos en los que el modelo predijo correctamente que un videojuego sería un "Éxito". Es decir, 743 videojuegos que realmente fueron exitosos y que el modelo también clasificó como tales.
  
- **✅ Verdaderos Negativos (VN)**: 1317. Estos son los casos en los que el modelo predijo correctamente que un videojuego sería un "Fracaso". Así que 1317 videojuegos que realmente fracasaron y que el modelo también clasificó como fracasados.
  
- **❌ Falsos Positivos (FP)**: 408. Estos son los casos en los que el modelo predijo incorrectamente que un videojuego sería un "Éxito", pero en realidad fue un "Fracaso". Es decir, 408 videojuegos que el modelo clasificó como éxitos, pero no lo fueron.
  
- **❌ Falsos Negativos (FN)**: 918. Estos son los casos en los que el modelo predijo incorrectamente que un videojuego sería un "Fracaso", pero en realidad fue un "Éxito". Es decir, 918 videojuegos que el modelo clasificó como fracasos, pero sí tuvieron éxito.

## 9. Conclusión
En este análisis, hemos examinado diversos aspectos clave del mercado de videojuegos, revelando patrones sobre las plataformas, géneros y su relación con las ventas y calificaciones. El procesamiento de datos es esencial para comprender las tendencias en la industria de los videojuegos y su relación con las ventas globales. 

Con una base de datos procesada, será posible avanzar hacia análisis más complejos y construir modelos predictivos que apoyen la toma de decisiones estratégicas en el desarrollo y publicación de videojuegos. 🎮

1. **Plataformas con mayores ventas globales:** Las consolas **PlayStation 2**, **Xbox 360** y **PlayStation 3** dominan el mercado, demostrando que la calidad, el acceso a juegos icónicos y una sólida base de jugadores son fundamentales para el éxito comercial. 
2. **Géneros más vendidos:** Los videojuegos de **Acción**, **Deportes** y **Shooter** generan las ventas más altas a nivel global. Esto refleja una clara preferencia por juegos con alta adrenalina, interacción directa y experiencias inmersivas.
3. **Distribución por género y plataforma:** Se observa que **PlayStation 2** y **Nintendo DS** ofrecen una amplia variedad de juegos, especialmente en los géneros de **Acción** y **Deportes**. Esto subraya la importancia de contar con un catálogo diverso.
4. **Relación entre puntuaciones y ventas:** Aunque existe una correlación positiva entre altas calificaciones y ventas, también se encontraron ejemplos de juegos con bajas puntuaciones que lograron ventas significativas. Esto sugiere que factores como la nostalgia y el marketing pueden impulsar las ventas, incluso ante críticas negativas. 💡

En resumen, nuestro análisis no solo responde a preguntas clave sobre los factores que impulsan las ventas, sino también a cómo las preferencias de los jugadores, la atracción de los géneros y las estrategias de las plataformas se combinan para crear fenómenos globales en la industria del videojuego. 🌍

## 10. Entregables
- Código ejecutable en Google Colab o Jupyter Notebook que realice el procesamiento y análisis de datos.
- Documento en Google Docs o Word que describa los pasos y resultados del procesamiento y análisis de datos.
- Presentación en PowerPoint o Google Slides con un resumen de las técnicas aplicadas y los resultados obtenidos en el análisis de los datos. 📑
