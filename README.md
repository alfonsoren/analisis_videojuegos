# 📊 Análisis de Videojuegos — Proyecto Integrado

Este proyecto forma parte del curso de análisis de datos y tiene como objetivo aplicar las habilidades adquiridas para realizar un estudio de caso real. Se trabajó con datos históricos de ventas de videojuegos, clasificaciones, plataformas y géneros con el fin de identificar patrones que determinen el éxito de un videojuego. El análisis busca ayudar a una tienda ficticia llamada **Ice** a planear su campaña de ventas para el año 2017.

## 📁 Dataset

- Archivo: `/datasets/games.csv`
- Columnas disponibles:
  - `name`: Nombre del videojuego
  - `platform`: Plataforma (ej. Xbox, PlayStation)
  - `year_of_release`: Año de lanzamiento
  - `genre`: Género
  - `na_sales`, `eu_sales`, `jp_sales`, `other_sales`: Ventas por región (en millones USD)
  - `critic_score`: Calificación de críticos (0–100)
  - `user_score`: Calificación de usuarios (0–10)
  - `rating`: Clasificación ESRB

## 🧹 1. Preparación de los datos

- Las columnas fueron renombradas en minúsculas para mayor consistencia.
- Se convirtieron los datos a los tipos adecuados (`year_of_release` a entero, `user_score` a flotante).
- Se abordaron los valores nulos de forma razonada:
  - Se dejaron en blanco los que no podían deducirse.
  - Se excluyó "TBD" en calificaciones.
- Se creó la columna `total_sales` sumando las ventas por región.

## 📈 2. Análisis exploratorio

- Se evaluó la distribución de lanzamientos por año y se definió un periodo relevante (últimos años antes de 2017).
- Se identificaron plataformas líderes y aquellas en declive.
- Se analizó el ciclo de vida de plataformas: introducción, auge y decadencia.
- Se seleccionaron plataformas rentables para 2017.
- Se construyeron diagramas de caja de ventas globales por plataforma.
- Se analizó la correlación entre reseñas de usuarios/críticos y ventas en una plataforma específica.
- Se compararon las ventas cruzadas de juegos entre plataformas.
- Se evaluó la rentabilidad por género.

## 🌍 3. Perfil de usuario por región

Se construyeron perfiles para:
- **Norteamérica (NA)**
- **Europa (EU)**
- **Japón (JP)**

Para cada región se identificaron:
- Top 5 de plataformas más populares.
- Top 5 de géneros más rentables.
- Impacto de la clasificación ESRB en las ventas.

## 📊 4. Pruebas de hipótesis

Se probaron dos hipótesis estadísticas:

1. **H₀:** Las calificaciones promedio de usuarios para Xbox One y PC son iguales.  
   **H₁:** Las calificaciones promedio de usuarios para Xbox One y PC son diferentes.

2. **H₀:** Las calificaciones promedio de usuarios para los géneros Acción y Deportes son iguales.  
   **H₁:** Las calificaciones promedio de usuarios para los géneros Acción y Deportes son diferentes.

- Se utilizó un nivel de significancia `α = 0.05`.
- Se aplicó la prueba t de Student para muestras independientes.
- Se interpretaron los resultados y se sacaron conclusiones basadas en los valores p obtenidos.

## ✅ 5. Conclusiones generales

- Se identificaron plataformas en crecimiento para enfocar la campaña 2017.
- Los géneros con mayor potencial de ventas y preferencia por región fueron determinados.
- Las reseñas de críticos y usuarios influyen, pero varía según plataforma.
- Las diferencias culturales influyen en el gusto por plataformas y géneros (ej. Japón vs. NA).
- Se comprobó estadísticamente que ciertas diferencias de opinión entre plataformas y géneros son significativas.

---

**📎 Herramientas utilizadas:**  
Python · pandas · matplotlib · seaborn · scipy · Jupyter Notebook


---

¡Gracias por revisar este proyecto!
