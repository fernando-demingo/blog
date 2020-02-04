---
title: Instalación cocos2d-x v4.0
date: 2020-02-04 23:07:06
tags: cocos2d-x
---


### Instalación de ```cocos2d-x v4.0```
(https://docs.cocos2d-x.org/cocos2d-x/v3/en/installation/CMake-Guide.html)

---

### Pre-requisitos

1. Instalar ```python 2.7.10``` 

2. Instalar ```cmake 3.1+```
Si se ha instalado el GUI entonces hay que activar el CLI (command-line).

- ```Tools -> How to install command line```

3. Instalar ```Xcode``` o ```Visual Studio``` o ```Android Studio```

---

### Descargar última versión de ```cocos2d-x``` (v 4.0)


1. Descargarse fichero ```cocos2d-x.zip```

2. Descomprimir el fichero ```.zip``` donde quiera tener la instalación (en mi caso ```/Applications```)
3. Ejecutar ```python download-deps.py```
4. Ejecutar ```python setup.py```


---

### Crear un nuevo juego 

1.- Ejecutar el comando:

```sh 
cocos new -p juego.etsisi.upm.es -d ~/Documents -l cpp DemoJuego
```

para crear la estructura del juego, en mi caso en la carpeta ```~/Documents/DemoJuego```

---

### Generar el fichero del proyecto (parte 1/2)

- Para ```Mac Xcode```

```sh
mkdir mac-build
cd mac-build
cmake .. -GXcode
open Cocos2d-x.xcodeproj
```


- Para ```IOS Xcode```

```sh
mkdir ios-build
cd ios-build
cmake .. -GXcode -DCMAKE_TOOLCHAIN_FILE=../cmake/ios.toolchain.cmake
open Cocos2d-x.xcodeproj
```

--- 

### Generar el fichero del proyecto (parte 2/2)

- Para ```Linux```

```sh
mkdir linux-build
cd linux-build
cmake ..
make
```

- Para ```Windows```

```sh
mkdir win32-build
cd win32-build
cmake .. -G"Visual Studio 15 2017" -Tv141
```


---

# Ejecutar el ejemplo

 Abrir el fichero del proyecto creado y ejecutarlo.





