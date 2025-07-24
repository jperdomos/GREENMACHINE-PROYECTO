# GreenMachine 🌿 - Universidad Nacional de Colombia Sede Manizales

##- Jholman Dasney Meza Pasinga
##- Juan Camilo Perdomo Soto
##- Campos Herney Tulcan Cuasapud

**GreenMachine** es una aplicación interactiva que permite identificar y clasificar plantas medicinales latinoamericanas mediante visión por computador. Utiliza modelos YOLOv8 en modo clasificación, exportados a TorchScript, y una interfaz gráfica desarrollada con Tkinter en Python.

## Características principales

- Clasificación en tiempo real usando la cámara web.
- Reconocimiento de múltiples especies como sábila, ruda, coca, valeriana, entre otras.
- Interfaz intuitiva con visualización en vivo e información curativa detallada.
- Inferencia local optimizada (sin necesidad de GPU).
- Basado en un modelo YOLOv8/YOLOv10 entrenado con datos etiquetados en Roboflow.

## Requisitos

Instala las dependencias con:

```bash
pip install -r requirements.txt
