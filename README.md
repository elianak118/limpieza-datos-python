# limpieza-datos-python
Proyecto de Datos en Python para la limpieza y auditoría de 1,000 registros comerciales de telefonía. Automatiza la detección de duplicados, la normalización de texto y el tratamiento de valores nulos con Pandas y NumPy, optimizando la base de datos para análisis estadístico.

## 🛠️ Tecnologías Utilizadas
- **Python**
- **Pandas** (Estructuración de DataFrames, eliminación de duplicados y manejo de nulos)
- **NumPy** (Cálculos matemáticos para imputación de datos estadísticos)

## 🚀 Fases del Proceso de Limpieza
1. **Diagnóstico Inicial:** Conteo automático de registros corruptos, celdas vacías (`NaN`) y filas repetidas.
2. **Tratamiento de Duplicados:** Remoción de registros de ventas idénticos mediante `.drop_duplicates()`.
3. **Estandarización de Texto:** Homologación sintáctica de categorías comerciales escritas inconsistentemente (ej. celulares, CELULARES -> Celulares).
4. **Imputación de Valores Faltantes:** Eliminación de filas críticas sin autoría y reemplazo de montos de venta vacíos utilizando el promedio financiero calculado con NumPy.
