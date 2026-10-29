# App interactiva de EDA y reducción de dimensionalidad (Streamlit)

Aplicación web en **Streamlit** para explorar un dataset, preprocesarlo y comparar técnicas de reducción de dimensionalidad con métricas objetivas.

## Funcionalidades
- **Carga de datos**: archivo local o dataset de ejemplo (Abalone, descargado automáticamente).
- **Exploración**: estadísticas, reporte de valores faltantes, histogramas, boxplots y matriz de correlación.
- **Preprocesamiento**: imputación (simple / KNN), escalado (Standard / MinMax) y codificación de variables categóricas.
- **Reducción de dimensionalidad**: **PCA, LDA, t-SNE y UMAP**, con hiperparámetros ajustables y modo comparativo.
- **Evaluación del embedding**: Silhouette, ARI, NMI (sobre K-Means) y accuracy de kNN.
- **Exportación**: datos filtrados, embeddings y figuras.

## Ejecución
```bash
pip install -r requirements.txt
streamlit run app.py
```
Luego abre la URL que indica Streamlit (por defecto `http://localhost:8501`). Para exportar imágenes se requiere `kaleido`.

## Estructura
```
app.py                                   # Aplicación Streamlit
requirements.txt
Abulon.xlsx                              # Dataset de ejemplo (Abalone)
docs/decisiones_preprocesamiento.pdf     # Justificación de las decisiones de preprocesamiento
```

**Stack:** Python · Streamlit · scikit-learn · UMAP · Plotly · Altair · Seaborn
