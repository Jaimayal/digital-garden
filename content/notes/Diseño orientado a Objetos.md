---
title: "Diseño orientado a Objetos"
date: "2022-09-20 08:44"
tags: 
  - ooad
  - oop
draft: true
---
Nivel siguiente al [Diseño Modular](notes/Dise%C3%B1o%20Modular.md), ahora ya no solo son piezas bien inspiradas, legibles, poco acopladas y cohesivas, si no que se aprovechan los mecanismos de Polimorfismo y Herencia + Composicion para hacer jerarquias altamente reusables y flexibles respetando principios de la programacion orientada a objetos.

Contempla:
- Principio Open/Closed
- Principio de Sustitucion de Liskov
- Principio de Separacion de Interfaces
- Principio de Inversion de Dependencias

La herencia tiene la misma reusabilidad que una composicion.

La herencia te acopla fuertemente a la interfaz de tu padre y a sus atributos. Solo se pueden agregar atributos y metodos y redefinir metodos, nada mas.

El polimorfismo es una relajacion del sistema de tipos que nos permite interactuar con una clase y con todos sus derivados no abstractos apegandonos de forma fiel a su interfaz publica.

## Teoria de Lenguajes
Enlace estatico, tiempo de compilacion. toda aquella caracteristica que se pueda resolver mirando el codigo, viendolo. Aqui entran las checked exceptions.

Enlace dinamico, tiempo de ejecucion. lo contrario, esta caracteristica no se puede saber quien es hasta que se esta ejecutando la sentencia. Aqui entra el polimorfismo. Aqui entran las unchecked exceptions

Expresion combinacion de operadores y operandos que se evaluan devolviendo un unico valor.

Sin polimorfismo es un enlace estatico puesto que en todo momento sabemos el tipo del valor de retorno. Lo unico que podemos utilizar es sobrecarga.

Con polimorfismo tenemos un enlace dinamico puesto qu eno sabemos el tipo de valor real del retorno hasta que se ejecuta. Cada uno tendra comportamientos diferentes ya sea el original implantado o el de cualquiera de sus descendientes.

### Operaciones Polimorficas
Lo anterior mismo puede mandar con comunicacion entre clases con mensajes. Mientras una expresion me prometa que me devuelve A yo no se si me va a devolver A realmente o alguno de sus subclases.

- Prohibido el instanceof
- Prohibido atributos publicos
- Prohibidas las variables globales

DEBIDO A QUE ESTO NOS ACOPLA A LAS PARTICULARIDADES DETRAS DE UNA JERARQUIA POLIMORFICA.
 
## Principio Open/Closed
Es el Objetivo del Diseño Orientado a Objetos.

Todas las partes del paradigma orientaod a objetos deberian estar **abiertas a la extension, cerradas a la modificacion.**

Es decir, debemos lograr tal diseño que no tengamos que modificar nada para arreglar algo, unicamente para extender su funcionalidad.

Esto se hace teniendo dos partes
1. Una clase fija, que sirve como base y que es polimorfica
2. Multiples implementaciones dinamicas que pueden colgar de una referencia a una clase fija polimorfica

Por tanto, la clase fija SIEMPRE sera abstracta y el infinito numero de posibilidades extensibles son las clases concretas dinamicas.

El controlador se encarga del dialogo entre el actor y el sistema. Existe uno por cada caso de uso.

## Reusabilidad
Presente en la Herencia, Composicion y Parametrizacion. La reusabilidad esta permitida y puede ser aprovechada mediante estos tres mecanismos

### Herencia vs Parametrizacion
La parametrizacion es la programacion generica, en general se usa cuando se busca tener exactamente las mismas operaciones en una clase pero hablando de diferentes cosas. 

Por ejemplo una ColaDePersonas tiene las mismas operaciones que una ColaDeHormigas. Si quisieramos usar Jerarquia aqui tendriamos que hacer que la clase base utilizara Object, y todos los objetos que entraran serian objects y cuando necesitaramos obtener uno se tendria que hacer downcast preguntando el tipo y es un caos.

Por otro lado, con la programacion parametrizada no tenemos esa necesidad, podemos tener una pila de T, cualquier objeto y las operaciones ya sabrian por si mismas de que tipo de objeto se esta tratando.

La diferencia entre usar genericos y Object es que con genericos te ahorras todos los cast y poder guardar cosas que no se podrian.

Esta es un aspecto en que la herencia no sirve para hacer reusabilidad

### Herencia vs Composicion
En la Composicion la reusabilidad es programatica, debido a que debo enviar mensajes a mis colaboradores y relegar las operaciones para que ellos la satisfascan. En este caso, la clase que mantiene las partes (el todo) tiene la capacidad de decidir que operaciones estan disponibles y cuale sno.
- Enlace Dinamico
- No existe acoplamiento alguno con la clase parte, solo le delego responsabilidades

En la Herencia la reusabilidad es automatica, debido a que teniendo operaciones en la clase padre no necesito redefinir los metodos. El lenguaje lo hace por ti. Caso contrario a la Composicion, la herencia no tiene forma de ocultar metodos heredados por el padre, los tiene que ofrecer si o si.
- Enlace estatico
- Acoplamiento a los atributos de la clase base por modificador 'protected'.

La herencia con polimorfismo es el mecanismo mas fuerte para utilizar en las partes del proyecto que son mas propensas a ser extendidas

### Ley Flexible y Estricta de Demeter
#### Ley Estricta de Demeter
- Ni se te ocurra hablar con los atributos de la clase base, esto para evitar acoplamiento a la clase base.
- Si es la parte critica de la aplicacion, la que mas tiende a los cambios, esta es la indicada
#### Ley flexible de Demeter
- Si se te permite hablar con los atributos de la clase base. Si es una herencia pequeña esta es la indicada

### Patron Metodo Plantilla
Template Method. Es utilizado en una Jerarquia de herencia.

Se utiliza cuando dos clases derivadas tienen partes similares dentro del algoritmo de un metodo cambiando solo una pequeña parte debido a los detalles de su especializacion.

Lo que se hace es mover el codigo comun de ese metodo a la clase padre y definir un metodo abstracto para que los detalles que cambian sean redefinidos por las clases hijas.

## Flexibilidad
### Clases Abstractas e Interfaces
La interfaz es un contrato que existe entre una clase derivada y la interfaz, declara que, toda clase que la implemente como minimo debe implementar de forma concreta un algoritmo para los metodos si no quiere ser abstracta.

Una interfaz es una clase abstracta pura la cual no fomenta la reusabilidad porque no tiene atributos ni metodos que debe transmitir, solo cabeceras de metodos (es decir, solo la interfaz).

Por otro lado, las interfaces aportan mucha flexibilidad con respecto al cambio, porque, mientras que una clase concreta implemente esos metodos a nadie le interesa que tecnologias utiliza o como lo este haciendo.

### Principio Separacion de Interfaces












