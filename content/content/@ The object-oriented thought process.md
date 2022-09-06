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

### The Importance of Scope
Como sabemos en una clase podemos encontrar datos en forma de atributos o variables. Estos estan disponibles a distintos grados para su acceso:
- Metodo
- Objeto
- Clase

Multiples objetos pueden tener un metodo compartido (como un constructor).

Tambien cada objeto puede tener variables locales dentro de sus metodos, estas variables locales unicamente pueden ser vistas desde ese metodo en particular, por tanto, se dice que su Scope es de Metodo.
#### Object Attributes
Adicionalmente tambien es posible establecer atributos globales que son accesibles para todos los metodos, pero que su Scope se encuentra solo dentro del objeto actual. Es decir, si creamos multiples objetos cada uno tendra estos atributos que son accesibles desde todos los metodos.

#### Class Attributes
Finalmente tenemos una forma de crear datos globales que son accesibles para todos los objetos desde todos los metodos, esto se hace utilizando el keyword *static* al declarar tu atributo.

Es un poco peligroso utilizarlo por temas de sincronizacion, pero hay muchos casos donde es valido y necesario utilizarlos.
### Operator overloading
Es una practica bastante especial, no esta incluida en ningun otro lenguaje que no sea C++. Esta caracteristica permite sobreescribir lo que hace un operador (+ - / == !=, etc) para hacer lo que tu quieras que haga. Un ejemplo de esto lo vemos cuando se trabaja con Strings y se utiliza el operador + para concatenar. Eso es resultado del operator overloading.

### Multiple Inheritance
Es otro mecanismo de programacion bastante especial, unicamente incluido en C++. Esta caracteristica permite que una clase herede de multiples clases a la vez. Incrementa muchisimo la complejidad para el desarrolldor y para los compiladores, es por eso que Java, C# y Swift no la incluyen.

Encontramos dos tipos de herencia con exactitud *behavioral inheritance* y *implementation inheritance*. Los lenguajes como Java permiten *multiple behavioral inheritance* proveniente de la implementacion de multiples *interface*. Las *abstract class* son un ejemplo de *implementation inheritance*.

Behavioral Inheritance se refiere a que una clase especial no tiene implementacion de los metodos, unicamente representa comportamientos que seguramente seran implementados.

Implementation Inheritance representa lo opuesto, en este caso no solo se pueden dar metodos sin implementacion sino que muchos de ellos ya estan implementados.

### Object Operations
Las operaciones de copiado y comparacion con objetos son operaciones bastante complejas que toman de bastante computacion (dependiendo en cuantos niveles de referencias a objetos existen).

Hay dos tipos de copia posibles Deep Copy en la cual se hacen copias del elemento y de todos los elementos que referencia y Shallow Copy en la cual solo se hace una copia de la referencia principal.

De esta forma, hacer comparaciones debe ser implementado con tu propio mecanismo y no recaer con el que te da el mismo lenguaje, de esta forma, aseguras que tu comparacion se comporte como esperas.

## The Anatomy of a Class
Como sabemos una clase no debe estar creada sola, esta debe formar parte de una jerarquia o de interacciones mediante mensajes con otras clases.

A continuacion veremos descompuesta la estructura de una clase y sus partes. Muchos metodos se encuentran con implementacion volviendo a hacer enfasis en que la interfaz publica es lo que nos interesa extraer de los primeros diseños de las clases.

### The Name of The Class
El nombre de la clase debe ser descriptivo y claro para saber como sus objetos van a interactuar con todo el sistema, debido a que es la forma principal de referirse a ella debemos asegurarnos de usar nombres descriptivos.

### Comments
Como sabemos hay dos (tres a veces) tipos de comentarios. Estos comentarios en muchas ocasiones nos sirven para dar guia sobre lo que hace la clase o crear documentacion implantada en el lenguaje.

### Attributes
A continuacion encontramos los atributos que guardan los datos de nuestros objetos. Estos por lo regular se encuentran protegidos con el modificador de vista privada. Esto con el fin de cumplir con el principio de brindar la minima interfaz publica posible.

Recordemos que podemos tenerlos en dos scopes globales (por clase, static) y por instancia (por objeto).

### Constructors
Como sabemos podemos encontrar multiples constructores gracias al methodoverloading. Estos constructores tienen el mismo nombre de la clase y si uno es especificado el constructor default no sera creado.

Debemos evitar recaer en utilizar el constructor default.

Lo que se busca con los constructores es obtener una forma de inicializar todos los atributos de los objetos (Aunque sea a null), esto nos dara una forma estable a todos los objetos que sean creados a partir de el.

### Accessors
Son metodos especiales que sirven para obtener informacion de un objeto utilizando metodos. 

Estos metodos especiales no solo se utilizan para acceder a la informacion, sino que le brinda un control a cada objeto individual sobre las operaciones que pueden hacer con los datos que ofrece, quizas a veces solo deben ser accedidos o quizas solo deben ser escritos si se asignan valores vallidos. Todo este control te lo permiten hacer los metodos accesores.

### Public Interface Methods
Aparte de los accesores y constructores, existen otros metodos que son declarados como publicos y que nos sirven para hacer las operaciones pesadas de la clase. Regularmente estos son abstraidos con un nombre lo mas descriptivo posible mientras que la implementacion es la parte concreta donde se hace todo el trabajo

### Private Implementation Methods
Adicionalmente existen otros metodos que son declarados con el modificador de vista privada, y como se podra intuir, son utilizados dentro de la misma clase para hacer operaciones reducidas en pequeños metodos.

Un ejemplo seria la encripcion de datos, regularmente no queremos que esta sea vista desde otras clases, por tanto, al momento de recibir una contraseña, esta es encriptada por un metodo privado de la clase y nadie sabra siquiera que paso esa operacion.
___

