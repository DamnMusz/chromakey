# chromakey
A program that replaces green background from a video with an image. Developed in C++

# Instalación en Windows

El siguiente instructivo es una recopilación simplificada de los oficiales que se pueden encontrar en:
http://docs.opencv.org/3.0-last-rst/doc/tutorials/introduction/windows_install/windows_install.html
http://docs.opencv.org/3.0-last-rst/doc/tutorials/introduction/windows_visual_studio_Opencv/windows_visual_studio_Opencv.html#windows-visual-studio-how-to

## Pasos previos
Descargar la librería OpenCV (v3.2).
http://opencv.org/downloads.html

Descomprimir donde se desee dejar la librería. Por ejemplo C:\

Settear la variable de entorno del sistema:
OPENCV_DIR = C:\opencv\build\x64\vc14
OPENCV_BASE_DIR = C:\opencv\build

Agregar a la variable de entorno PATH la siguiente ruta, relativa a la anterior:
%OPENCV_DIR%\bin

## Visual Studio 2015
Crear un proyecto o clonar este de github.
Seleccionar el nombre del proyecto, ir al menú "Edit" -> "Property pages"

C/C++:
General: Additional Include Directories: Agreagar $(OPENCV_BASE_DIR)\includes

Linker:
General: Additional Library Directories: Agregar $(OPENCV_DIR)\lib
Input: Additional Dependencies: C:\opencv\build\x64\vc14\lib\opencv_world320.lib (o bueno, lo que sea equivalente)

(Si no reconoce las variables de entorno reemplazar con el path)

Para verificar, debería poder resolver un include como el siguiente:
#include <opencv2/opencv.hpp>
