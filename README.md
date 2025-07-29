# 🌆 Análisis y Visualización de Airbnb NYC

Este proyecto tiene como objetivo analizar y visualizar datos de Airbnb en la ciudad de Nueva York, utilizando herramientas de procesamiento de datos en Python, almacenamiento en la nube con AWS S3, y visualización interactiva mediante Power BI.

---

## 🚀 Tecnologías utilizadas

- **Python** (`pandas`, `pyarrow`): limpieza y transformación de datos.
- **AWS S3**: almacenamiento de archivos Parquet accesibles desde URL pública.
- **Power BI**: visualización de datos, KPI, mapas y análisis interactivo.
- **Formato Parquet**: optimiza el rendimiento en la carga y consulta de datos.

---

## 📊 Dataset

El dataset fue extraído de Kaggle: [New York City Airbnb Open Data](https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data)

Incluye información detallada de anuncios publicados en Airbnb:

- ID de anuncio y anfitrión
- Localización geográfica
- Tipo de habitación
- Precio por noche
- Mínimo de noches requeridas
- Disponibilidad en el año (`availability_365`)
- Número de reseñas y más

---

## 📁 Proceso ETL

1. ✅ Carga del archivo original en formato CSV
2. ✅ Limpieza de filas incompletas o erróneas
3. ✅ Conversión de columnas a tipos numéricos válidos
4. ✅ Filtrado de precios sospechosos (`price < 10` o `price > 1000`)
5. ✅ Exportación a formato `.parquet` para optimizar carga
6. ✅ Subida del archivo limpio a un bucket público en AWS S3
7. ✅ Conexión directa desde Power BI a la URL de S3

---

## 💡 Panel de visualización

### 🧮 Métricas clave:

- **Precio promedio general**
- **Total de anuncios**
- **Cantidad de anfitriones**
- **Total de barrios**
- **% Ocupación ideal** (availability > 200 días)
- **% Alojamiento tipo "entire home"**
- **% Anuncios en Manhattan**

### 📊 Gráficos:

- Top 5 distritos con más anuncios
- Distribución por tipo de habitación
- Mapa interactivo de barrios

### 📸 Captura del dashboard final:

Imagenes/dashboard.png


---

## 🏗️ Arquitectura del pipeline

El siguiente pipeline resume el flujo completo:

1. 🧾 Carga de datos CSV desde Kaggle
2. 🧹 ETL en Python (`pandas`, `pyarrow`)
3. 📦 Exportación a Parquet
4. ☁️ Almacenamiento en **AWS S3** (público)
5. 📊 Visualización desde Power BI vía URL Parquet

![Pipeline](./Captura%20de%20pantalla%202025-07-29%20141122.png)

---

## 🚫 Limitaciones

- No se incluyó análisis temporal ni tendencias mensuales.
- La geolocalización fue usada solo para mapeo, no para segmentaciones espaciales avanzadas.

---

## 🎯 Futuras mejoras

- Integrar **Amazon Athena** como fuente directa para Power BI.
- Incluir análisis de predicción de precios mediante ML.
- Desarrollar una PWA para visualización desde móvil.

---

## 📅 Estado del proyecto

✅ **Completado y funcional**

---

## 👤 Autor

**Octavio Alvarez**  
[LinkedIn](https://www.linkedin.com/in/octavioalvarez)

---


