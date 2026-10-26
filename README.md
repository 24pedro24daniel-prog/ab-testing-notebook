# A/B Testing: Publicidad estática (A) vs. Publicidad variante (B)

Notebook de Jupyter que analiza un experimento A/B clásico de publicidad: un **anuncio base (A)** frente a un **anuncio variante (B)**, midiendo CTR y tasa de conversión, y determinando si la diferencia es estadísticamente significativa.

## Contenido

- `ab_testing_publicidad.ipynb`: notebook principal con:
  1. Simulación de un experimento (impresiones, clics, conversiones por grupo).
  2. Métricas descriptivas (CTR, tasa de conversión) por anuncio.
  3. Visualizaciones con intervalos de confianza del 95%.
  4. Pruebas de hipótesis: z-test de proporciones y chi-cuadrado de independencia.
  5. Conclusión y recomendación de negocio (adoptar B, mantener A, o seguir probando).
  6. Guía para sustituir los datos simulados por datos reales (CSV propio).

## Requisitos

- Python 3.9+

## Instalación

```bash
pip install -r requirements.txt
```

## Ejecutar

```bash
jupyter notebook ab_testing_publicidad.ipynb
```

o ábrelo directamente en VS Code / JupyterLab.

## Usar tus propios datos

Reemplaza la celda de simulación por la carga de un CSV con columnas `grupo` (`A`/`B`), `click` (0/1) y `conversion` (0/1):

```python
df = pd.read_csv('mi_experimento.csv')
```

y vuelve a ejecutar el resto de las celdas.
