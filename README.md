# Implementación de un modelo que permita predecir la perdida de clientes

---

## Resumen

Este repositorio contiene un notebook de jupyter donde se implementa un modelo de clasificación que permita predecir la **perdida de clientes (churn)** en **Telecom X**. El objetivo principal de este proyecto es ilustrar el proceso de seleccion del modelo, su evaluación e implementación final.

---

## Estructura del Proyecto

La implementación del modelo consistio de las siguientes etapas:

### 1. Carga de Datos
El paso inicial consistió en cargar el conjunto de datos proporcionado por Telecom X para obtener una comprensión preliminar de su estructura y contenido.

### 2. Analisis preliminar de datos
Aqui se exploraron los datos para tratar de entender las principales diferencias entre los dos grupos de usuarios y tener una idea de que factores pueden tener mayor peso.

### 3. Division de datos y codificación de variables categóricas
Se procedio a repatir los datos en los conjuntos de entrenamiento y validación y se uso un OneHotEncoder para la codificación de las variables categóricas dentro de los datos y que asi mi modelo pueda hacer uso de ellas.

### 5. Selección de modelos iniciales
Para este caso se decidio considerar dos tipos de modelos para abordar el problema uno de arboles de decisión aleatoreos y un modelo de regresión logistica, ambos a implementar usando la librería sklearn.

### 6. Análisis de Multicolinealidad
Se procedio a realizar dos tipos de test para detectar la Multicolinealidad, usando una matriz de correlación y un análisis VIF, luego se procedio a eliminar las columnas que precentaban una alta correlación entre ellas.

### 6. Evaluación de los modelos implementados
Se entreno y procedio a evaluar los modelos en base a metricas como precission, accuracy, f1 y recall, siendo la metrica considerada a maximizar en este caso el recall, ya que se considero que es más importante tratar de identificar correctamente a la mayor cantidad de usuarios con churn 1 o que es candidato a abandonar.

### 7. Selección del modelo final
Finalmente se opto por elegir el modelo de regresión logistica ya que presento un recall levemente superior que el otro modelo (81% vs 80%), además de ser considerado más valioso a la hora de determinar como cada atributo de los datos afecta las probabilidades de churn.

### 8. Validación cruzada e hiperparametrización
Se procedio a realizar la validación cruzada y la hiperparametrización para eliminar posibles efectos por la repartición inicial de los datos y para definir con que parametros mi modelo tiene el mejor desempeño, al final el modelo logro obtener un recall del 80%.

### 9. Análisis de la importancia de mis atributos
En base a lo entregado por mi modelo se procedio a analisar que factores son los que más hacían la diferencia a la hora de inclinar la decisión del modelo ya sea hacia un churn 0 (se quedo) o 1 (se fue).

### 4. Informe final y recomendaciones
En esta fase final, se elabora un informe donde se presentan los principales descubrimientos a partir de mi modelo, se listan los factores que más influyen en que un cliente se quede o abandone y se da una serie de recomendaciones a la empresa Telecom X para hacer uso de los atributos que potencian la estancía de clientes a su favor y minimizar o remediar aquellos que aportan al abandono.
