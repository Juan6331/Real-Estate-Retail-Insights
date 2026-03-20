# 🏠 Análisis del Mercado Inmobiliario — King County, Seattle
![Python](https://img.shields.io/badge/Python-3.9-blue)
![scikit-learn](https://img.shields.io/badge/sklearn-regresión-orange)
![Dataset](https://img.shields.io/badge/Dataset-21600_propiedades-lightgrey)
## ️ Contexto de negocio
El mercado inmobiliario de King County (Seattle) presenta alta volatilidad en precios.
El objetivo fue identificar qué características físicas y de ubicación tienen mayor
impacto en el precio de venta, para apoyar decisiones de inversión y tasación.
## ❓ Pregunta analítica
> ¿Qué variables (tamaño, ubicación, vista al agua) tienen mayor peso en el precio
> de una propiedad en King County?
## 🔧 Herramientas y proceso
- **Python** (pandas, numpy) → Limpieza de 21,600 registros
- **Seaborn / Matplotlib** → Análisis de distribución de precios
- **Scikit-learn** → Modelo de regresión lineal múltiple
- **Folium** → Mapa de calor de precios por ZIP code (opcional)
## 📊 Hallazgos principales
| Variable | Impacto en precio |
|------------------|------------------------------------------|
| Vista al agua | +25% en promedio vs propiedades sin vista |
| sqft_living | Correlación 0.70 con el precio |
| Grado de calidad | Diferencia de $200K entre grado 7 y 10 |
| ZIP code | Varianza de $400K entre zonas más caras |
**RMSE del modelo:** $142,000 USD | **R2:** 0.68

El modelo explica el 68% de la varianza en precio — resultado sólido para un modelo lineal de primera iteración. Las variables no incluidas (antigüedad del vecindario, datos de criminalidad por ZIP, cercanía a escuelas) podrían mejorar el R² a ~0.80 en una segunda versión

## 💡 Recomendación
Para un inversionista: priorizar propiedades con vista al agua en ZIP codes premium
y sqft_living > 2,000. El modelo puede estimar precio de compra con error de ±$142K,
útil como primera referencia de tasación rápida.

```
