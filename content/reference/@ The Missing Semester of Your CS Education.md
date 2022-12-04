---
title: "The Missing Semester of Your CS Education"
date: "2022-12-04 08:46"
tags: 
  - 
draft: true
---
Muchas veces nos abemos de la existencia de herramientas ya existentes para hacer cosas de neustra vida cotidiana.

Esta clase busca mostrar algunas herramientas que pueden impactar tu dia a dia y tu vida en general.

## Shell
Interfaz basica en la cual podemos insertar comandos. Usualmente es ejecutar programas con argumentos. 

Los argumentos modifican el comportamiento del programa

Tambien usa un lenguaje de programacion. ifs, functions, loops, otros.
### date
Nos da la fecha al dia de hoy

### echo
Imprime en la consola el argumento que se le pasa

Como la consola sabe lo que los programas hacen?. Estos suelen venir con tu computadora y le permite 

## Environment Variables
Environment Variable. Es una variable que se refiere a la localizacion de programas, un valor especifico o cualquier otra cosa que nos gustaria guardar en una variable.

Usualmente, estas son utilizadas para guardar la localizacion de un programa como referencia para poder ser utilizado en el shell.

### Path
Una variable importante a tener en cuenta es $PATH. Esta variable nos muestra las diferentes localizaciones en las que se pueden encontrar los programas que pueden ser accedidos desde la consola. Para ello, el nombre del programa debe ser igual al comando que se esta insertando.

Es decir, que al ejecutar date o echo busca entre estas rutas un programa con ese nombre y de encontrarlo, lo ejecuta.

Un path muestra la localizacion real de un archivo a partir de la raiz inicial de un programa.

#### Absolute Paths
Paths que determinan la localizacion absoluta de un archivo a partir de un directorio raiz

#### Relative Paths
Paths que determinan la localizacion de un archivo relativo al directorio en el que te encuentras actualmente

## which \>argument\?
Es un comando que te permite saber el path absoluto de la ejecucion de un archivo.

## pwd
Imprime el path absoluto en el que te encuentras actualmente.

## cd
Te permite cambiar el directorio en el que te encuentras actualmente

Existen dos directorios especiales que sirven para facilitar la navegacion.

- . (dot). Este path ayuda a referirnos al directorio actual en el que nos encontramos
- .. (double dot). Este nos sirve para referirnos al directorio padre directo de donde nos encontramos actual mente
- ~ (tilda). Sirve para referirte al directorio home en tu usuario y maquina especificos
- - (dash). Sirve para volver al directorio previo en el que estabas. Puedes intercambiar entre dos directorios
- 

Como se nota esta es una forma de navegar de forma relativa al directorio en que te encuentras

## ls
Sirve para listar todfo lo que se encuentra en el directorio en el que estas actualmente

Adicionalmente tambien puede recibir un path ya sea relativo o absoluto y mostrar los archivos que se encuentran ahi

Un flag interesante que se puede utilizar con este comando y que es muy comun de ver es el \-l. 

### Leer informacion proveniente del flag -l
La primera columna indica el tipo de formato del que se trata una cosa. Si esta marcado con d se refiere a un directorio y cualquier otra cosa con un guion es un archivo.

Las siguientes columnas indican los permisos que se tienen sobre un archivo o directorio.

Las primeras tres columnas de este grupo indican los permisos que tiene sobre este particular archivo EL DUEÑO del mismo (quien lo creo o quien fue marcado como dueño).

Las siguientes tres columnas indican los permisos que tiene sobre ese elemento en particular EL GRUPO QUE ES DUEÑO del mismo.

Las ultimas tres son los permisos que tienen el resto de usuarios, es decir, quienes no son ni el dueño ni se encuentran en el grupo de dueños.

Cada una de las letras en estos grupos representa un permiso diferente, escencialmente son:
- r (Read).
- w (Write)-
- x (Execute)

En caso de tratarse de un archivo la r te permite leer su archivo la w te permite sobreescribir su contenido y la x te permite ejecutar el programa.

En caso de tratarse de un directorio la r te permite ver los archivos dentro de un directorio. La w te permite renombrar, crear y remover contenido del directorio. La x te permite entrar al directorio.

Estos permisos en particular funcionan de forma jerarquica, si yo quiero entrar a determinado directorio tengo que tener los permisos de x de todos sus padres y del directorio mismo
## Flags y Opciones
Usualmente todos los comandos tienen un flag --help que sirve para mostrar el uso de un comando en especifico. 

Para leerlos correctamente tenemos lo siguiente:
- \[\] (brackets). El argumento es opcional, puede o no estar incluidos
- ... (triple dot). Zero, uno o mas

### Flags
Una flag es identificada por constar no recibir ningun valor extra como argumento

Ejemplos de flags:
- \-b
- \-d
- \-h

###  Opciones
Cualquier cosa reciba un valor despues de escribirse como extra al comando es considerada una opcion

Ejemplos de opciones:
- \-\-color\[COLOR\]
- \-\-block-size=SIZE

## mv
Te permite mover o renombrar un archivo.

Recibe dos paths, la localizacion y la nueva localizacion.

```bash
mv dotfiles.md name.md # renombrar
mv dotfiles.md ../../dotfiles.md #mover
```

## cp
Te permite copiar un archivo

Recibe dos, la localizacion desde donde copiar a la nueva localizacion
```bash
cp dotfiles.md ../dotfiles.md
```

## rm
Te permite remover un archivo. Por defecto no es recursiva, por tanto, no podemos remover un directorio a menos que le demos el flag -r

```bash
rm dotfiles.md #borra el archivo
rm -r ../ #borra el directorio padre
```

## rmdir
Te permite remover un directorio PERO SOLO SI SE ENCUENTRA VACIO
```bash
rmdir ../ 
```

## mkdir
Te permite crear nuevos directorios, recibe el nombre del directorio o los multiples directorios separados por espacio
```bash
mkdir My Files #Crea dos directorios, My y Files
mkdir "My Files" #crea un directorio My Files
mkdir My\ Files #Crea un directorio My Files
```

## man
Es como un manual que te permite ver la documentacion de un comando

```bash
man ls #Devuelve la pagina del manual del comando ls
```

## Combinacion entre comandos
El shell nos da una nocion de streams. Cada programa tiene dos por defecto
- Entrada
- Salida

El stream de entrada mas comun para un programa es el teclado

El stream de salida mas comun para un programa es la consola

Sin embargo, hay formas de hacer que el stream de salida de un programa se conecte con el stream de entrada de un programa, es decir, nos da formas de redirigir la entrada y salida de cada programa.

Una forma facil de hacerlo es utilizando los brackets \< y \>.

```bash
echo Hello > hello.txt
```

El comando de arriba toma el stream de salida de echo y lo pasa al archivo hello.txt

Algo un poco mas complejo seria
```bash
cat < hello.txt > hello2.txt #hello
```

Estos angle brackets tambien nos sirven para apender a un stream ya activo
```bash
cat > hello.txt >> hello2.txt #hello \n hello
```

### Pipe
Sirve para estableccer una pipa de conexion entre el stream de salida de un programa y el stream de entrada de otro.

Es decir, *toma el stream de salida del programa de la izquierda y conectalo con el stream de entrada de la derecha*
## cat
Te permite ver los contenidos de un archivo

usuario root
es especial porque tiene acceso y permiso a todas las cosas del sistema. La mayoria del tiempo no seras root, seras un usuario normal. Si fueses un usuario root todo el tiempo podrias destruir tu SO.

## sudo
Te permite convertirte en superusuario por un momento para ejecutar un comando en particular

## root
El simbolo del # te permite ejecutar como un root
