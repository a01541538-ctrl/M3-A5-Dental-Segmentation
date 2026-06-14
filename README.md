# M3-A5-Dental-Segmentation
Este proyecto implementa un modelo de segmentación semántica basado en U-Net para identificar estructuras dentales en radiografías panorámicas.

El sistema utiliza imágenes anotadas en formato COCO, las convierte en máscaras binarias y entrena una red neuronal convolucional para generar segmentaciones automáticas de las regiones dentales.

Dataset

Panoramic Dental X-Ray Dataset

Las anotaciones se encuentran en formato COCO y fueron transformadas a máscaras binarias para el entrenamiento supervisado.

Metodología

Flujo general del sistema:

Radiografía panorámica

↓

Conversión de anotaciones COCO a máscaras binarias

↓

Normalización de intensidades

↓

Redimensionamiento a 512 × 1024 píxeles

↓

Arquitectura U-Net

↓

Predicción de máscara binaria

↓

Evaluación mediante Dice e IoU

Arquitectura

Se utilizó una arquitectura U-Net compuesta por:

Encoder basado en capas convolucionales
Max Pooling para reducción espacial
Bottleneck para extracción profunda de características
Decoder con UpSampling
Conexiones de salto (skip connections)
Capa de salida con activación sigmoide

Resultados

Resultados obtenidos sobre el conjunto de prueba:

Métrica	  Valor
Dice	    0.849
IoU	      0.737
Loss	    0.151

Estructura del repositorio
M3-A5-Dental-Segmentation/
│
├── M3_A5_Dental_Segmentation.ipynb
├── requirements.txt
│
├── report/
│   └── M3_A5_Mini_Project.pdf
│
├── figures/
│   ├── curvas_entrenamiento.png
│   ├── figura_segmentacion_unet.png
│   ├── unet_architecture.png
│   └── validacion_externa.png
│
└── models/

Trabajo futuro
Incrementar el tamaño del dataset.
Realizar validación multicéntrica.
Evaluar arquitecturas Attention U-Net y U-Net++.
Comparar el desempeño frente a modelos basados en Transformers.
Extender el sistema hacia clasificación automática de anomalías dentales.
Reducir el tiempo de inferencia para aplicaciones clínicas.
