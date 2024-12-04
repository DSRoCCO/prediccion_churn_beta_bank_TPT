# Proyecto: Modelo Predictivo para Detectar Clientes en Riesgo de Deserción en Beta Bank

## Descripción del Proyecto
El objetivo de este proyecto es desarrollar un modelo predictivo que permita identificar clientes con alto riesgo de cancelar sus cuentas en **Beta Bank**. Retener clientes existentes es más rentable que adquirir nuevos, por lo que este modelo ayudará al banco a priorizar estrategias de retención.

Se utilizaron datos históricos sobre el comportamiento de los clientes, incluyendo características como saldo, edad, género, país, actividad, número de productos y estado de cancelación de la cuenta. El modelo debe alcanzar un puntaje F1 mínimo de **0.59**.

---

## Metodología

### 1. Preparación de Datos
- **Exploración inicial**:
  - Se identificaron valores faltantes y outliers.
  - Se verificaron desequilibrios en las clases objetivo.

- **Preprocesamiento**:
  - Se aplicaron técnicas de **one-hot encoding** para variables categóricas.
  - Las características numéricas fueron estandarizadas para mejorar el rendimiento de los modelos.

### 2. Selección de Modelos
Se evaluaron tres algoritmos principales:
- **Regresión Logística**
- **Árbol de Decisión**
- **Bosque Aleatorio**

Se optimizaron los hiperparámetros de cada modelo mediante validación cruzada y se ajustaron las técnicas para manejar el desequilibrio de clases, como el **sobremuestreo**.

### 3. Optimización del Modelo Seleccionado
El modelo final seleccionado fue el **Bosque Aleatorio** debido a su rendimiento superior:
- **n_estimators**: 60 (número de árboles en el bosque, balance entre rendimiento y costo computacional).
- **max_depth**: 100 (profundidad máxima, para evitar el sobreajuste y maximizar el rendimiento).

---

## Resultados del Modelo Final

Con la configuración óptima, el modelo alcanzó los siguientes resultados:

- **F1 Score**: **83.39%**
  - Indica un buen balance entre precisión y sensibilidad.
- **Recall (Sensibilidad)**: **83.73%**
  - Alta capacidad para identificar correctamente a los clientes que cancelan sus cuentas.
- **Exactitud (Accuracy)**: **83.77%**
  - Alto porcentaje de predicciones correctas, tanto positivas como negativas.
- **AUC-ROC**: **83.77%**
  - Muestra que el modelo tiene un desempeño significativamente mejor que uno aleatorio.

### Matriz de Confusión
La matriz de confusión reveló:
- Alta proporción de verdaderos positivos y negativos.
- Baja cantidad de falsos positivos y falsos negativos, confirmando un rendimiento robusto.

---

## Hallazgos y Conclusión
1. **Consistencia del modelo**:
   - La validación cruzada demostró que el modelo generaliza bien en diferentes subconjuntos de datos.

2. **Impacto práctico**:
   - El modelo predictivo es una herramienta valiosa para priorizar clientes en riesgo y diseñar estrategias de retención.

3. **Recomendaciones**:
   - Implementar este modelo en el flujo operativo del banco para mejorar la experiencia del cliente y reducir la tasa de deserción.

Este modelo posiciona a Beta Bank para tomar decisiones informadas y fortalecer la lealtad de sus clientes.
