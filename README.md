# GreenMachine - Universidad Nacional de Colombia Sede Manizales

## Autores
- Jholman Dasney Meza Pasinga  jmezap@unal.edu.co
- Juan Camilo Perdomo Soto  jperdomos@unal.edu.co
- Campos Herney Tulcan Cuasapud  ctulcan@unal.edu.co

---

GreenMachine es una aplicación de clasificación de plantas medicinales que integra visión por computador y aprendizaje profundo. El sistema fue diseñado para funcionar de forma local, utilizando modelos YOLOv8 entrenados en modo clasificación y exportados a formato TorchScript para inferencia eficiente en CPU.

La aplicación cuenta con una interfaz desarrollada en Python utilizando Tkinter, y permite la captura e inferencia de imágenes en tiempo real con una cámara conectada.

---

## Características principales

- Clasificación en tiempo real de plantas medicinales usando imágenes capturadas desde la cámara del sistema.
- Interfaz gráfica desarrollada con Tkinter, que incluye visualización de la imagen procesada, la clase predicha y el nivel de confianza.
- El modelo está entrenado con datos anotados mediante la plataforma Roboflow.
- Inferencia completamente local sin requerimientos de GPU o conexión a internet.
- Exportación del modelo a TorchScript (.pt) para integración embebida.

---

## Requisitos del sistema

Para ejecutar correctamente el proyecto se requiere Python 3.8 o superior y la instalación de las siguientes librerías:

- torch
- opencv-python
- numpy
- matplotlib
- Pillow
- tkinter (incluido por defecto en la mayoría de instalaciones de Python)

Instalación automática con:

```bash
pip install -r requirements.txt
```

---

## Estructura del proyecto

```
GREENMACHINE/
├── main.py                           # Script principal, ejecuta la interfaz
├── YoloViewer.py                    # Módulo con la lógica de inferencia y GUI
├── best.torchscript                 # Modelo YOLOv8 exportado en formato TorchScript
├── proyecto-greenmachine-pdi-jp-jm.ipynb  # Notebook con desarrollo y documentación
├── requirements.txt                 # Lista de dependencias
├── README.md                        # Archivo de documentación del proyecto
```

---

## Ejecución

Para ejecutar la aplicación, abra una terminal en el directorio raíz del proyecto y ejecute:

```bash
python main.py
```

Esto abrirá una interfaz gráfica desde la cual se podrá capturar imágenes en tiempo real y obtener la clase predicha junto al porcentaje de confianza.

---

## Detalles del modelo

El modelo utilizado es una red neuronal basada en YOLOv8 entrenada en modo clasificación. El entrenamiento se realizó sobre un conjunto de datos curado y anotado manualmente con especies medicinales y no medicinales latinoamericanas.

El modelo fue exportado a formato TorchScript con el fin de facilitar su uso en dispositivos de cómputo de bajo consumo, sin dependencias de Ultralytics o PyTorch Lightning.

Clases incluidas en el modelo (ejemplos):

- Aloe vera
- Manzanilla
- Valeriana
- Ruda
- Boldo
- Coca
- Plantas no medicinales

---

## Aplicaciones futuras

- Migración del modelo a TensorFlow Lite para despliegue en Android
- Integración con sensores ambientales y plataformas embebidas (Raspberry Pi, ESP32)
- Incorporación de una base de datos botánica y módulo de búsqueda
- Reconocimiento multimodal mediante fusión de imagen y texto

---

## Documentación adicional

El archivo `proyecto-greenmachine-pdi-jp-jm.ipynb` contiene:

- Descripción de la metodología empleada
- Detalles del dataset y proceso de entrenamiento
- Resultados de validación
- Justificación de arquitectura y formato de exportación

---

