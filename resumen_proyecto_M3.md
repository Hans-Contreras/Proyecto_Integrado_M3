# Proyecto ABP: Preparación de Datos con Python

## Justificación de uso
- **NumPy** fue utilizado por su eficiencia en operaciones vectorizadas y creación de datos simulados.
- **Pandas** permitió transformar, explorar y limpiar estructuras tabulares de manera eficiente.

## Descripción de los datos
- Datos ficticios de clientes con variables como ID, nombre, edad, ciudad, total de compras y monto total.
- Se integraron datos desde:
  - Archivo CSV (`clientes_ecommerce.csv`)
  - Archivo Excel (`clientes_ecommerce.xlsx`)
  - Una tabla web pública de Wikipedia (comunas de Chile).

## Técnicas aplicadas

### Limpieza de datos
- **Valores nulos** imputados con la media.
- **Outliers** detectados mediante **Z-score** y removidos.

### Data Wrangling
- Conversión de tipos (`ID` a string).
- Eliminación de duplicados.
- Creación de nuevas columnas:
  - `Monto_Promedio` por compra.
  - `Monto_Normalizado` por escalamiento min-max.

### Agrupamiento y pivoteo
- Se utilizó `groupby()` para agrupar por cantidad de compras.
- Se aplicó `pivot_table()` para organizar el monto total promedio por nivel de compras.

## Decisiones tomadas
- Outliers con Z-score > 3 fueron eliminados para asegurar consistencia.
- Se mantuvo el duplicado entre CSV y Excel para simular integración de múltiples fuentes.
- Las columnas creadas facilitarán análisis predictivo posterior.

## Resultados
- Dataset final limpio, transformado y exportado en formatos **CSV y Excel**.
- Listo para su uso en modelos de análisis o dashboards de negocio.


---
