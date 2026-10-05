# TP Final - Aprendizaje de Máquina I (CEIA - FIUBA)

## Detección de fugas internas en la bomba de un sistema hidráulico

**Integrantes:** Nelson Martín Villagra y Víctor Hugo Astorga

Usamos los datos de un banco de pruebas hidráulico (17 sensores, ciclos de 60 segundos) para clasificar el estado de la bomba principal en tres clases: sin fuga, fuga leve y fuga severa. Todo el trabajo (análisis, modelos, resultados y conclusiones) está en el notebook `tp_final.ipynb`.

### Dataset

*Condition monitoring of hydraulic systems* (ZeMA gGmbH), descargado de Kaggle:

https://www.kaggle.com/datasets/jjacostupa/condition-monitoring-of-hydraulic-systems

El original está en el UCI Machine Learning Repository: https://archive.ics.uci.edu/dataset/447/condition+monitoring+of+hydraulic+systems

El dataset no está incluido en este repositorio porque descomprimido pesa unos 550 MB.

### Cómo correrlo

1. Descargar el dataset desde Kaggle y descomprimirlo en una carpeta `data/` dentro de este repositorio. Tiene que quedar así:

   ```
   tp_final.ipynb
   data/
   ├── PS1.txt ... PS6.txt
   ├── EPS1.txt, FS1.txt, FS2.txt
   ├── TS1.txt ... TS4.txt, VS1.txt
   ├── CE.txt, CP.txt, SE.txt
   └── profile.txt
   ```

2. Instalar las dependencias con [uv](https://docs.astral.sh/uv/):

   ```bash
   uv sync
   ```

3. Abrir el notebook y ejecutar todas las celdas (tarda unos 3 minutos):

   ```bash
   uv run jupyter notebook tp_final.ipynb
   ```
