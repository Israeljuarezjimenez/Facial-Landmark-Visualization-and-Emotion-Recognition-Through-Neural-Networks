#  Reconocimiento  de Emociones Faciales con Redes Neuronales


El sistema utiliza landmarks faciales para extraer características
geométricas del rostro y técnicas estadísticas para analizar y
procesar los datos.

Se comparan diferentes modelos de clasificación, incluyendo un
Árbol de Decisión y Redes Neuronales.

El modelo de Red Neuronal optimizada alcanzó una precisión del
**98.48 %** en el conjunto de prueba.

---

##  Objetivo

Desarrollar un modelo capaz de reconocer emociones faciales mediante
el análisis de puntos clave del rostro y técnicas de Machine Learning.

---

##  Dataset

Se utilizó el conjunto de datos **CK+ (Cohn-Kanade)**, que contiene
secuencias de imágenes faciales desde una expresión neutra hasta
la máxima intensidad de una emoción.

El proyecto trabaja con 7 emociones:

- 😠 Enojo
- 😒 Desprecio
- 🤢 Disgusto
- 😨 Miedo
- 😊 Felicidad
- 😢 Tristeza
- 😲 Sorpresa

---

## Metodología

### 1. Procesamiento de imágenes

Para cada sujeto se selecciona una imagen con expresión neutra y
otra correspondiente a la máxima intensidad de la emoción.

### 2. Detección de landmarks

Se utiliza **Dlib** para detectar el rostro y obtener **68 puntos
faciales** correspondientes a regiones como:

- Ojos
- Cejas
- Nariz
- Boca
- Contorno facial

Los puntos son normalizados para reducir las variaciones producidas
por la posición y el tamaño del rostro.

### 3. Extracción de características

Se calculan las diferencias entre los landmarks de la expresión
neutra y los de la expresión emocional.

También se utilizan técnicas estadísticas como:

- Cuartiles
- Rango intercuartílico (IQR)
- Detección de valores atípicos
- Normalización Min-Max

---

##  Modelos utilizados

### Árbol de Decisión

Se utilizó como modelo de referencia para comparar el rendimiento.



### Red Neuronal Básica

Arquitectura con capas de 256 y 128 neuronas, activación ReLU
y Dropout.


### Red Neuronal Optimizada

Se implementó una arquitectura más avanzada utilizando:

- Batch Normalization
- GELU
- Dropout
- Conexiones residuales
- AdamW
- CosineAnnealingLR


---

##  Resultados

| Modelo | Precisión |
|---|---:|
| Árbol de Decisión | 80 % |
| Red Neuronal Básica | 96.97 % |
| Red Neuronal Optimizada | **98.48 %** |

La Red Neuronal Optimizada obtuvo el mejor desempeño, logrando
clasificar las emociones con una precisión del **98.48 %**.

---

##  Tecnologías

- Python
- Machine Learning
- Redes Neuronales
- Dlib
- NumPy
- Análisis estadístico
- Visualización de datos

---
