# 🧼 Limpieza y Auditoría de Datos Comerciales con Python

## 📝 Descripción del Proyecto
Este proyecto implementa un flujo de trabajo automatizado en Python para el procesamiento y purificación de datos (*Data Wrangling*). Se procesó un volumen de más de 1,000 registros de ventas tecnológicas, simulando las inconsistencias y errores humanos más comunes en los sistemas de captura (ERP/CRM) para transformarlos en una base de datos estructurada, limpia y lista para analítica avanzada.

## 🛠️ Tecnologías y Librerías
- **Python:** 
- **Pandas:** Manipulación de DataFrames, normalización de strings y gestión de registros corruptos.
- **NumPy:** Computación matemática para el cálculo e imputación de métricas financieras.

## 🚀 Desafíos Técnicos Resueltos (Paso a Paso)
1. **Auditoría e Inspección Semántica:** Diagnóstico automático mediante `.isnull().sum()` y `.duplicated()` para cuantificar el estado de corrupción del archivo original.
2. **Control de Duplicados Masivos:** Eliminación de registros de ventas idénticos mediante `.drop_duplicates()` para evitar la sobreestimación de ingresos.
3. **Normalización de Texto y Resolución de Tildes:** Uso de `.str.lower().str.capitalize()` y reemplazos lógicos con `.replace()` para consolidar variantes inconsistentes (ej. *celulares, CELULARES, electrodomesticos* -> *Celulares, Electrodomésticos*).
4. **Sanación de Codificación (Character Encoding):** Implementación de codificación universal `utf-8-sig` para corregir la corrupción de caracteres especiales (é, Ñ) al exportar hacia herramientas tradicionales como Microsoft Excel.
5. **Tratamiento Avanzado de Nulos (Imputación):** Remoción de filas críticas huérfanas de autoría (Asesor nulo) y sustitución inteligente de montos financieros vacíos utilizando el promedio estadístico general de la tienda mediante NumPy.

## 📊 Estructura de Datos Final
El script exporta de manera limpia un archivo optimizado con dos categorías unificadas:
- `Celulares`
- `Electrodomésticos`
