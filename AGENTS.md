# AGENTS.md — Proyecto Integrador UPATECO (Visualización y Narrativa de Datos)

Instrucciones de proyecto para el agente de IA. Se cargan automáticamente en cada sesión.

## Contexto

- Proyecto académico: tablero de control sobre `data/raw/operacion_organizacion.csv`
  (506 operaciones, 2023-01-02 → 2025-06-25, 12 columnas).
- Entregables: notebooks Google Colab en `notebooks/etapa_1/`
  (`Proyecto_Integrador_Unidad_I.ipynb`) y `notebooks/etapa_2/`
  (`Proyecto_Integrador_Etapa_2.ipynb`).
- Nueva evidencia de la etapa_2: `docs/Caso 8.pdf` (estacionalidad sep–nov 2024).
- **Idioma de los entregables: español.** Consigna: analizar solo con la evidencia
  del dataset y los `docs/*.pdf`; no incorporar información externa.
- `data/raw/` es intocable: el análisis trabaja sobre una **copia** (`datos = df.copy()`).

## Identidad visual (obligatorio)

Paleta oficial en `Esquema de Colores.txt` (fuente autoritativa):

| Elemento | HEX |
|---|---|
| h1 | `#8B5CF6` |
| h2 | `#de9f68` |
| h3 | `#e391e3` |
| h4 | `#d6a487` |
| Destacado | `#a091e3` |
| Listas | `#91b9e3` |
| Resaltado | `#adc261` |

Aplicar estos HEX en documentos markdown/HTML y en gráficos Plotly del proyecto.

## Convenciones de código

- Carga de datos con fallback: ruta local → URL cruda GitHub → Google Drive → subida manual.
- Visualizaciones con **Plotly** (`plotly.express`, `plotly.graph_objects`,
  `plotly.subplots.make_subplots`); template por defecto `plotly_white`.
- No dejar archivos temporales ni scratch en el repositorio (usar temp y limpiar).
- Notebooks ejecutables de punta a punta sin errores; validar con `nbformat.validate`.
