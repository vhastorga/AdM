# TP Final — Aprendizaje de Máquina I (CEIA-FIUBA)

## Monitoreo de Condición de un Sistema Hidráulico mediante Aprendizaje de Máquina

**Materia:** Aprendizaje de Máquina I — Especialización en Inteligencia Artificial, CEIA–FIUBA  
**Dataset:** *Condition monitoring of hydraulic systems* (ZeMA / UCI Machine Learning Repository #447, descargado vía mirror de Kaggle)  
**Fecha:** Octubre 2026  
**Integrantes:** Nelson Martín Villagra (nelsonmvillagra1976@gmail.com) y Víctor Hugo Astorga (vhastorga@gmail.com)

### Descripción

Este proyecto aborda el mantenimiento predictivo de un banco de pruebas hidráulico.
A partir de datos de 17 sensores muestreados durante ciclos de trabajo de 60 segundos,
se extraen características estadísticas por ciclo y se entrenan modelos de clasificación
para determinar el estado de degradación de cuatro componentes: *cooler*, válvula, bomba
y acumulador hidráulico.

### Estructura del proyecto

```
Project/
├── pyproject.toml          # Dependencias y configuración del entorno (uv)
├── tp_final.ipynb          # Jupyter Notebook con el desarrollo completo
├── tp_final.tex            # Informe en LaTeX (formato IEEE)
├── references.bib          # Bibliografía en formato BibTeX
└── README.md               # Este archivo
```

### Instalación del entorno

```bash
# Requiere uv (https://docs.astral.sh/uv/)
uv sync
```

### Ejecución

```bash
uv run jupyter notebook tp_final.ipynb
```

### Dataset

El dataset debe estar ubicado en `../DataSET/` relativo a esta carpeta.
Fuente: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Condition+monitoring+of+hydraulic+systems)

### Referencias

- Helwig, N., Pignanelli, E., Schütze, A. (2015). *Condition Monitoring of a Complex Hydraulic System Using Multivariate Statistics*. IEEE I2MTC 2015.
- Schneider, T., Helwig, N., Schütze, A. (2017). *Automatic feature extraction and selection for classification of cyclical time series data*. tm – Technisches Messen 84(3).
