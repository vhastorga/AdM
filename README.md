# TP Final - Aprendizaje de Máquina I (CEIA - FIUBA)

## Detección de fugas internas en la bomba de un sistema hidráulico

**Integrantes:** Nelson Martín Villagra y Víctor Hugo Astorga

Usamos los datos de un banco de pruebas hidráulico (17 sensores, ciclos de 60 segundos) para clasificar el estado de la bomba principal en tres clases: sin fuga, fuga leve y fuga severa. El trabajo tiene dos notebooks:

- `tp_final.ipynb` (Parte I): análisis exploratorio, baseline, comparación de modelos y elección del modelo.
- `tp_final_parte2.ipynb` (Parte II): ponemos a prueba las conclusiones de la Parte I sacando los sensores calculados y evaluando con una temperatura que el modelo no vio.

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

3. Abrir los notebooks y ejecutar todas las celdas (la Parte I tarda unos 3 minutos y la Parte II unos 2):

   ```bash
   uv run jupyter notebook
   ```
