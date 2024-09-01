# Detección de Fraudes en Reportes de Daños Vehiculares

![cover](/images/cover.jpg)

Este proyecto desarrolla un modelo de inteligencia artificial diseñado para detectar fraudes en reportes de daños vehiculares. Utilizando técnicas avanzadas de análisis de datos y modelado, hemos implementado un sistema que identifica reportes fraudulentos con alta precisión.

## Tabla de Contenidos
- [Descripción del Proyecto](#descripción-del-proyecto)
- [Análisis Exploratorio](#análisis-exploratorio)
- [Procesamiento de Datos](#procesamiento-de-datos)
- [Modelamiento](#modelamiento)
- [Resultados y Conclusiones](#resultados-y-conclusiones)
- [Contribuidores](#contribuidores)
- [Licencia](#licencia)

## Descripción del Proyecto

Este proyecto tiene como objetivo crear un modelo predictivo capaz de identificar fraudes en reportes de daños vehiculares. A partir de un dataset extenso de registros de vehículos y reportes de averías, el modelo analiza diversas características para determinar la probabilidad de que un reporte sea fraudulento.

## Análisis Exploratorio

![description](/images/description.jpg)

Durante la fase de análisis exploratorio, se trabajó con un dataset de 196,000 registros y 20 columnas. Algunas observaciones clave incluyen:

**Distribución de Millas Recorridas:** La mayoría de los vehículos tienen menos de 100,000 millas.
![distribution](/images/distribution.jpg)

**Costos de Reparación:** Predominantemente menores a $1,000, y la mayoría de las reparaciones toman menos de 10 horas.
![cost](/images/cost.jpg)

**Análisis de Complejidad:** Las reparaciones que requieren más días de espera suelen ser más complejas y costosas.
![complexity](/images/complexity.jpg)

## Procesamiento de Datos

El procesamiento de datos incluyó la imputación de valores nulos y la creación de nuevas variables para mejorar la precisión del modelo. Algunas de las transformaciones realizadas son:

**Imputación por Moda y Promedio:** Basado en características como marca, modelo, y año de registro.
![null_values](/images/null_values.jpg)

**Nuevas Variables:** Se introdujeron variables como el costo del problema, complejidad de reparación, y porcentaje de reparación para capturar patrones de fraude.
![new_variables](/images/new_variables.jpg)

## Modelamiento

Se probaron varios modelos, incluyendo Random Forest, Naive Bayes, Logistic Regression, y XGBoost. Los resultados mostraron que:

- **XGBoost:** Fue el modelo con mejor desempeño, alcanzando un Balanced Accuracy de 0.9904 después de la optimización de parámetros.
- **Logistic Regression:** Ofreció un buen balance con un Balanced Accuracy de 0.884.
- **Random Forest:** También mostró un buen desempeño con un Balanced Accuracy de 0.8657.
![xgboost](/images/xgboost.jpg)

### Optimización de Parámetros

Para mejorar el desempeño de XGBoost, se utilizó `RandomizedSearchCV`, logrando una configuración óptima que incluye `subsample`, `n_estimators`, `min_child_weight`, `max_depth`, entre otros.

![xgboost_parameters](/images/xgboost_parameters.jpg)

## Resultados y Conclusiones

- **XGBoost:** Resultó ser el mejor modelo para la tarea, destacándose por su capacidad de manejar datos complejos y ajustar pesos de clases.
- **Impacto de Características:** Variables como el color del vehículo, número de asientos, y tipo de vehículo son cruciales en la detección de fraudes.
- **Análisis SHAP:** Proporciona una visión detallada del impacto de cada característica en las predicciones del modelo.

## Contribuidores

### Edwin Veloz
✉️ edwin06111998@gmail.com

---

### Francisco Cruz
✉️ franciscocruz907@gmail.com

---

### Carlos Ordoñez
✉️ caropala@espol.edu.ec

---

### Alex Mora
✉️ aemorah@gmail.com