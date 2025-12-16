# Análisis de Sentimientos y Manipulación de Datos en Python

Cuaderno práctico ejecutable en Google Colab con 4 ejercicios independientes (¡cada uno usa su propio dataset!).

## Práctica 1 – Análisis de Sentimientos en Español
**Modelo preentrenado basado en Naive Bayes y TF-IDF**  
Biblioteca: `sentiment-analysis-spanish`

### Objetivo
Implementar y evaluar un analizador de sentimientos en español utilizando un modelo preentrenado simple y eficiente. Combina **Multinomial Naive Bayes** con vectorización **TF-IDF**, diseñado especialmente para textos cortos en español.

### Pruebas realizadas 

Se evaluaron tres frases representativas utilizando el modelo de análisis de sentimientos:

| Frase                           | Tipo esperado | Puntuación obtenida | Interpretación                 |
|---------------------------------|---------------|------------------|-------------------------------|
| "Esta muy buena esa pelicula"   | Positiva      | 0.948            | Muy positiva (cercana a 1)    |
| "Que horrible comida!!!"        | Negativa      | 0.001            | Muy negativa (cercana a 0)    |
| "Tuve una experiencia neutral"  | Neutral       | 0.207            | Tendencia negativa ( debería ser más cercana a 0.5)             |

### Interpretación de los Resultados

- Detecta correctamente polaridades positiva y negativa extremas con alta confianza.  
- La frase neutral se clasifica como negativa, revelando una limitación típica de modelos clásicos: tendencia binaria y dificultad con textos neutros o ambiguos.

#### Análisis Detallado

- **Fortalezas:** Excelente detección de polaridades extremas y claras en textos cortos.  

- **Limitaciones:** Dificultad con neutralidad real y posible fallo en sarcasmo, ambigüedad o negaciones complejas.

### Conclusiones

**Enfoque clásico Naive Bayes + TF-IDF:**  
- Simple, rápido y ligero (perfecto para recursos limitados).  
- Eficiente en textos cortos con polaridad clara.  
- Limitado en ambigüedad, sarcasmo y neutralidad.

## Práctica 2 – Análisis Exploratorio con Pandas
- Dataset real de redes sociales (likes, retweets, países, usuarios…)
- Limpieza, filtros, nuevas columnas con `apply()`, `groupby()` y gráficos rápidos
- Exportación de resultados a CSV

## Práctica 3 – Joins, Fechas y Pivoteo Avanzado
- Unión de 3 CSV relacionados mediante `merge()`
- Conversión y extracción de día/mes/año con `pd.to_datetime()`
- Pivot tables + transpose para crear reportes listos para dashboard

## Práctica 4 – Visualización de Datos con el Titanic (el dataset más famoso del mundo)
- Comparativa real de las 3 formas más usadas de graficar en Python:
  - Pandas puro → gráficos en 1 línea
  - Seaborn → estética profesional sin esfuerzo
  - Matplotlib → control total del diseño
- Gráficos creados:
  - Barras: supervivencia por sexo y clase
  - Histogramas: distribución de edades y tarifas
  - Scatter plots: relación tarifa vs edad
- Personalización completa: títulos, colores, tamaños y leyendas

A continuación encontrarás el colab con las prácticas realizadas →  
[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Z-7rJwjfZ9NGsjlU4nktm8iuz-Ag4FT5?usp=sharing)

### Tecnologías usadas
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=python&logoColor=white)
