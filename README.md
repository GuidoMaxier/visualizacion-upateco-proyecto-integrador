# Proyecto Integrador Unidad I — Del dato a la decisión

**Tecnicatura universitaria en Ciencia de Datos e Inteligencia Artificial Aplicada** — **UPATECO**
**Materia:** Visualización y Narrativa de Datos (2026) · **Profesora:** María Dolores Costa

Proyecto integrador de la Unidad I: análisis de un dataset de operaciones y construcción de un **tablero de control** para la toma de decisiones, trabajando exclusivamente con la evidencia disponible (sin información externa, según consigna).

---

## Estructura del proyecto

```
├── data/
│   └── raw/                          # Datos crudos, tal como se entregaron (no se modifican)
│       └── operacion_organizacion.csv
├── notebooks/                        # Análisis y tablero de control (formato Google Colab), por etapa
│   └── etapa_1/
│       └── Proyecto_Integrador_Unidad_I.ipynb
├── docs/                             # Documentación, consigna y logo institucional
│   ├── Proyecto Integrador Unidad I.pdf
│   └── logo_upateco.png
├── README.md                         # Este archivo
└── .gitignore                        # Excluye .reasonix/ y artefactos
```

## Datos

`operacion_organizacion.csv` contiene **506 operaciones** registradas entre el **02/01/2023** y el **25/06/2025** (≈ 2,5 años), con 12 columnas:

| Columna | Descripción |
|---|---|
| `ID` | Identificador único de la operación |
| `Fecha` | Fecha de la operación |
| `Unidad` | Unidad organizacional (A–E) |
| `Region` | Región (Norte, Centro, Sur) |
| `Actividad` | Nivel de actividad esperado/planificado (actúa como meta, r = 0,97 con `Resultado`) |
| `Horas` | Horas invertidas |
| `Recursos` | Cantidad de recursos utilizados |
| `Incidentes` | Cantidad de incidentes |
| `Tiempo` | Tiempo de la operación |
| `Calidad` | Índice de calidad (0–100) |
| `Costo` | Costo de la operación |
| `Resultado` | Resultado efectivamente logrado |

## Consumir los datos desde GitHub (URL cruda)

Como el repositorio es **público**, el dataset se puede leer directamente desde la URL cruda:

```python
import pandas as pd

url = "https://raw.githubusercontent.com/GuidoMaxier/visualizacion-upateco-proyecto-integrador/main/data/raw/operacion_organizacion.csv"
df = pd.read_csv(url)
print(df.shape)  # (506, 12)
```


## Cómo ejecutar el notebook

1. Abrir [Google Colab](https://colab.research.google.com) → *Archivo → Subir notebook* (o arrastrar `notebooks/etapa_1/Proyecto_Integrador_Unidad_I.ipynb`).
2. El notebook busca los datos automáticamente en este orden:
   1. **Ruta local** (`operacion_organizacion.csv`, `data/raw/…`)
   2. **URL cruda de GitHub** (variable `GITHUB_RAW` en la celda de carga)
   3. **Google Drive** (montado)
   4. **Subida manual** (último recurso)
3. *Entorno de ejecución → Ejecutar todo*.

## Entregables del proyecto

- **Indicadores (KPIs):** resultado, cumplimiento (`Resultado/Actividad`), eficiencias por hora y por costo, costo promedio, tasa de incidentes, calidad y tiempo.
- **Visualizaciones:** tarjetas KPI, tendencia mensual/trimestral, comparativos por Unidad y Región, matriz de correlación, dispersiones, histograma y boxplot.
- **Tablero de control consolidado** (figura 3×2) para la presentación.
- **Conclusiones, decisiones propuestas, limitaciones y supuestos** fundamentados en los datos.

## Integrantes

1. **Hernan Guido Gustavo Casasola** — DNI 29.976.458
2. *—*
3. *—*

> Grupo: 1 integrante por el momento (se completa a medida que se sumen compañeros).

---

*Uso académico — todos los análisis se realizan exclusivamente sobre la evidencia del dataset.*
