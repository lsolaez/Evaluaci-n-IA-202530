# Proyecto: Evaluación y Detección de Phishing con Modelos ML y C

Este proyecto analiza el dataset **PhiUSIIL Phishing URL Dataset** y desarrolla un pipeline completo de:
- Exploración de datos (EDA)
- Limpieza y transformación
- Entrenamiento de modelos en Python (Random Forest, Naive Bayes)
- Implementación paralela de un modelo en **C**
- Comparación entre modelos
- Métricas de rendimiento y conclusiones

El notebook reproduce paso a paso el flujo completo.

---

## 📌 Requisitos

### Python
- Python 3.10+
- pandas  
- numpy  
- scikit-learn  
- matplotlib  
- seaborn  

### C
- GCC o Clang para compilar programación en C
- Extensión para ejecutar código C en Jupyter (Google Colab o Jupyter C++ Kernel)

---

## 📁 Estructura del Notebook

### **1. Contexto y formulación del problema**
Describe la hipótesis sobre cómo características de una URL permiten detectar phishing.

### **2. Exploración (EDA)**
- Lectura del dataset CSV  
- Limpieza básica  
- Distribución de clases  
- Análisis de correlación  
- Identificación de variables más relevantes  

### **3. Preprocesamiento**
- Manejo de valores nulos  
- Conversión a numérico  
- Separación `X` y `y`  
- División en entrenamiento/prueba  

### **4. Modelos en Python**
Modelos entrenados:
- **Random Forest**
- **Naive Bayes (Multinomial y Categorical)**

Incluye:
- Feature importance  
- Matriz de confusión  
- Exactitud y métricas generales  

### **5. Implementación en C**
Se reproduce un clasificador Naive Bayes desde cero:
- Lectura del dataset procesado  
- Cálculo manual de probabilidad por clase  
- Predicción por lotes  
- Comparación con sklearn  

### **6. Resultados**
Comparación presentada al final del notebook:
- Modelo en C: >99%  
- sklearn MultinomialNB: ~99%  
- Interpretación de diferencias  
- Limitaciones y recomendaciones  

---

## 🚀 Cómo Reproducir

### 1. Clonar o cargar el notebook

```
ia_2025_30_eval_final_perezdeaguas_solaez_suarez.ipynb
```

### 2. Cargar el dataset zip que se encuentra en el repositorio en `/content/` o ruta local equivalente

### 3. Ejecutar el notebook secuencialmente
> No requiere configuración adicional si se ejecuta en Google Colab.

### 4. (Opcional) Compilación del modelo en C

En Colab:

```bash
gcc model.c -o model
./model
```

En Linux local:

```bash
gcc naive_c.c -o naive
./naive
```

---

## 📊 Interpretación de Resultados

El proyecto concluye que:
- Las características construidas desde la URL permiten una detección extremadamente precisa.
- La implementación en C es eficiente y cercana a sklearn.
- La limpieza del dataset afecta fuertemente los resultados.
- La importancia de características ayuda a detectar *data leakage*.

---

## 🙌 Créditos

Autores:  
**Pérez de Aguas, Solaez y Suárez**  
Proyecto académico 2025.  
Incluye análisis, modelos y experimentación técnica reproducible.

---
