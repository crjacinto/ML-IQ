# ML-IQ: Introducción al Machine Learning en Ingeniería Química

Material del taller práctico de Machine Learning para el curso de Termodinámica de Procesos. El objetivo es predecir la potencia generada en turbinas a partir de datos de operación, poniendo énfasis en el análisis y la limpieza de datos con criterio físico.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/crjacinto/ML-IQ/blob/main/taller_ml_iq.ipynb)

## Contenido

```
ML-IQ/
├── data/
│   ├── Datos_CH.csv      # Turbina de vapor de un ingenio azucarero (zafra 2025–2026)
│   └── gt_2011.csv       # Turbina de gas, UCI (promedios horarios, 2011)
└── taller_ml_iq.ipynb    # Notebook del taller
```

## Uso

La forma recomendada es abrir el notebook en Google Colab con el botón de arriba. No requiere instalación: los datos se descargan directamente desde este repositorio.

Para ejecutarlo localmente se necesita Python 3.11+ con `numpy`, `pandas`, `matplotlib` y `scikit-learn`. La sección de modelos termodinámicos requiere además `iapws`.

## Datos

- **Datos_CH.csv**: registros diarios de operación de la turbina de extracción-condensación de un ingenio azucarero local.
- **gt_2011.csv**: Gas Turbine CO and NOx Emission Data Set, [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/551/gas+turbine+co+and+nox+emission+data+set). El repositorio original contiene los años 2011–2015.

  Kaya, H., Tüfekci, P., & Uzun, E. (2019). Predicting CO and NOx emissions from gas turbines: novel data and a benchmark PEMS. *Turkish Journal of Electrical Engineering and Computer Sciences*, 27, 4783–4796.
