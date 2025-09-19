# 💻 Predicción de Precios de Laptops con Machine Learning

## 📌 Descripción
Este proyecto implementa un modelo de **Machine Learning supervisado** para **predecir el precio en euros de laptops** a partir de sus características técnicas.  
Se siguió un flujo completo de ciencia de datos: **análisis exploratorio (EDA), limpieza y procesamiento de datos, entrenamiento de modelos, comparación de resultados y prueba con muestras artificiales**.

El dataset utilizado proviene de **Kaggle** y contiene información real de laptops disponibles en el mercado europeo.

---

## 🚀 Tecnologías utilizadas
- **Python 3**  
- **pandas, numpy** → análisis de datos  
- **matplotlib, seaborn** → visualización  
- **scikit-learn** → preprocesamiento y modelos (kNN, RandomForest, MLP)  
- **TensorFlow / Keras** → Deep Neural Network (DNN)  

---

## 📂 Estructura del proyecto
- `notebooks/` → Jupyter Notebook con todo el análisis y el pipeline completo.  
- `laptop_price.csv` → dataset utilizado.  
- `wiki/` → documentación detallada (desarrollo paso a paso del proyecto).  
- `README.md` → introducción general.  

---

## 📊 Resultados principales
- **Modelos evaluados**: kNN, RandomForest, DNN.  
- **Mejor modelo**: **RandomForest**, con un error promedio (RMSE) de ~290 € en el conjunto de prueba y R² de 0.79.  
- **Variables más influyentes**: RAM, SSD, resolución de pantalla, GHz del CPU y GPU GTX.  

---

## 📈 Diagrama de flujo del pipeline

```mermaid
flowchart TD
    A[Dataset original] --> B[Limpieza y procesamiento]
    B --> C[Pipeline de preprocesamiento]
    C --> D[División Train / Val / Test]
    D --> E1[kNN]
    D --> E2[RandomForest]
    D --> E3[DNN]
    E1 --> F[Comparación de métricas]
    E2 --> F
    E3 --> F
    F --> G[Modelo seleccionado: RandomForest]
    G --> H[Predicción en muestra artificial]
