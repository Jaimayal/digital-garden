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
Es un principio que dicta que una clase no debe conocer nada mas alla de lo que le compete con otra clase con la que colabora.

Es decir, solo deben de tener la minima cantidad de metodos de modo que puedan comunicarse y hablar entre ellos.

Imaginando que un Alumno interactua con un Profesor mediante su interfaz Profesor y no conoce sus otras interfaces de Padre, Hermano, Hijo que forman parte de el y con la que otros interactuan, el solo conoce la de Profesor.

Otro ejemplo con una Secretaria se veria asi:

![[files/SegregacionInterfaces.png]]

Es como agregar otro nivel de abstraccion para que un cliente de una clase solo conozca las operaciones minimas.

### Principio de Inversion de Dependencias
Surge como resultado de cumplir el principio Open/Closed y la Sustitucion de Barbara Liskov.

Dicta que, si se busca flexibilidad y extensibilidad ni los modulos de alto nivel ni los de bajo nivel deb eben de trabajar con interfaces intermedias para que se pueda extender a futuro y incremente la flexibilidad de mis colaboradores.

![[files/PrincipioInversionDeDependencias.png]]


### Inversion de Control
Es cuando. en vez de que llame a las funciones de una libreria, la libreria me llame a mi.

No me llames, ya te llamaremos.

El Template Pattern consigue la Inversion de Control debido a que el control se encuentra en la clase abstracta que cuenta con los metodos definidos en las clases concretas. Las clases concretas desconocen cuando su codigo sera llamado.

Otro ejemplo es la inyeccion de dependencias

### Inyeccion de Dependencias
En vez de elegir de forma clara dentro de la clase que colaborador tienes, este te llega como parametro a un constructor o un setter.

En vez de acoplarte como clase concreta, te acoplas unicamente con una clase abstracta y esperas a que te pasen una clase concreta desde fuera, unicamente apegandote a los metodos de la clase abstracta.

En vez de composicion, se basa en una asociacion.

### Principio de Sustitucion de Liskov
Es un principio que sirve para evaluar una Jerarquia de Clasificacion (herencia) y ver si es valido utilizarla en conjunto con sus colaboradores por un cliente.

Para que la Jerarquia sea dada como valida, un cliente deberia de poder utilizar una clase abstracta y cualquiera de sus derivadas, utilizar sus operaciones publicas y que todas ellas ejecuten su funcion.

Como sabemos que ejecuto su funcion correctamente?.
- Lo que **si esta permitido** esque la precondicion de las derivadas sea mas flexible que la precondicion de la base.
- Lo que **no esta permitido** esquie la postcondicion de la derivada sea mas flexible que la precondicion de la base

Si una clase derivada tontita se le ocurre violar las condiciones de arriba es mejor ni concebirla como funcional.

Es como el pinguino y el ave, no puede ser una jerarquia de clasificacion debido a que el pinguino limita las operaciones de ave porque no puede volar.

Como yo lo entiendo tambien indica que las jerarquias de herencia por limitacion y herencia por exclusion rompen este principio.

### Herencia vs Delegacion
Como sabemos, la herencia permite transmitir metodos y datos de una clase base a unas clases derivadas. Asi mismo, si es una clase abstracta permite tener implementaciones entre meditas y utilizar el Template Pattern.

Sin embargo, todo esto tambien es posible hacer mediante una Composicion utilizando el mecanismo de Delegacion.

Con el mecanismo de Delegacion, una clase todo puede utilizar el codigo de su parte para brindar un servicio, esta clase todo tiene un nivel de abstraccion debido a que los clientes que interactuan con el no saben ni la existencia de sus partes.

Mediante la delegacion tambien podemos aplicar el Template Pattern, teniendo en la clase parte una llamada al metodo de la clase Todo.

Esto forma un ciclo, debido a que la clase todo conoce a la parte y la parte al todo para llevar a cabo el Template Pattern.

La forma de romperlo es meter una interfaz, de modo que la Parte puede utilizar a cualquiera que implemente la interfaz con el metodo que se encuentra dentro del Template y no necesita conocer de forma directa a ningun Todo.

### Tecnica de Doble Despacho
Esta tecnica se utiliza cuando un objeto A tiene que responder de una u otra forma dependiendo del tipo de objeto que es B dentro de una Jerarquia Polimorfica.

La mala solucion a este problema seria darle la responsabilidad al objeto A de checar el tipo del objeto polimorfico con el operador 'instanceof' o similar.

La solucion correcta recaeria en dejar que la responsabilidad recayera en cada uno de los objetos B polimorficos, de modo que ellos le pidan a el Objeto A ejecutar el metodo con ellos, pasandose a si mismos como parametro

```Java
abstract class Person {  
    void greet() {  
        System.out.println("Hi!");  
    }  
  
    abstract void accept(Global global);  
  
    void receive(Global global) {  
        System.out.println("Yes i receive u");  
        this.accept(global);  
    }  
}  
  
class Men extends Person {  
    @Override  
    void accept(Global global) {  
        global.accept(this);  
    }  
}  
  
class Women extends Person {  
    @Override  
    void accept(Global global) {  
        global.accept(this);  
    }  
}  
  
class Global {  
    void greet(Person person) {  
        person.greet();  
        person.receive(this);  
    }  
  
    void accept(Men men) {  
        System.out.println("I accept a men");  
    }  
  
    void accept(Women women) {  
        System.out.println("I accept a women");  
    }  
}
```

Ahora para probarlo podriamos utilizar cualquier objeto polimorfico sin problemas

```Java
public class Main {  
    public static void main(String[] args) {  
        Global global = new Global();  
        Person men = new Men();  
          
        global.greet(men);  
    }  
}
```

Utilizar instanceof rompe el principio openclosed.

Ante cualquier mala herencia se debe de considerar la composicion.





















