# ML-IQ: Introducción al Machine Learning en Ingeniería Química

Material del taller práctico de Machine Learning para el curso de Termodinámica de Procesos. El objetivo es predecir la potencia generada en turbinas a partir de datos de operación, poniendo énfasis en el análisis y la limpieza de datos con criterio físico, y en la comparación con modelos termodinámicos.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/crjacinto/ML-IQ/blob/main/ML_IQ.ipynb)

## Contenido

```
ML-IQ/
├── data/
│   ├── Datos_CH.csv      # Turbina de vapor de un ingenio azucarero (zafra 2025–2026)
│   └── gt_2011.csv       # Turbina de gas, UCI (promedios horarios, 2011)
└── ML_IQ.ipynb           # Notebook del taller
```

## Uso

La forma recomendada es abrir el notebook en Google Colab con el botón de arriba. No requiere instalación: los datos se descargan directamente desde este repositorio. La primera celda imprime las versiones de las librerías; si tus resultados difieren de los publicados, compáralas.

Si la descarga falla, sube los archivos de `data/` desde el panel de archivos de Colab y reemplaza `URL_INGENIO` y `URL_TURBINA` por los nombres de archivo en la celda indicada del notebook.

Para ejecutarlo localmente se necesita Python 3.11+ con `numpy`, `pandas`, `matplotlib` y `scikit-learn`. La sección de modelos termodinámicos requiere además `iapws` (versión fija, porque los resultados de esa sección dependen de ella). La celda del anexo para exportar a PDF solo funciona en Colab.

## Datos

- **Datos_CH.csv**: un registro por día (probablemente promedios diarios) de la turbina de extracción-condensación de un ingenio azucarero local. Las presiones son manométricas, en kg/cm². Incluye el arranque de zafra, paradas, valores congelados y un cambio de régimen al terminar la molienda; no se ha limpiado a propósito.
- **gt_2011.csv**: Gas Turbine CO and NOx Emission Data Set, [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/551/gas+turbine+co+and+nox+emission+data+set). El repositorio original contiene los años 2011–2015; aquí se usa solo 2011. Nota: la fuente indica `CDP` en mbar, pero los valores (~12) corresponden a bar.

  Kaya, H., Tüfekci, P., & Uzun, E. (2019). Predicting CO and NOx emissions from gas turbines: novel data and a benchmark PEMS. *Turkish Journal of Electrical Engineering and Computer Sciences*, 27, 4783–4796.
