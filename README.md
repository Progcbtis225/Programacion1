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




Para clonar el repo te recomendamos crear una nueva carpeta,  (asegurate de no utilizar la misma que el prep curse). Una vez clonado entrá a esa carpeta y ejecutá los siguientes comandos:

    npm install
    npm test

>Si ves los tests fallando, estás listo para comenzar, si no lee bien el output para identificar el error.


### 2. RESOLVER EL CHALLENGE

Tu tarea es completar el código en los archivos  
 - `01.js` 
 - `02.js` 
 - `03.js` 
 - `04.js` 
 - `05.js` 
 - `06-07-08.js` 
 - `09.js` 
 
 De tal forma que pasen la mayoría de los tests.


### 3. ENTREGAR TU CHECKPOINT

Correr por ultima vez los tests y verificar cuantos pasan. Ten en cuenta que si te aparece "1 failed;1 total" es porque tienes un error de sintaxis: seguramente falta o sobra una llave, paréntesis, punto y coma, etc.
Saca un print de pantalla de tus tests.
Luego, debes subir un commit a tu repo. Para hacerlo, debes ejecutar el siguiente comando:

    git add .
    git commit -m 'checkpoint commit'
    git push origin main

Una vez finalizado, chequea:
1. Que veas los cambios reflejados en el repo de la cuenta de `checkpoints-soyhenry` (entrando al link brindado anteriormente.)
2.  Que no haya un require - solo debe haber codigo dentro de las funciones de cada ejercicio 


<img src="https://a.slack-edge.com/production-standard-emoji-assets/13.0/google-medium/26a0-fe0f@2x.png" style="float:left; width:35px; padding: 10px;" /> Atención: no debes realizar un commit después de la hora de entrega porque se anulara la totalidad del examen. 
>Revisar la hora del entrega del examen en los emails que te llegaron. 

### ¿TENES ALGUN PROBLEMA / CONSULTA?

1. Busca la solución en la "guía de errores comunes".

2. Si no la encuentras, revisa el canal de #henry_challenge en Slack. Probablemente a algún compañero le paso algo similar y ya lo consulto.

3. Si no encuentras la respuesta, puedes publicar un mensaje en dicho canal.

> No se puede hacer consultas sobre la resolucion de los ejercicios.


### GUIA DE ERRORES COMUNES

Para identificar el error, vas a tener que leerlo en la consola.


* "jest" no se reconoce como un comando externo o interno...:
    1. Borrar la carpeta `node_modules` y el archivo `package-lock.json` e instalar nuevamente ( `npm install` ).
    2. Si esto no funciona, instalar test con el comando `npm install jest`.


* 1 failed, 1 total:
    1. Tenes un error de sintaxis. Revisa el último ejercicio que hayas hecho, seguramente falta o sobra una llave, paréntesis, punto y coma, etc.

* Author identity unknown.  
    1. Intenta ejecutar los siguientes comandos para configurar tu cuenta:
        * git config --global user.name "Tu usuario de GitHub aca"
        * git config --global user.email "Tu email aca"

    2. Ingresa a [Github](https://docs.github.com/es/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) y sigue las instrucciones para configurar tu token. 

* La consola se tilda en `Runs`:
    1. Revisa tu código, tenes un bucle infinito. Tenes que checkear la condición de corte de tus bucles.
