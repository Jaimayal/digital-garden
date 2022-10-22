---
title: "Diseño Modular"
date: "2022-09-20 08:42"
tags: 
  - ooad
  - programming
draft: false
---
Es el nivel posterior al [Diseño en Codigo](notes/Dise%C3%B1o%20en%20Codigo.md), aparte de ser codigo bien inspirado del modelo del dominio que es altamente legible, se agrega que son modulos (o piezas) de codigo que tienen un tamaño homogeneo con alta cohesion y poco acoplamiento. 

Es decir, piezas que tienen un tamaño similar, en el cual cada una ejerce una sola y unica funcion que se acopla con muy pocas piezas porque no es un experto que tiene que realizar todo en la aplicacion.

Para hacerlo aprovecha e impulsa la abstraccion, encapsulacion, modularidad y jerarquia, busca finalmente crear modulos de alta calidad, es decir, que tengan alta [Mantenibilidad](Mantenibilidad.md)] (escalabilidad, calidad, reusabilidad, etc).

## Criterios
Esta disciplina del diseño recupera tres conceptos recurrentes.
- Cohesion (Maxima)
- Acoplamiento (Menor)
- Tamaño (Poco)

Una buena aplicacion de estos criterios resulta en clases altamente cohesivas y pocamente acopladas (acoplamiento eferente a clases inestables), con un bajo tamaño. Es decir, respetando al maximo el KISS.

- [[notes/Cohesion]]
- [[notes/Acoplamiento]]



## Tamaño
Sirven como una referencia a tener en cuenta para escribir codigo de calidad, no se deben seguir a rajatabla sin embargo establecen un punto de partida para permitir identificar codigo de calidad.

- Paquete - 12 a 20 clases
- Clase - 3 a 5 atributos
- Clase - 15 a 25 metodos
- Clase - 200 a 500 lineas
- Metodo - 1 a 3 parametros
- Metodo - 10 a 25 lineas
- Metodo - 2 a 3 sentencias anidadas
- Linea - 80 a 120 caracteres

**Son solo valores orientativos**.

## Modularidad
### Numero de Modulos
La cantidad de modulos por programa debe ser ajustada a la cantidad de codigo que tendra cada una.

Al realizar diseño modular existen dos costes principales.
- Costo por Implementacion. Lo que cuesta escribir cada clase (cantidad de lineas).
- Costo por Integracion. Lo que cuesta integrar todas las clases con un buen diseño.

### Distribucion de Responsabilidades
El problema debe ser dividido entre distintos modulos de modo que todos aporten algo a resolver el problema de forma relativamente equitativa

## Jerarquizacion
Existen dos formas de jerarquizar el diseño para resolver un problema
- Top Down
	1. Se desarrolla la clase principal
	2. Se escriben sus atributos privados 
	3. Se escribe su interfaz publica
	4. Se codifican las interfaces
	5. Se instancian objetos y se usan metodos conforme sean necesarios de otras clases.
	6. Se evalua que clase de las que faltan es la mas riesgosa de escribir
	7. Se vuelve al paso 2
- Me hago el diagrama de clases en el que hago el reparto de responsabilidades e inicio con el metodo top down
- Un diseño es un diagrama UML que puede servir para plantearse el codigo antes de escribirlo

## Interfaz - Parte Publica
Los smell codes contribuyen a tener un pesimo codigo.
- Homogenea. Nombrado, orden de parametros, valores de retorno
- Suficiente. Que no haya efectos secundarios, que solo sean acciones unicas.
- Minima. Que ofrezca la interfaz minima suficiente para satisfacer las necesidades basicas (primitivas) y nada mas.

**Una buena interfaz publica debe de ser minima, ofreciendo los metodos suficientes de forma homogenea para que otros lleven acabo sus operaciones**
### Codigo Sucio por Clases Alternativas con Interfaces Diferentes
Se debe homogeneizar el nombrado que se le da a las cosas de escencia similar dentro del codigo, tratar de mantener una terminologia homogenea en el como son nombrados los metodos publicos a traves de todas las clases es algo a lograr.

- Homogeneizar los nombres
- Utilizar herencia por extension o implementacion
- Mover responsabilidades

### Principios del Menor Compromiso
Una clase solo debe exponer en su interfaz publica los metodos suficientes como para que desarrolle su unico trabajo sin tener efectos secundarios o tener metodos que no van de acuerdo con el nombrado / los datos que tiene.

**Cada metodo tiene que ser un unico verbo, e implementa solo lo que dice**.

### Interfaz Suficiente, Completa y Primitiva
- Suficientes caracteristicas para satisfacer las funcionaldiades que debe proveer a otras clases
- Primitiva. Solo contener operaciones que son primitivas para esta clase y no requiere de muchas especificaciones.

## Diseño por contrato
Tres terminologias
- Error
- Defecto
- Fallo

Dos tipos de errores
- Errores Excepcionales
- Errores logicos

Dos mecanismos para lidiar con fallos
- Programacion Defensiva
- Aserciones

El diseño por contrato establece un contrato entre dos partes, el cliente y el servidor.
El cliente de un metodo es quien le esta llamando, el servidor es el que procesa la entrada y del que se espera obtener un resultado.

El diseño por contrato concibe que estas dos partes tengan un contrato formal en el que se establecen:
1. Las precondiciones que debe de cumplir un cliente para llamar una funcion
2. Las postcondiciones que debe de cumplir el servidor y retornarle al cliente

De esta forma, las dos partes del contrato pueden estar seguras que ambas cumpliran con su parte y pueden avanzar de forma segura.

Para implementarlo se suele utilizar los assert.

## Implementacion - Vista Privada
### Cohesion
- Cohesion de Metodos
- Principio de Unica Responsabilidad (S de SOLID)
- Responsabilidad fuera de Lugar. La responsabilidad no esta donde deberia de estar
	- Condigo Sucio por Envidia de Caracteristicas
	- Codigo Sucio por Clase de Datos
	- Codigo Sucio por Cambios Divergentes
- Sin clase para una Responsabilidad. Sin nadie puede asumir la responsabilidad
	- Codigo Sucio por Cirugia a Escopetazos
	- Codigo Sucio por Grupo de Datos
	- Codigo Sucio por Obsesion de Tipos Primitivos
- Clase sin Responsabilidad. Existe una clase pero no tiene nada por hacer
	- Codigo Sucio por Clases Perezosas

#### Cohesion de Metodos
- Las funciones deberian hacer una sola cosa.
- Violaciones
	- Las funciones realizan mas de una operacion
	- Las lineas persiguen objetivos distintos a lo que espeifica el metodo
	- Falta de Cohesion en el metodo
- Solucion
	- Dividir las distintas lineas de distinto tipo en diferentes funciones
	- Evitar el acoplamiento entre distintas funcionalidades de una clase
**Pedirle Cohesion a un metodo**

#### Principio de Unica Responsabilidad
Una clase cohesiva (como deberia de estar hecha) solo **deberia tener un unico motivo de cambio**, es decir, solo se deberia ver afectada por una unica cosa (persistencia, vista, comunicacion solo uno pero no todos a la ves).

**Pedirle cohesion a una clase**.

#### Codigo Sucio por Envidia de Caracteristicas
Una clase que envidia a otra clase pidiendole todo el rato sus caracteristicas para hacer los calculos en vez de que la clase que tiene los datos hacerlos.

Es decir, no se respeta el Patron Experto en la Informacion.

#### Codigo Sucio por Clase de Datos
El otro lado de la moneda, en este caso la clase que permite que le pidan todo y queno calcula nada es la clase de Datos.

#### Codigo Sucio por Cambios Divergentes
Ocurre cuando una clase puede ser afectada por multiples cambios, es decir, si se cambia una tecnologia se cambiara una parte, si se cambia la persistencia otra parte, si se cambia la vista otra parte. Eso esta mal, una clase solo deberia ser afectada por una sola cosa.

La solucion seria dividir esta en diferentes clases.

#### Codigo Sucio por Cirugia a Escopetazos
Es el lado contrario al anterior, en vez de que exista una clase que se encargue de una responsabilidad, esta responsabilidad esta distribuida a traves de multiples clases y si es cambiada tiene que cambiar en varios lugares a la ves.

#### Codigo Sucio por Grupo de Datos
Hay grupos de datos que son utilizados en muchos lados y que en realidad deberia estar como una clase y no como datos separados.

La solucion es crear una clase que ademas de ser reusable puede asumir responsabilidad y aliviar a otras clases.

#### Codigo Sucio Obsesion por Tipos Primitivos
Ocurre cuando en vez de utilizar una clase (donde es necesario porque se requieren operaciones) se utiliza un primitivo con el argumento de que una clase de un atributo no existe.

#### Codigo Sucio por Clases Perezosas
Una clase que tiene muy pocos datos y ni siquiera hace operaciones, es perezosa. Puede ser como un holder nada mas de datos que no hace nada.


### Acoplamiento
#### Codigo Sucio Inapropiada Intimidad (Evita los ciclos). - No te acoples en ciclos
Una relacion bidireccional complica el codigo y muchas veces crea ciclos muy complejos que hacen al codigo dificil de manejar
- Para quitar una relacion bidireccional se debe abstraer eso que tienen en comun las dos clases (se debe cosificar) en otra clase aparte. Entre Compra y Venta se deben conocer, para eviarlo se crea la clase CompraVenta,

#### Leyes de Demeter - No te acoples con quien no conoces
Son un conjunto de leyes obtenidas desde un proyecto. En el cual se dictamenta que UNICAMENTE SE PUEDE COLABORAR CON:
- this
- Parametros
- Atributos
- Objetos Locales

Por tanto, nunca se debe interactuar con un encadenamiento de mensajes obtenidas de enviar un mensaje a otro objeto. Es decir EVITAR EL ACOPLAMIENTO INDIRECTO A TODA COSTA.


#### Codigo Sucio por Libreria Incompleta - No te acoples a librerias
Crea una clase para englobar una libreria, no hagas que la libreria interaccione con todos y despues, cuando quieras cambiar la libreria, se tenga que hacer una cirugia a escopetazos.

ENCAPSULA LA LIBRERIA EN UNA SOLA CLASE. PATRON FACHADA.

La libreria da las primitivas (en su interfaz) y es nuestro deber encapsular para reducir el acoplamiento que tenemos a ella.

### Tamaño
#### Codigo Sucio por Listas de Parametros Largas
Es una variacion del smell code de Grupos de Datos, cuando, en vez de utilizar una clase cohesivas que encapsule operaciones y datos se utilizan un grupo de valores primitivos, lo que incrementa mucho la complejidad de los metodos o clases.

En base a las heuristicas lo maximo serian 2 -3 parametros por metodo.

Para tener cero parametros se necesitan de establecer buenas relaciones entre las clases. Muchas veces no hay necesidad de tenerlas

#### Codigo Sucio por Metodos Largos
Todos los metodos deben ser pequeños 10 a 15 lineas

#### Codigo Sucio por Clases Grandes
Siguiendo las metricas tambien deben ser pequeñas 200 a 500 lineas
## Patron de Indireccion
Los niveles de abstraccion ayudan a reducir el acoplamiento de la cantidad de elementos con los que se trabaja.

Para agregar un nivel de abstraccion en codigo basta con agregar una clase y posteriormente utilizar su interfaz publica para ejecutar las operaciones de los elementos que engloba. 

No necesariamente se puede agregar una, se pueden agregar varias e incrementar la Cohesion, dividir un problema y dividir responsabilidades.

**Todo se resuelve con mas clases, que reduzcan las responsabilidades y reduzcan el acoplamiento**

## Patron de Invencion Pura
Inventate todas las clases que te hagan falta, mientras mantengan un conjunto altamente cohesivo de operaciones aunque no representen a un objeto del modelo del dominio en particular. Todo esto mientras no hagas YAGNI, NO TE INVENTES PROBLEMAS, creala donde veas que hay mucha

## Patron de Vista Separada
Nunca hagas un modulo que interactue con el usuario, comunicacion o que sea cualquier interfaz para cualquier canal externo. SEPARA LAS COMUNICACIONES, LA PANTALLA Y TUS MODELOS.

Todas las clases con System.out y todo deben ir en otra clase. Para trabajar con ficheros otra clase, para trabajar con GUI otra clase.

**Una vista es todo aquello que recibe, lee y valida la informacion que proviene de un sitio externo al software**. 

## Patron Controlador
**Un controlador maneja el evento proveniente de una vista, se encarga de mantener la logica**


Por tanto en resumen, tenemos tres capas.
- Modelos
- Controladores
- Vistas

Las vistas son con lo que el usuario final interactua, este unicamente se encarga de recibir datos que pueden provenir desde multiples fuentes (una API, un archivo, un usuario u otro).

Los controladores son aquellos que se encargan de procesar un pedido SIN IMPORTAR EL MEDIO DEL QUE PROVENGA, debido a que las vistas ya prepararon todo para que llegue como me tiene que llegar por el contrato.

Los modelos se encargan de ejecutar y administrar las peticiones ya evaluadas, son los datos sensibles y no pueden estar siendo modificadas asi sin mas.

## Patron Creador
Debido a que, la solucion a los problemas de diseño (para lograr una buena cohesion con bajo acoplamiento y bajo tamaño) es agregar clases las cuales pueden venir del modelo o ser inventadas (Como las vistas y los controladres), el patron creador viene para resolver toda esa conglomeracion de creacion de objetos y clases que pueden hacer que un sistema se vuelva dificil de manejar.

- Factorias
- Builder

En el caso de una aplicacion de Spring.
- Lo comunmente llamado "Controller" (o donde recide toda la llegada de comunicacion mediante endpoints HTTP) es la Vista.
- Lo comunmente llamado "Service" (o donde recide toda la logica de negocio fuerte) es el controlador.

La capa Controller solo se encarga de recibir peticiones y remover todo lo relacionado con HTTP, al servicio nada mas le llegan los datos y el lo procesa, ni siquiera sabe que llegan por HTTP, bien podria ser cambiado por una app de Swing y no hay ningun problema.

- Vista, una por cada protocolo de comunicacion, interfaz o forma de recibir datos
- Controlador, uno por cada caso de uso que se necesitan
- Modelo, inspirados del modelo del dominio, datos duros

Inyeccion de Dependencias = Relacion por Asociacion

**TODOS LOS PROBLEMAS DE DISEÑO, DESACOPLAMIENTO, COHESION SE ARREGLAN AGREGANDO MAS CLASES.**