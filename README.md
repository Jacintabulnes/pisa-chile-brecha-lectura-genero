# La brecha de género en comprensión lectora en Chile

## Descripción

Esta visualización analiza la evolución de los puntajes de comprensión lectora de mujeres y hombres chilenos en PISA entre 2000 y 2022.

La pregunta que guía el análisis es: **¿por qué se redujo la ventaja de las mujeres chilenas en comprensión lectora?**

La hipótesis es que la reducción reciente de la brecha se explica principalmente por una caída del puntaje femenino y no por una mejora estadísticamente significativa del masculino.

## Fuente de datos

- **Institución:** Agencia de Calidad de la Educación de Chile.
- **Documento:** Informe de resultados PISA 2022.
- **Referencia específica:** página 26, gráfico «Lectura: tendencia Chile según sexo 2000–2022».
- **Período:** 2000, 2006, 2009, 2012, 2015, 2018 y 2022.
- **Cobertura:** estudiantes de Chile participantes en PISA.
- **Unidad de análisis:** puntaje promedio de comprensión lectora por año y sexo.

Los datos fueron transcritos de los valores publicados en el gráfico oficial. No se utilizaron microdatos individuales.

## Preparación y limpieza

1. Se identificaron los puntajes de mujeres y hombres para cada año disponible.
2. Se transcribieron los valores a una tabla estructurada.
3. Se transformó la tabla a formato largo mediante `pandas.melt()`, con una fila por año y sexo.
4. Se crearon las columnas `anio`, `sexo`, `puntaje_lectura` y `fuente`.
5. Se exportó la tabla limpia a CSV para su visualización.

No se aplicaron imputaciones ni se modificaron los puntajes originales.

## Diccionario de variables

| Variable | Descripción |
|---|---|
| `anio` | Año de aplicación de PISA |
| `sexo` | Mujeres u hombres |
| `puntaje_lectura` | Puntaje promedio en comprensión lectora |
| `fuente` | Documento del cual se obtuvo el dato |

## Visualización

El gráfico fue desarrollado en Python con Altair. Se utilizaron dos líneas para comparar las trayectorias de mujeres y hombres, con colores diferenciados, puntos por medición y etiquetas en los resultados de 2022.

La versión HTML permite consultar los valores mediante el cursor. La versión JPG corresponde a la exportación estática.

## Hallazgo principal

Entre 2018 y 2022, el puntaje femenino descendió de 462 a 451 puntos, mientras que el masculino pasó de 442 a 445. La brecha se redujo de 20 a 6 puntos.

Según el informe oficial, la diferencia entre mujeres y hombres dejó de ser estadísticamente significativa en 2022.

## Limitaciones

Los valores provienen de un gráfico publicado y están expresados en puntos enteros. La base no incluye errores estándar ni intervalos de confianza. Por ello, la significancia estadística se interpreta a partir del informe oficial y no de cálculos propios.

La visualización permite describir tendencias, pero no establecer las causas de los cambios.

## Reproducción

1. Abrir el archivo `.ipynb` en Google Colab.
2. Ejecutar todas las celdas en orden.
3. El cuaderno genera automáticamente el CSV utilizado.
4. El gráfico se construye con pandas y Altair.
5. Las últimas celdas exportan las versiones HTML, PNG y JPG.

Para exportar imágenes puede ser necesario instalar `vl-convert-python`.

## Archivos del proyecto

- Cuaderno `.ipynb`: código y procesamiento.
- CSV: base limpia utilizada.
- HTML: visualización interactiva.
- JPG: visualización estática.
- `cronica.md`: texto periodístico que acompaña el gráfico.

## Proyecto grupal

Este análisis forma parte de la investigación grupal sobre desigualdades en comprensión lectora en Chile.

[Ver repositorio grupal](https://github.com/Jacintabulnes/pisa-chile-educacion)
