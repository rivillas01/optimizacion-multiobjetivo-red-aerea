# Optimización multiobjetivo de redes de transporte aéreo

Repositorio asociado al Trabajo Fin de Grado en Ingeniería Industrial de la Universidad Internacional de Valencia (VIU).

**Autora:** Angie Katherin Rivillas C.  
**Título:** Formulación y resolución de un modelo de optimización multiobjetivo para la planificación eficiente y sostenible de redes de transporte internacional de pasajeros bajo restricciones operativas

## Descripción

El proyecto formula y resuelve un modelo de programación lineal entera binaria multiobjetivo para la selección de itinerarios aéreos, considerando simultáneamente coste, tiempo de viaje y emisiones de CO₂. La estrategia de resolución utiliza el método ε-Constraint y un criterio posterior de distancia al punto ideal normalizado para seleccionar una solución de compromiso.

## Estructura del repositorio

- `datos/red_aerea.xlsx`: datos de entrada utilizados por el modelo.
- `notebooks/01_modelo_base.ipynb`: notebook original de desarrollo, con sus salidas.
- `notebooks/01_modelo_base_limpio.ipynb`: mismo código sin salidas previas.
- `resultados/`: archivos Excel generados durante la resolución y validación.
- `figuras/`: figuras generadas a partir de los resultados.
- `requirements.txt`: principales dependencias del proyecto.

## Caso de estudio

La red considerada incluye ocho aeropuertos del Sudeste Asiático y 28 conexiones bidireccionales. El itinerario estudiado tiene como origen Bangkok (BKK) y destino Denpasar–Bali (DPS).

La ejecución documentada en el TFG contempla 25 escenarios ε-Constraint, de los cuales 22 resultaron factibles. Tras eliminar duplicidades y aplicar el análisis de dominancia, se identificaron cuatro soluciones no dominadas. Bajo el criterio de igual importancia relativa entre los tres objetivos, la solución de compromiso seleccionada fue S2: BKK → SIN → DPS.

## Reproducción

El notebook está desarrollado en Python mediante Jupyter Notebook y utiliza Gurobi como solver. También emplea pandas, NumPy, Matplotlib y openpyxl.

Instalación orientativa:

```bash
pip install -r requirements.txt
```

La reproducción requiere una instalación y licencia válidas de Gurobi. El notebook debe ejecutarse manteniendo la estructura de carpetas del repositorio, ya que utiliza rutas relativas hacia `datos`, `resultados` y `figuras`.

## Nota sobre reproducibilidad

Este repositorio conserva el notebook original y los archivos originales de datos, resultados y figuras de la carpeta de desarrollo del TFG. La copia denominada `01_modelo_base_limpio.ipynb` únicamente elimina las salidas de ejecución; no modifica el código.

La preparación del repositorio no implica una nueva ejecución integral del modelo.

## Citación

Angie Katherin Rivillas C. *Formulación y resolución de un modelo de optimización multiobjetivo para la planificación eficiente y sostenible de redes de transporte internacional de pasajeros bajo restricciones operativas*. Trabajo Fin de Grado, Universidad Internacional de Valencia (VIU), 2026.

URL del repositorio: https://github.com/rivillas01/optimizacion-multiobjetivo-red-aerea
