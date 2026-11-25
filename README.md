# Predicción de precios de alojamientos en Bogotá

## Objetivo
Estimar el precio anunciado por noche de alojamientos en Bogotá a partir de sus características y ubicación, y utilizar esa estimación como referencia para evaluar escenarios de rentabilidad.

## Pregunta de investigación
¿En qué medida las características de un alojamiento y su ubicación permiten predecir el precio anunciado por noche en Bogotá, y cómo puede utilizarse esa estimación para evaluar escenarios de rentabilidad?

## Datos
El proyecto utiliza datos de anuncios de Inside Airbnb: listings, reviews y calendar.
Los archivos de datos originales se mantienen fuera del repositorio por su tamaño.

## Metodología
1. Limpieza y preparación de datos.
2. Análisis descriptivo y visualización.
3. Comparación de modelos predictivos.
4. Evaluación del modelo en datos de prueba y validación cruzada.
5. Exportación del modelo seleccionado.

## Modelo candidato principal
Random Forest.

Resultados en el conjunto de prueba:
- MAE: aproximadamente 77.807 COP.
- RMSE: aproximadamente 193.975 COP.
- R²: aproximadamente 0,3406.

La validación cruzada obtuvo un MAE promedio aproximado de 79.862 COP y un R² promedio de 0,279.

## Limitaciones
El modelo estima precios anunciados, no reservas, ingresos efectivamente recibidos ni rentabilidad real.
La importancia de las variables no implica causalidad.
Las predicciones de alojamientos de precio alto presentan errores importantes.
El simulador de rentabilidad requiere costos, ocupación y otros supuestos introducidos por el usuario.

## Cómo ejecutar
```bash
pip install -r requirements.txt
jupyter notebook notebooks/Proyecto_Analitica_Airbnb_Bogota.ipynb
```
Descarga `listings.csv` de Bogotá desde [Inside Airbnb](https://insideairbnb.com/get-the-data/) y ajusta la variable `ruta_listings` en el notebook (originalmente apunta a Google Drive en Colab).

## Estructura
- `notebooks/`: notebook de análisis.
- `modelos/`: modelo exportado.
- `documentacion/`: material complementario.
