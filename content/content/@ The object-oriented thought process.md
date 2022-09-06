---
title: "The object-oriented thought process"
authors: "Matt Weisfeld"
year: 2019
URL: "www.amazon.com/Object-Oriented-Thought-Process-Developers-Library-dp-0135181968/dp/0135181968"
tags: programming oop
draft: true
---
## 🌱 Idea Principal

## 🌌 Impacto

## ✍ Mejores Frases

## 📔 Resumen + Notas
## Introduction to Object-Oriented Concepts
## How to Think in Terms of Objects
## More Object-Oriented Concepts
Los dos capitulos anteriores sentaron las bases con los conocimientos basicos relacionados a la programacion orientada a objetos. Sin embargo, si lo que se busca es analizar, diseñar y desarrollar un sistema orientado a objetos aun se necesitan ver unos conceptos mas como constructores, herencia multiple, scope, error handling, scope, etc.

### Constructors
Son metodos especiales que son llamados en el momento en el que se busca instanciar un nuevo objeto, sirven para inicializar los valores de los atributos de un objeto.

La sintaxis varia entre lenguajes, algunos utilizan *new*, otros *init*, etc. 

Para el contexto de Java un constructor es como un metodo que debe de llevar el mismo nombre de la clase actual y no debe tener valor de retorno.
#### When is a Constructor Called ?
El constructor es llamado de forma automatica tras instanciar (alocar memoria suficiente para) un objeto de una clase especifica, en Java se utiliza el keyword *new* seguido del nombre del metodo constructor.

#### What's Inside a Constructor ?
El constructor debe contener el codigo suficiente para que los atributos que va a guardar el nuevo objeto tenga un estado limpio y estable.

#### The Default Constructor
Hay un estandar respecto a la creacion de constructores, principalmente debido a que una clase necesita uno obligatoriamente para funcionar, los lenguajes de programacion proveen uno estendar en caso de que ninguno este disponible. Es importante no recaer mucho en este mecanismo y SIEMPRE implementar al menos uno.

En Java por ejemplo, debido a que todos los objetos heredan de la clase Object, podemos saber con exactitud que el constructor default llama al constructor de Object.

Es buena practica implementar AL MENOS un constructor por nosotros mismos para saber que la clase se va a comportar de forma esperada bajo cualquier cambio. 

#### Using Multiple Constructors
Es un proceso que debe ser ejecutado cuando lo que se busca esque distintos objetos de la misma clase sean inicializados o tengan valores diferentes al momento de creacion. 

Para realizar este mecanismo se aprovecha del **method overloading**, que funciona para sobrecargar metodos cambiando la signatura de ellos (tipo, nombre de parametros, cantidad, etc.)

#### Overloading Methods
Es un concepto de programacion en la cual se permite tener metodos multiples metodos de caracteristicas similares siempre y cuando se cambie su signatura.

La signatura de un metodo varia de lenguaje en lenguaje, para Java y C# la signatura consiste del nombre del metodo + sus parametros.

Otros lenguajes consideran al tipo de valor de retorno tambien como parte de la signatura.

Esto es muy utilizado en los constructores, se puede tener sobrecarga de constructores y por tanto, construir un objeto de una misma clase de distintas formas diferentes.

#### Using UML to Model Classes
UML es un lenguaje de modelado extremadamente fuerte, nos permite modelar en una clase los constructores unicamente removiendo el retorno que estos tienen.

#### How the Superclass is Constructoed
Si estamos utilizando herencia entre nuestras clases, hay que aclarar que el constructor de cualquier subclase esta obligado a llamar al constructor de superclase, en caso de que no lo especifiquemos el compilador lo hara automaticamente llamando al constructor default, pero como siempre, no es bueno recaer en estos comportamientos porque lleva a conducta aleatoria.

#### The Design of Constructors
Recordemos que los constructores deben de ser diseñados de tal forma que brinden objetos con un estado ==CONSISTENTE== y ==ESTABLE==, por tanto, queremos inicializar absolutamente todos los atributos a valores que tengan aunque sea un poco de sentido.

### Error Handling
El Error Handling es una practica muy comun, ocurre debido a que nadie puede diseñar un software perfecto completamente, por tanto, se toman medidas para lidiar con los posibles errores que puedan surgir durante la ejecucion de un programa.

Hay cuatro formas de lidiar con los errores que son muy comunmente utilizadas.
1. Ignorar. Dejar sin arreglar el problema, ignorarlo y dejar el resultado al azar.
2. Interrumpir la ejecucion. Se utiliza cuando se encuentra un problema y se interrumpe la ejecucion.
3. Tratar de arreglar. Usualmente se utiliza encontrando el problema y tratando de dar una solucion (redireccionamiento, alerta, etc).
4. Tirar una excepcion. Se utiliza dando una excepcion personalizada con todo el resultado de lo que fue mal en la ejecucion.

#### Ignoring the Problem
Probablemente el peor acercamiento para resolver un problema, ignorarlo te dara resultados indefinidos o incorrectos, te dara versiones inestables y muchos problemas de ejecucion ademas de crasheos y otros errores. Si un error es conocido ==JAMAS== deberia de pasar sin arreglarse.

#### Checking for Problems and Aborting the Application
Aqui lo que se hace es tirar una pantalla de error y terminar la ejecucion, aunque no es extremadamente descriptiva cumple su funcion, otorgando una version mas estable, cerrando recursos y conexiones en caso de un problema.

#### Checking for Problems and Attempting to Recover
Otra forma de solucionar un error es utiliza precisamente una forma de recuperacion una vez un error fue encontrado. Se utiliza en forma de validacion.

Muchas veces puede ser la solucion al costo de entregar a veces resultados inesperados o poco exactos, requiere de que predigas en donde ocurriran los problemas.

Muchas veces se pueden usar combinaciones de tecnicas basada en lo que se busque obtener de tu producto.

#### Throwing an Exception
Es el ultimo acercamiento y el mas apropiado en la mayoria de lenguajes.

En lenguajes con POO como Java, C#, Swift y otros tenemos las clausulas *try* y *catch* que sirven para manejar excepciones y dar puntos de entrada y salida para ellas.

En los bloques try colocamos el codigo que puede tirar una excepcion

Dentro de las clausulas del catch colocamos las excepciones que atrapara y dentro de su bloque de codigo el comportamiento que ejecutara en caso de encontrar una

Una combinacion de todos los metodos anteriores puede ser utilizada para satisfacer los requerimientos y hacerte inmune a tu interaccion con el usuario.
___

