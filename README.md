# Prediccion de conversion en e-commerce: Que comportamiento web predice una compra?

## Descripcion
Analisis de machine learning sobre sesiones web de usuarios en una tienda online para predecir si una sesion terminara en compra, e identificar los comportamientos mas importantes para esa decision. Incluye comparacion de modelos, evaluacion con metricas apropiadas para datos desbalanceados, interpretacion con SHAP y recomendaciones de marketing.

## Dataset
- **Fuente:** [UCI ML Repository - Online Shoppers Purchasing Intention](https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset)
- **Tamano:** 12,330 sesiones x 18 variables (12,205 tras eliminar duplicados)
- **Variable objetivo:** `Revenue` (True/False) - si la sesion termino en compra
- **Desbalance:** ~15% de sesiones terminan en compra
- El notebook **descarga el dataset automaticamente** desde UCI; no es necesario bajarlo a mano.

## Enfoque
**Prediccion supervisada (clasificacion binaria):** comparacion de Regresion Logistica vs Random Forest, evaluacion con accuracy, precision, recall, F1, ROC-AUC y PR-AUC, e interpretacion del mejor modelo con SHAP.

## Resultados principales
- **Mejor modelo:** Random Forest (ROC-AUC 0.924, PR-AUC 0.731 en el conjunto de prueba).
- **Variable mas influyente:** `PageValues` (valor de las paginas visitadas), seguida de las tasas de salida/rebote, el mes y la navegacion de productos.
- Se incluyen matrices de confusion, curvas ROC/PR, analisis de sensibilidad del umbral y recomendaciones de marketing basadas en la probabilidad de compra de cada sesion.

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

3. Abrir el notebook y ejecutarlo de principio a fin (descarga los datos automaticamente):
   ```bash
   jupyter notebook notebooks/analisis_conversion.ipynb
   ```

## Estructura del proyecto
```
proyecto-final-curso3-prediccion-conversion/
|-- README.md
|-- requirements.txt
|-- .gitignore
|-- data/                  # el CSV se descarga aqui al correr el notebook (no se versiona)
|-- notebooks/
|   `-- analisis_conversion.ipynb
`-- figures/
```

## Contenido del notebook
1. **Problema y datos** - pregunta, dataset, exploracion y limpieza
2. **Modelado / Analisis** - Pipeline, Regresion Logistica vs Random Forest, metricas y evaluacion
3. **Interpretacion** - SHAP sobre el mejor modelo
4. **Conclusiones** - respuesta, limitaciones y recomendaciones
5. **Uso de IA** - documentacion del uso de herramientas de IA

## Autora
Juliana Castano Yarce

## Curso
Modelado predictivo, automatizacion y proyectos inteligentes - Proyecto Final (Curso III)
