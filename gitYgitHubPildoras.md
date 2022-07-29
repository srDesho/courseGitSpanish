# Curso de Git y GitHub con Píldoras Informáticas

## 1. Introducción

## 1.1 ¿Qué es Git?

Es un software de control de versiones creado por Linus Torvalds.

es un software libre.

## ¿Para qué sirve Git?

Facilitar el desarrollo y mantenimiento de aplicaciones tanto de forma individual como sobre todo al trabajar en equipo.

## ¿Cómo facilita el desarrollo y el mantenimiento de aplicaciones?

Guardando un registro de todos los cambios que sufran los archivos.

## Ramas

Git cuenta con ramas que es una funcionalidad que sirve para dividir un archivo y pueda repartirlo a 2 o mas programadores que trabajarán en él mismo, al final Git une inteligentemente todos los cambios que hicieron los programadores.

## Descarga e Instalación de Git

Buscamos "Descargar Git" en [Google](https://www.google.com/), y seguimos las instrucciones de descarga según a qué sistema operativo vamos a instalar.

Una vez descargadas ejecutamos, y sólo clickeamos siguiente, siguiente, siguiente.... hasta que termine de instalar.

## 2. Creando repositorio

## 2.1 Crear repositorio 

1ro debemos conocer éstos 3 primeros comandos para utilizar: git init, git add y git commit.

Así trabajan estos comandos: ![imagen](https://miro.medium.com/max/1372/0*AtDEJJwMtdcMMVrQ.png) 

## 2.2 Agregar archivos y directorios a repositorio

Desde la consola de Git, podemos abrirla directamente desde la carpeta donde tenemos ubicado nuestro proyecto que queremos hacer seguimiento con Git, dentro de la carpeta del proyecto hacemos clic derecho en cualquier parte y seleccionamos "git bash here", de esa manera abrimos la consola.

Aquí escribiremos los comandos.

    git init : para poner el proyecto en el "Directorio de trabajo (Working directory)" de Git.

    git status -s : para poder ver una los archivos del proyecto que ya están en Git.

    git add : para agregar todo el proyecto al área de ensayo (Staging area).

    y si no queremos agregar todo, podemos darle el o los nombre de los archivos que queremos agregar al staging area, de la siguiente manera:

    git add index.html

## 2.3 Respaldar archivos y directorios repositorio

para crear respaldos de los archivos que están en el staging area, lo hacemos con los siguiente comandos:

    git commit -m "Comienzo del proyecto" <- entre comillas va la descripción que queremos darle.

**Si es la primera vez que hacemos un respaldo, git nos pedirá nuestro datos para que pueda guardarlo.**

Nos mostrará un mensaje así: 

    $ git commit -m "Comienzo del proyecto"
    Author identity unknown

    *** Please tell me who you are.

    Run

    git config --global user.email "you@example.com"
    git config --global user.name "Your Name"

    to set your account's default identity.
    Omit --global to set the identity only in this repository.

    fatal: unable to auto-detect email address (got 'Maribel@DESKTOP-3I2V7LF.(none)')

No pide un correo electrónico y un nombre de usuario, lo escribimos de tal manera que nos está indicando.

    git config --global user.email "you@example.com"
    git config --global user.name "Your Name"

Luego de hacer ésto ya podremos hacer el respaldo, escribimos de nuevo el comando:

    git commit -m "Comienzo del proyecto"

**Nota**
Cuando ya tenemos un archivo respaldado, y hacemos una modificación en el mismo archivo, si nosotros escribimos el comando "git status -s" en git veremos que nos muestra ese archivo pero marcado con una letra en rojo, de la siguiente manera:

    $ git status -s
    M index.html <--- M se muestra en rojo en Git
    ?? css/
    ?? js/

eso significa que el archivo fue modificado y que si queremos respaldar(Enviarlo al repositorio) debemos agregarlo nuevamente al stanging area, con el comando git add:

    git add index.html

Luego de agregarlo nos mostrará la letra en color verde haciendo referencia que está habilitado para pode hacer otra imágen(respalo, captura, etc) del archivo modificado, lo haremos nuevamente con el comando git commit y con otra descripción:

    git commit -m "agregando título, primer parrafo":

### Cómo ver una lista de los respaldos que tenemos

    git log --oneline

    // Y nos muestra la lista con su respectivo código
    370c797 (HEAD -> master) agregando título, primer parrafo
    4d18d99 Comienzo del proyecto


### Para volver el archivo a un respaldo anterior que queremos, o sea restaurar un archivo

Escribimos el siguiente comando "git reset --hard" con el código de la imágen donde queremos restaurar.

    git reset --hard 4d18d99

## 3. Capítulo III Subiendo a GitHub

## 3.1 Algunos comandos más

### Agregar todos los archivos del proyecto al repositorio

    git add . 

### Agregar directamente al área de ensayo(stanging area) y al repositorio

    git commit -am "nombre que querramos"

### Abrir editor de texto en Git
    
    git commit --amend

### Modificar la descripción de un repositorio guardado.

Tenemos que ingresar al editor de texto en mi caso instalé el VSCode como editor de texto en git

    git commit --amend

luegos de escribir el comando nos abrirá un archivo en VSC y ahí cambiamos el título, guardamos, lo cerramos y listo automáticamente se verá en la terminal de comandos de Git.

## 3.2 Subir repositorio a GitHub

- Debemos crearnos una cuenta en la web GitHub
- Crear un repositorio en GitHub
- copiamos el comando que nos da gitHub:

    …or push an existing repository from the command line
    git remote add origin https://github.com/srDesho/cursoGit.git  <--copiamos éste a la consola de GIT local
    git branch -M main
    git push -u origin main

- Una vez copiado -> git remote add origin https://github.com/srDesho/cursoGit.git
lo pegamos en la consola de Git y presionamos enter.

- Luego si es la primera vez nos pedirá nuestro usuario y contraseña.
- Sino nos pide usuario y contraseña, escribimos el siguiente código :

    git push origin master

luego de escribirlo y presionar enter nos deberá salir.

## 4. Curso Git. Clonación y tags
## 4.1 Editar desde GitHub

## 4.2 Crear Tags

## 4.3 Clonación de repositorio en local
