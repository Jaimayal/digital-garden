---
title: "Modelo del Dominio"
date: "2022-09-20 09:00"
tags: 
  - softwaredev
draft: true
---
Es una representacion abstracta de lo que pasa en el mundo real, usualmente tambien es el primer modelo (dibujito, imagen, UML) y sirve para visualizar de forma clara como llega a haber colaboraciones entre los objetos de un problema.

Se relaciona estrechamente con los [Requisitos](notes/Requisitos.md) y existen muchas estrategias para obtenerlo.

### Estrategias de Clasificacion
- Descripcion Informal
- Analisis Clasico
- Analisis del Dominio
- Analisis del Comportamiento
	- Patron Experto en la Informacion
- Analisis de Casos de Uso

De las primeras tres se obtienen las clases y los datos (preferentemente) de palabras directas del experto y de la cuarta se obtiene un flujo de mensajes que se deben mandar las clases para satisfacer las operaciones que necesitan entre ellos y lograr el objetivo del software.
#### Descripcion Informal
Consiste en tomar los requisitos en un documento escrito (regularmente informal) del cual se substraen los sustantivos y los verbos. Una vez extraido se dice que *todo sustantivo puede ser una clase y que todo verbo puede ser un metodo*.

Problemas del enfoque: 
- **Ambiguedad del lenguaje natural**, debido a que solemos usar sinonimos, metaforas, etc. diferentes personas pueden interpretar cosas diferentes del mismo texto.
- **Cosificacion** del lenguaje (Todo verbo puede ser un sustantivo y viceversa). La accion *correr* no solo puede ser un metodo de una persona, cosificado puede ser un *corredor*. Y la clase *Deportista* puede ser transformada a *hacer deporte*.

Razones para entenderlo:
- Ayuda a identificar los nombres y acciones clave que **deben terminar dentro del codigo si o si**.
- Ayuda a **identificar el vocabulario comun entre desarrolladores y cliente** mediante el uso de las palabras que vienen del documento de requisitos.
#### Analisis Clasico
Se formalizan las principales fuentes principales de clases y objetos:
- Tangibles 
- Intangibles

Y tienen dos fuentes principales estos pueden venir tanto del problema como de la solucion. Por tanto, algunas cosas puede que no sean contempladas. Teniendo en mente todo el tiempo la **cosificacion**.
#### Analisis del Dominio
Se busca traer todos los objetos, acciones y relaciones **directamente de la boca de un experto del dominio**, que sea el el que diga las cosas que hay en el sistema.

Caracteristica de un Experto:
- No suele desarrollar Software
- Debe estar fuertemente implicado con el problema, como un usuario final.
- Conoce el vocabulario que se utiliza en el entorno
#### Analisis del Comportamiento
Un comportamiento surge de la cantidad de operaciones que ofrece una parte del sistema con el conocimiento que tiene dentro de si (los datos).

Cualquier parte del Software tiene un comportamiento. Un paquete, un subsistema, una clase, una funcion. 

Por tanto, debemos prestar suma atencion al modelo del dominio, debido a que este es el que genera no solo clases si no operaciones que ocurren dentro del sistema para lograr su objetivo.

*Un objeto es conformado por conocimiento y operaciones que puede realizar. Su responsabilidad recae en la cantidad de contratos que satisface mediante sus operaciones*

Lo anterior no solo se aplica a un objeto, un paquete tambien tiene un conocimiento y una serie de operaciones que debe cumplir. Tambien un subsistema, tiene un conocimiento y una serie de operaciones a cumplir. Eso es el comportamiento, es mas abstracto y se aplica a distintas partes del sistema

##### Patron Experto en la Informacion
Es una variacion y replanteamiento de las ideas definidas ya en el Analisis del Comportamiento. En este caso, se dice que un Objeto cuenta con dos responsabilidades principales.
- Responsabilidad de Conocer. Conocer solo los datos que le interesan
- Responsabilidad de Hacer. Se dice que un objeto tiene obligaciones que son dadas por los datos que guarda. Sus obligaciones es ofrecer una interfaz publica que satisfasca las operaciones necesarias que otros objetos tienen que hacer con ese dato.

Reafirma que se tiene que respetar el [Principio General de Asignacion de Responsabilidades](notes/Principio%20General%20de%20Asignacion%20de%20Responsabilidades.md)

#### Analisis de Casos de Uso
