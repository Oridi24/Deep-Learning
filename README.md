
 # 🧠 *Multimodal Deep Learning model for Predicting Tourist Engagement*
  > *"El aprendizaje profundo no es solo código, es un vistazo al futuro”.*
---

*Este proyecto utiliza técnicas avanzadas de **Deep Learning multimodal** para predecir el **nivel de engagement (alto o bajo)** que generarán distintos **Puntos de Interés turísticos (POIs)**  con base en su contenido visual y atributos contextuales, aplicando una arquitectura de red **multimodal**.*

---

## 📌 *Descripción*

*El modelo desarrollado integra dos fuentes de información complementarias:*

- ***Características visuales:*** *extraídas de imágenes con una red neuronal convolucional (CNN).*
-  ***Metadatos estructurados:*** *como ubicación geográfica, etiquetas, categoría, nivel de popularidad, etc.*

 🔹 1. ***Convolutional Neural Networks (CNNs)***:

*Las CNNs son redes neuronales diseñadas para procesar y extraer patrones de imágenes. A diferencia de una red normal que ve solo números crudos, las CNNs pueden detectar bordes, texturas, formas y combinarlos progresivamente hasta entender conceptos más complejos. En el proyecto, la CNN fue la encargada de “mirar” las fotos de los puntos turísticos y traducirlas en representaciones numéricas útiles para predecir engagement.*

🔹 2. ***Fully Connected Networks (Redes Densas para Tabular Data)***

*Los metadatos estructurados como categorías, ubicación o etiquetas de cada atracción, no son imágenes, sino tablas. Para procesarlos, se utilizan redes densas, también conocidas como fully connected layers, que permiten modelar relaciones entre variables. En el proyecto, esta subred entendió el “contexto” de los puntos turísticos, complementando lo que las imágenes no podían explicar por sí solas.*

🔹 3. ***Multimodal Fusion Layer***

*El verdadero poder vino de la capa multimodal, donde combinamos la visión (CNN) y el contexto (tabular network). Esta fusión permitió que el modelo aprendiera de ambas fuentes al mismo tiempo, imitando un poco cómo nosotros tomamos decisiones: no solo vemos una foto de un lugar, también consideramos su descripción, categoría o popularidad. Es aquí donde el Deep Learning muestra su versatilidad: integrar distintos tipos de datos en una sola predicción robusta.*


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

## 🧪 *Flujo de trabajo*

1. ***Exploración y limpieza del dataset***
2. ***Feature Engineering** sobre variables como tags, ubicación, popularidad*
3. ***Preprocesamiento de imágenes** con `torchvision.transforms`*
4. ***Clustering geográfico** con KMeans*
5. ***Normalización** y división del dataset (70% train, 15% val, 15% test)*
6. ***Construcción del Dataset personalizado***
7. ***Entrenamiento de modelo multimodal***
8. ***Evaluación con métricas de clasificación***


---

- ***¡Tu feedback es bienvenido! Si tienes ideas, mejoras o sugerencias, no dudes en abrir una issue o pull request.***

---

### ⚠️ *Disclaimer*

*El dataset utilizado en este proyecto pertenece a la plataforma Argonuts. Este trabajo no tiene fines comerciales y contiene errores y aproximaciones con fines ilustrativos.*
