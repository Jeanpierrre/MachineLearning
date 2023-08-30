
<p align="center">  
<span style="font-size: 45px;font-weight:bold">
    Primer Laboratorio de Introduction to <br> Machine Learning  
</span >
</p>
<p align="center">
  <img src="image.png" alt="logo UTEC" width=200 height=200>
</p>
<p align="center"> 
  <em >
    Universidad de Ingenieria y Tecnologia (UTEC) -- Lima, Peru
  </em>  
</p>
  
<p align="center"> 
  <em >
    August 2023 -- Seccion Profesor Arturo Deza <br>    
  </em>  
</p> 
<p align="center"> 
  <span style="font-size: 30px;font-weight:bold">
    Tema de Laboratorio: LINEAR REGRESION
  </span >
</p> 

## Preguntas:  

### Cual es tu dataset? (5pts)  

El dataset elegido contiene los detalles sobre la emisión de CO2 parte de vehículos con diversas características. Estos datos fueron recopilados en Canadá durante un período de 7 años y constan de 7385 registros con 12 columnas en total. Dentro del contenido del dataset se encuentran los siguientes campos:  

-  **Modelo:** Hace referencia a la designación específica del vehículo  
-  **Transmisión:**  Describe cómo se realiza el cambio de marchas en el vehículo y qué tipo de transmisión utiliza  
-  **Tipo de combustible:** Especifica el tipo de combustible que utiliza el vehículo.  
-  **El consumo de combustible:** Proporciona información sobre el rendimiento en términos de consumo de combustible del vehículo en diferentes condiciones de conducción  
-  **Emisiones de CO2:** Representa la cantidad de dióxido de carbono emitido por el vehículo por kilómetro recorrido, considerando tanto la conducción en ciudad como en carretera  

### Cual es el problema de regresion que estas resolviendo? (2pts)  
_*Predicción de CO2 emitida en función del tamaño del motor.*_  
El objetivo es poder comprender sobre cómo el tamaño del motor afecta a las emisiones del CO2. A medida que el tamaño del motor aumenta o disminuye se quiere determinar si existe una relación lineal entre estas dos variables. Con ella poder predecir las emiciones del CO2.

### Cuantos data points tiene tu data? (0.5pts)  
Mi conjunto de datos contiene un total de 7385 registros donde cada registro representa una única con información sobre emisiones de CO2 de vehículos y sus características asociadas.  

### Cual es el $\beta$ asumiendo que cruza el origen? (1pt)  

### Cual es el $\beta$ asumiendo que no cruza el origen? (2pts)  

### Cual es el número de variables independientes? (0.5pts)  

### Cual es la variable dependiente? (0.5pts)  
La variable dependiente es el CO2, ya que es la medida que se busca predecir en base a las características del vehículo.  

### Cuales son las unidades de medicion para cada variable? (0.5pts)  
Respecto a la cantidad de CO2 emitida esta medida en gramos/kilometros, y el Tamaño del motor esta en base a la capacidad en litros que soporta el motor.  

## Regresion por el Origen (3pts)  
Imagen aqui  

### Cual es el error promedio cuadratico?   

## Regresion que no pasa por el Origen (2pts)  
Imagen aqui  

### Cual es el error promedio cuadratico?  


## Regresion en base a 100 veces (3pts)  

### Cual es el $\beta$ promedio encontrado cuando la regresion se hace con la recta pasando por el origen y no pasando por el origen? 







#Formula que usaremos 

Y=β0+B1*X

Donde:
Y es la variable dependiente.

X es la variable independiente.

B0 es el intercepto (punto donde la línea cruza el eje y)

​
B1 es la pendiente de la línea de regresión.









BETA_ORIGEN.PY

el valor de "beta" representará directamente la pendiente de la línea de regresión que pasa por el origen (0,0)

Cuando especificas fit_intercept=False al crear la instancia del modelo de regresión lineal, estás indicando que la línea de regresión debe pasar por el origen en lugar de tener un término de intersección.


 en la fórmula 
    y=b0+b1*x
  es el coeficiente de la pendiente de la regresión lineal. Por lo tanto, en el caso de una regresión lineal simple, el valor que necesitas es el coeficiente b1

Si estás utilizando model.coef_[0], efectivamente estás accediendo al coeficiente b1,
 que es el coeficiente de la pendiente de la línea de regresión. El término [0] se refiere al primer coeficiente en la lista de coeficientes que devuelve model.coef_, que en este caso es el coeficiente b1

En resumen, para obtener el valor del coeficiente de la pendiente b1, en una regresión lineal simple, puedes utilizar model.coef_[0].






MSE
Incluso si los valores ajustados se encuentran muy cerca de los valores reales, siempre habrá alguna diferencia residual debido a la naturaleza de los datos y la forma en que se están ajustando. Sin embargo, el MSE puede ser bastante pequeño si la regresión se ajusta bien a los datos.

En términos prácticos, un MSE muy cercano a 0 podría ser indicativo de un sobreajuste (overfitting), lo que significa que el modelo se ajusta demasiado a los datos de entrenamiento y podría no generalizar bien a nuevos datos. Por lo tanto, no necesariamente buscas un MSE de 0, sino un valor bajo que indique un buen ajuste del modelo a los datos y una capacidad razonable de generalización.



![MSE](MSE.png)

MSE = (1/n) * Σ(yi - ŷi)^2

Donde:

n es el número de puntos de datos.
yi son los valores reales de la variable dependiente.
ŷi son las predicciones del modelo para la variable dependiente correspondiente a xi.
En otras palabras, el MSE es la suma de las diferencias al cuadrado entre las predicciones del modelo y los valores reales, dividida por el número total de puntos de datos. Cuanto más bajo sea el valor del MSE, mejor será el ajuste del modelo a los datos.