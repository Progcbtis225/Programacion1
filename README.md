# PROGRAMACIÓN 1
Curso de Programación 1 CBTIS225


### Bienvenido al curso inicial de programación en lenguaje C.

<p style="color:#f92850; font-size: 16px; text-align:center;">¡ Por favor lee TODO este material con atención !</p>

## PRIMEROS PASOS

Configuremos nuestro entorno de trabajo.

Tenemos dos opciones, trabajar en linea o instalar un IDE(entorno de desarrollo integrado) en tu computadora.

Hay cosas puntuales que tal vez no se encuentren específicamente en este material, vas a tener que investigar un poquito por tu cuenta (Google es tu mejor amigo 🤗).



## TRABAJAR NUESTROS PROGRAMAS EN LINEA:

### 1. Online Compiler

Deberás ingresar a cualquier IDE en línea, yo te propongo el siguiente 
`https://www.onlinegdb.com/online_c_compiler`

Abrir en un nueva ventana de tu navegador el siguiente link https://www.onlinegdb.com/online_c_compiler

<p align="center">
  <img height="200" src="../../blob/main/img/01.PNG" />
  <img height="200" src="../../blob/main/img/02.PNG" />
</p>



## INSTALAR UN IDE DE DESARROLLO:

### 2. Visual Studio Code
Tienes que instalar el VS como entorno de desarrollo, este lo puedes descargar del siguiente link `https://code.visualstudio.com/download`
abrelo en una nueva ventana https://code.visualstudio.com/download

>Es importante que selecciones tu sistema operativo,para iniciar la descarga.

<p align="center">
  <img height="400" src="../../blob/main/img/03.PNG" />
</p>

### 3. Extención C/C++
Estando dentro de Visual Studio debes configurar la extención `C/C++ Extension Pack`
solo debes buscarla y darle click en instalar

<p align="center">
  <img height="400" src="../../blob/main/img/04.PNG" />
</p>


### 4. Compilador MinGW-w64
Debes instalar el compilador de C que lo puedes descargar del siguiente link `https://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win64/Personal%20Builds/mingw-builds/8.1.0/threads-posix/sjlj/x86_64-8.1.0-release-posix-sjlj-rt_v6-rev0.7z/download`

abrelo en una nueva ventana y espera la descarga https://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win64/Personal%20Builds/mingw-builds/8.1.0/threads-posix/sjlj/x86_64-8.1.0-release-posix-sjlj-rt_v6-rev0.7z/download

<p align="center">
  <img height="400" src="../../blob/main/img/05.PNG" />
</p>


  Lleva el archivo descargado a la unidad "C:\" de tu computadora.
  Extrae la carpeta en este directorio.
  Entra en la siguiente ruta y copiala "C:\mingw64\bin"

<p align="center">
  <img height="400" src="../../blob/main/img/06.PNG" />
</p>


    Lleva el archivo descargado a la unidad "C:\" de tu computadora.
    Extrae la carpeta en este directorio.
    Entra en la siguiente ruta y copiala "C:\mingw64\bin"
    

<p align="center">
  <img height="400" src="../../blob/main/img/07.PNG" />
</p>

    En el menú de Windows buscamos la opción variables de entorno.
    Seleccionamos la opción de Variables de entorno.
    En las variables del sistema buscamos la variable Path
    Seleccionamos la opción editar.
    Presionamos en Nuevo y agregamos la ruta que copiamos anteriomente.

<p align="center">
  <img height="400" src="../../blob/main/img/08.PNG" />
  <img height="400" src="../../blob/main/img/09.PNG" />
  <img height="400" src="../../blob/main/img/10.PNG" />
  <img height="400" src="../../blob/main/img/11.PNG" />
</p>

Terminar el proceso aceptando las modificaciones en las ventanas abiertas.

Abrimos una ventana de consola de comandos y escribimos el siguiente comando "gcc --version"
si te aparece un mensaje como el de la imagen entonces ya está lista la instalación.

<p align="center">
  <img height="200" src="../../blob/main/img/12.PNG" />
</p>


## RESOLVER EJERCICIOS

Tu tarea es completar el código en los archivos  
 - `00.c` 
 - `01.c` 
 - `02.c` 
 




* La consola se tilda en `Runs`:
    1. Revisa tu código, tenes un bucle infinito. Tenes que checkear la condición de corte de tus bucles.
