# Prueba técnica de Ciencia de Datos

Este repositorio contiene los dos ejercicios de la prueba técnica.

## Parte 1. Comparación de modelos de clasificación

Notebook: `proyecto_cancer.ipynb`

Se compararon tres modelos (regresión logística, SVM y Random Forest) para clasificar tumores como malignos o benignos con el dataset de cáncer de mama de Wisconsin incluido en scikit-learn. El notebook incluye la exploración de los datos, la división en entrenamiento, validación y prueba, el ajuste de hiperparámetros con validación cruzada, la evaluación con matriz de confusión, métricas y curva ROC, y la evaluación final del modelo elegido en el conjunto de prueba.

## Parte 2. Chatbot con RAG sobre óperas de Puccini

Notebook: `Chatbot_Puccini_c.ipynb`

Se construyó un chatbot que responde preguntas sobre *La bohème*, *Tosca* y *Turandot* usando como documentos los artículos de Wikipedia en español de cada ópera (los documentos `La_bohème_(Puccini).pdf`, `Tosca_(ópera).pdf` y `Turandot.pdf`). El texto se dividió en chunks de 150 palabras con traslape de 40, los embeddings se generaron con `intfloat/multilingual-e5-small` y las respuestas se generan con Google Gemini.

Las 20 preguntas de evaluación con sus respuestas correctas están en `preguntas_evaluacion.csv`. La recuperación se evaluó con Hit Rate@k y MRR, y la generación con similitud semántica y con un LLM como juez.

## Cómo ejecutar

Parte 1:
pip install scikit-learn pandas matplotlib seaborn

Parte 2:
pip install pypdf sentence-transformers google-genai pandas

La Parte 2 necesita una API key de Gemini, que el notebook pide al ejecutarse (no está guardada en el repositorio).
