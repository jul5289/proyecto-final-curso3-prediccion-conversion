# Prediccion de conversion en e-commerce: Que comportamiento web predice una compra?

## Descripcion
Analisis de machine learning sobre sesiones web de usuarios en una tienda online para predecir si un usuario terminara comprando, e identificar los factores de comportamiento mas importantes para esa decision.

## Dataset
- **Fuente:** [UCI ML Repository - Online Shoppers Purchasing Intention](https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset)
- **Tamano:** 12,330 sesiones x 18 variables
- **Variable objetivo:** `Revenue` (True/False) - si la sesion termino en compra
- **Desbalance:** ~15% de sesiones terminan en compra

## Enfoque
**Prediccion supervisada (clasificacion binaria)**: comparacion de al menos dos modelos para identificar el mejor predictor y luego interpretarlo con SHAP.

## Como reproducir el analisis

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/jul5289/proyecto-final-curso3-prediccion-conversion.git
   cd proyecto-final-curso3-prediccion-conversion
   ```

2. Crear un entorno virtual e instalar dependencias:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

3. Abrir el notebook:
   ```bash
   jupyter notebook notebooks/analisis_conversion.ipynb
   ```

## Estructura del proyecto
```
proyecto-final-curso3-prediccion-conversion/
|-- README.md
|-- requirements.txt
|-- .gitignore
|-- data/
|   `-- online_shoppers_intention.csv
|-- notebooks/
|   `-- analisis_conversion.ipynb
`-- figures/
```

## Autora
Juliana Castano Yarce

## Curso
Modelado predictivo, automatizacion y proyectos inteligentes - Proyecto Final (Curso III)
