🌆 Análisis y Visualización de Airbnb NYC

Este proyecto tiene como objetivo analizar y visualizar datos de Airbnb en la ciudad de Nueva York, utilizando herramientas de procesamiento de datos en Python, almacenamiento en la nube con AWS S3, y visualización interactiva mediante Power BI.

🚀 Tecnologías utilizadas

Python (pandas, pyarrow): para limpieza y transformación de datos.

AWS S3: almacenamiento de archivos Parquet accesibles desde URL.

Power BI: visualización de datos, KPI, mapas, y análisis interactivo.

Formato Parquet: optimización del rendimiento en carga de datos.

📊 Dataset

El dataset fue extraído de Kaggle: New York City Airbnb Open Data

Contiene información detallada de anuncios publicados en Airbnb incluyendo:

ID de anuncio y anfitrión

Localización geográfica

Tipo de habitación

Precio por noche

Cantidad de noches mínimas

Disponibilidad anual

Reviews y más

📁 Proceso ETL

Se limpiaron datos erróneos y filas incompletas.

Se filtraron outliers (precio < 10 o > 1000).

Se exportó el dataset limpio como Parquet.

El archivo se subió a AWS S3 con acceso público.

Power BI consume directamente desde la URL S3.

💡 Panel de visualización

Métricas destacadas:

Precio promedio general

Total de anuncios, anfitriones y barrios

Porcentaje de ocupación ideal (>200 días/año)

Porcentaje de alojamientos completos y en Manhattan

Gráficos:

Top 5 distritos con más anuncios

Distribución por tipo de habitación

Mapa interactivo de barrios

Captura del dashboard final:



🏗️ Arquitectura del pipeline

El siguiente pipeline resume el flujo de trabajo del proyecto:



Carga de datos locales en formato CSV

Limpieza y transformación en Python

Exportación a Parquet

Carga a AWS S3 con permisos de acceso público

Visualización en Power BI desde la URL

🚫 Limitaciones

No se consideró la evolución temporal ni tendencias por mes.

La ubicación se usó solo en el mapa, no en segmentaciones espaciales avanzadas.

🎯 Futuras mejoras

Conexión directa con Athena desde Power BI

Análisis de predicción de precios con ML

Dashboard PWA para dispositivos móviles

📅 Estado del proyecto

✅ Completado y funcional.

👤 Autor

Octavio AlvarezLinkedIn
