
 # 🧠 *Multimodal Deep Learning model for Predicting Tourist Engagement*
  > *"Garbage In, Garbage Out"*
---

*Este proyecto utiliza técnicas avanzadas de **Deep Learning multimodal** para predecir el **nivel de engagement (alto o bajo)** que generarán distintos **Puntos de Interés turísticos (POIs)** combinando imágenes y metadatos.*

---

## 📌 Descripción

El modelo desarrollado integra dos fuentes de información complementarias:

- **Características visuales:** extraídas de imágenes con una red neuronal convolucional (CNN).
-  **Metadatos estructurados:** como ubicación geográfica, etiquetas, categoría, nivel de popularidad, etc.

El objetivo es clasificar automáticamente cada POI como de **alto o bajo engagement** utilizando un enfoque **multimodal**.

---

## 🛠️ Tecnologías y herramientas utilizadas

| Área              | Herramientas y librerías |
|-------------------|--------------------------|
| Manipulación de datos | `pandas`, `numpy` |
| Visualización | `matplotlib`, `seaborn`, `plotly` |
| Aprendizaje automático | `scikit-learn` (KMeans, escaladores) |
| Deep Learning | `PyTorch`, `torchvision.transforms`, `torchinfo` |
| Carga y procesamiento | `PIL`, `tqdm`, `custom Dataset` |
| Entorno | `Google Colab`, `Jupyter Notebooks` |

---

## 📦 Componentes del modelo

- `VisualCNN`: Red convolucional para extraer características de imágenes.
- `TabularNN`: Red densa para procesar metadatos estructurados.
- `MultimodalNet`: Modelo combinado que fusiona ambos vectores de características.
- Función de pérdida: `BCEWithLogitsLoss`
- Optimizador: `Adam`
- Métricas: Exactitud, precisión, recall, F1-score

---

## 🧪 Flujo de trabajo

1. **Exploración y limpieza del dataset**
2. **Feature Engineering** sobre variables como tags, ubicación, popularidad
3. **Preprocesamiento de imágenes** con `torchvision.transforms`
4. **Clustering geográfico** con KMeans
5. **Normalización** y división del dataset (70% train, 15% val, 15% test)
6. **Construcción del Dataset personalizado**
7. **Entrenamiento de modelo multimodal**
8. **Evaluación con métricas de clasificación**

---

##  Objetivo

Predecir si un punto turístico generará **engagement alto o bajo** con base en su contenido visual y atributos contextuales, aplicando una arquitectura de red **multimodal**.

---

##  Notas finales

- Este proyecto aún está en progreso y continuará siendo actualizado.
- ¡Tu feedback es bienvenido! Si tienes ideas, mejoras o sugerencias, no dudes en abrir una issue o pull request.
