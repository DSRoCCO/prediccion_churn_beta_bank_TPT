### Beta Bank

### Modelo Predictivo para Detectar Clientes en Riesgo de Deserción en Beta Bank

Este proyecto consiste en desarrollar un modelo predictivo de aprendizaje supervisado para identificar clientes de Beta Bank que tienen un alto riesgo de cancelar sus cuentas, dado que retener clientes existentes es más rentable que adquirir nuevos.

Se analizaron datos históricos del comportamiento de los clientes, incluyendo características como el saldo, edad, género, país, actividad, número de productos, y si han cancelado su cuenta o no. Estas características fueron procesadas y utilizadas para construir y optimizar un modelo que maximice el valor F1, asegurando un puntaje mínimo de 0.59.

### Metodología
#### 1. Preparación de Datos:
Se exploraron los datos para identificar valores faltantes, outliers y posibles desequilibrios en las clases objetivo.
Se aplicaron técnicas de codificación como one-hot encoding para variables categóricas y estandarización de datos numéricos para mejorar el rendimiento de los modelos.

#### 2. Modelos Considerados:
Se evaluaron tres algoritmos principales: Regresión Logística, Árbol de Decisión y Bosque Aleatorio.
Los modelos fueron optimizados mediante validación cruzada y búsqueda de hiperparámetros, incluyendo ajustes para el desequilibrio de clases mediante técnicas de sobremuestreo.

#### 3. Optimización de Parámetros:
Para el Bosque Aleatorio, el valor de n_estimators se fijó en 60, balanceando entre rendimiento y costo computacional, mientras que max_depth se estableció en 100 para maximizar el rendimiento sin sobreajustar el modelo.
Este modelo fue el seleccionado final debido a su desempeño superior en las métricas clave.

### Resultados del Modelo Final
Con un modelo de Bosque Aleatorio configurado con n_estimators = 60 y max_depth = 100, se lograron los siguientes resultados:

- F1 Score: 83.39%
  Indicador de un modelo bien balanceado entre precisión y sensibilidad.
-  Recall (Sensibilidad): 83.73%
  Muestra que el modelo identifica correctamente la mayoría de los clientes que cancelan sus cuentas.
- Exactitud (Accuracy): 83.77%
  Alta capacidad para predecir correctamente tanto positivos como negativos.
- AUC-ROC: 83.77%
  Confirmación de que el modelo es significativamente mejor que uno aleatorio.

### Hallazgos y Conclusión
La matriz de confusión mostró una alta proporción de verdaderos positivos y negativos, junto con pocos falsos positivos y negativos, indicando un rendimiento robusto.
Además, la validación cruzada confirmó que el modelo es consistente y generaliza bien en diferentes subconjuntos de datos.

Se concluye que este modelo predictivo es una herramienta efectiva para predecir clientes en riesgo de deserción, ayudando al banco a priorizar estrategias de retención y mejorar la experiencia del cliente.
