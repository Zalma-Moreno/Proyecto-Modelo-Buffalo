# Optimización y Evaluación de Modelos de Reconocimiento Facial

## 📌 Descripción del Proyecto

Este repositorio contiene el código fuente, los notebooks de exploración y los scripts de validación desarrollados como parte del **Trabajo de Fin de Máster**. El proyecto se centra en el análisis exhaustivo, la optimización y la evaluación de modelos de reconocimiento facial de última generación (basados en arquitecturas como InsightFace). 

El objetivo principal es analizar la robustez y eficiencia de estos sistemas para determinar su viabilidad en diferentes escenarios de hardware. Para ello, se realizan pruebas rigurosas aplicando múltiples estrategias de partición de datos y validación cruzada, además de explorar técnicas avanzadas de compresión de modelos (como cuantización y *pruning*) orientadas a entornos con recursos limitados, como dispositivos móviles y arquitecturas de *Edge Computing*.

## 📂 Estructura del Repositorio

El repositorio está organizado principalmente en los siguientes Jupyter Notebooks, cada uno enfocado en una fase específica del análisis:

* **`Aplicando_70_30,_80_20,_90_10_y_KFOLD.ipynb`**: Notebook dedicado a la validación de la robustez algorítmica. Implementa diferentes configuraciones de división del dataset para entrenamiento y prueba (70/30, 80/20, 90/10) y técnicas de validación cruzada (K-Fold) para garantizar que las métricas de los modelos sean consistentes y no sufran de sobreajuste.
* **`Proyecto_Modelo_buffalo_l.ipynb`**: Análisis y evaluación del modelo de alta precisión `buffalo_l`. Incluye pruebas de rendimiento, cálculo de métricas de precisión y recomendaciones de implementación (ej. ONNX FP16) para servidores de bajo costo y aplicaciones que requieren latencia crítica en tiempo real.
* **`ProyectoModelo_Buffal_s.ipynb`**: Optimización del modelo ligero `buffalo_s`. Se exploran técnicas de compresión profunda, combinando TFLite/ONNX FP16 con porcentajes de *Pruning* (30% - 50%). El enfoque es maximizar los cuadros por segundo (FPS) y reducir significativamente el peso del modelo (hasta ~3.2 MB) para despliegues en hardware restringido como Raspberry Pi o *smartphones*.

## 🛠️ Tecnologías y Librerías Utilizadas

El proyecto está desarrollado en **Python** y se apoya en el siguiente ecosistema de herramientas de analítica y visión artificial:

* **Visión y Deep Learning**: `insightface`, `opencv-python`, `torch`, `torchvision`, `mtcnn`.
* **Optimización e Inferencia**: `onnx`, `onnxruntime`, `onnxconverter-common`, `tensorflow`, `tf2onnx`.
* **Análisis de Datos y Machine Learning**: `pandas`, `numpy`, `scikit-learn`, `matplotlib`.

## 📊 Resultados Destacados

El proyecto documenta cómo diferentes técnicas de optimización impactan el rendimiento según el entorno objetivo. Algunas de las configuraciones logradas incluyen:

| Entorno Objetivo | Modelo / Técnica | Tamaño Estimado | FPS Estimado |
| :--- | :--- | :--- | :--- |
| **Edge Computing (Raspberry Pi)** | `buffalo_s` (ONNX FP16 + 50% Pruning) | ~3.2 MB | ~24.4 |
| **Dispositivos Móviles** | `buffalo_s` (TFLite FP16 + 30% Pruning) | ~4.5 MB | ~22.5 |
| **Servidores / Tiempo Real** | `buffalo_l` (ONNX FP16 + GPU) | ~6.5 MB | 15 - 20 |

> *Nota: Para ver el desglose completo de la justificación técnica y las métricas detalladas, consulta los DataFrames exportados dentro de los notebooks.*

## 🚀 Instalación y Uso

1. Clona este repositorio:
   ```bash
   git clone [[https://github.com/tu-usuario/tu-repositorio.git](https://github.com/tu-usuario/tu-repositorio.git)](https://github.com/Zalma-Moreno/Proyecto-Modelo-Buffalo.git)
