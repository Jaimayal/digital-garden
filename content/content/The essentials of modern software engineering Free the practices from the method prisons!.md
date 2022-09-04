---
title: "The essentials of modern software engineering: Free the practices from the method prisons!"
authors: "Ivar Jacobson, Harold W. Lawson, Pan-Wei Ng, Paul E. McMahon, Michael Goedicke"
year: 2019
URL: 
tags: softwaredev
draft: false
date: "2022-09-03 08:42"
---
## 🌱 Idea Principal
Debido a que el Software se encuentra presente en todos los aspectos de nuestra vida, este libro da la fundacion principal para construir una metodologia agil, tambien llamada *escencia* para que puedas dirigir equipos desarrollando de forma efectiva..
## 🌟 Nota 2/5
## 🌠 Consideraciones
- Es un libro sobre METODOLOGIAS de desarrollo.
- Asume conocimientos de Programacion Estructurada y Programacion Orientada a Objetos.
- Los ejemplos se encuentran escritos en Java y JavaScript.
- Se necesita un minimo de nociones sobre UML.
- Se necesita un poco de conocimientos sobre otras metodologias agiles (como Disciplined Agile) para hacer un contraste.

## 🌌 Impacto
Me ayudo a entender el ciclo de aprendizaje por el que pasaron los autores, las practicas mas comunes en empresas reales hoy en dia y me ayudo a entender las partes que tenia que rellenar en mi conocimiento. Aprendi un poco mas sobre la historia de practicas de desarrollo.

A pesar de lo anterior, deje de leer el libro. Mis razones son las siguientes:
- Parece otra metodologia de desarrollo agil, sin embargo, la mayoria del material para entenderla y aplicarla se encuentra detras de un paywall, 
- No hay proyectos exitosos (o siquiera que hayan fracasado) que utilicen esta metodologia. 
- Se asemeja a RUP pero sin ser tan estricta e incorporando practicas populares agiles (como juegos).
- Crean terminologia como "kernel", "competencias" que peca de lo que critica, tener que aprender conceptos de nuevo, gastar recursos, etc.

Recomiendo los primeros dos capitulos para entender un poco sobre como se trabaja en el mundo real y el punto en el que estamos respecto a las metodologias de desarrollo

## ✍ Mejores Frases
Software engineering is the application of a systematic, disciplined, and quantifiable approach to the development, testing, deployment, operation, and maintenance of software systems.

## 📔 Resumen + Notas
### From Programming to Software Engineering
Este capitulo en particular busca definir de forma clara los conceptos de programador, desarrollador de software e ingeniero de software. Nos dara sus diferencias y semejanzas para poder distinguir y transicionar de una posicion a otra.

##### 1.1 Beginning with Programming
**Programacion** se considera como sinonimo de *implementacion* o *codificacion*, este proceso no incluye ningun tipo de debug, o pruebas, se limita a la escritura del codigo fuente de una aplicacion.

**Desarrollo de Software** es una actividad que integra la *toma de requisitos*, el *diseño*, la *implementacion* (programacion), las *pruebas* y el *deployment*.

**Ingenieria de Software** es unir conceptos de la disciplina de *ingenieria* con el *desarrollo de software*, de modo que se obtengan todas las ventajas de ella y se agreguen a un proceso ya establecido.

Para esta parte, en la jornada de Smith el ya ha aprendido todo lo basico de programacion, desde programacion estructurada hasta programacion orientada a objetos y un par de lenguajes (Java y JavaScript).

##### 1.2 Programming is Not Software Engineering
Hacking y Desarrollo profesional son dos cosas muy distintas y son dos acercamientos muy distintos que podemos tener a la programacion de un software.

**Desarrollo Profesional** es cuando escribes el codigo de forma que refleja tu analisis y pensamiento para resolver determinado problema, de esta manera, entiendes el codigo que acabas de escribir.

**Hacking** es cuando intentas codigo casi al azar hasta lograr alcanzar el objetivo que tienes sin siquiera saber como funciona.

El Desarrollo Profesional es una parte vital de la Ingenieria del Software, adicionalmente, esta ultima tiene muchas mas actividades relacionadas que no son solo escribir codigo.

Para esta parte, Smith ya ha trabajado en un proyecto con compañeros y se dio cuenta que programar solo forma una parte del ciclo, llego a la conclusion de que se tienen que tener unos requisitos, se llega a un consenso mediante lluvia de ideas, se desarrolla y finalmente se mantiene, algo todavia muy alejado de la realidad.
##### 1.3 From Internship to Industry
Usualmente, en un equipo de desarrollo podemos encontra dos tipos de personas:
- Aquellas que dictan y solicitan lo que el software debe hacer
- Aquellas que lo codifican, prueban y entregan

 La comunicacion entre Managers o personas con dominio sobre el problema del que se trata (primer grupo) hablan una jerga muy particular, usualmente, esta varia de empresa a empresa debido al dominio de la misma.

Como leccion, para ser un buen ingeniero de software, no solo debes conocer la forma de desarrollo de tu equipo sino tambien el dominio del problema de tu empresa.

Usualmente el trabajo en una empresa no se va a tratar de escribir codigo nuevo, si no de mantener y revisar el ya existente, ademas, para asegurarse de que no rompiste nada siempre hay que realizar testing a todos los cambios que hagas.

Mientras mas vas avanzando en los puestos de desarrollo, mayor es la cantidad de Sr (Seniority) que se te atribuye, conforme esta crece lo hacen proporcionalmente tus responsabilidades de liderazgo y comunicacion con los Stakeholders (Empresarios, jefes, CEOs, etc).

Una buena comunicacion con los Stakeholders se basa en llegar a terminos y practicas comunes de modo que permitan el flujo de trabajo de todos los miembros del equipo, basandose en unos buenos valores (en tiempo, forma y de alta calidad). Engloban cosas como revisiones, correccion de bugs, recibimiento de feedback y otras habilidades para alcanzar esas metas particulares que ambos tienen en mente.
##### 1.4 Journey into the Software Engineering Profession
La experiencia en la universidad solo son los fundamentos de desarrollo pero carece de los siguientes aspectos:
- No se realiza mantenimiento al codigo
- No se implementan nuevas caracteristicas
- No se escala para el uso de mas usuarios

Ignorando las grandes compañias de tecnologia como Facebook, Amazon, Twitter, Netflix, Shopify, etc. Una compañia promedio seguramente buscara tener un departamento de desarrollo para satisfacer una necesidad suya, de sus clientes o de sus usuarios finales.

Un joven estudiante seguramente estara mas interesado en conocer las tecnologias, las computadoras, las redes con las que se trabaja y no tanto con el dominio (negocio) de la empresa para la que va a trabajar, por tanto, no le interesaran las practicas de desarrollo, los valores u otras cosas relacionadas.

Los equipos del trabajo son la unidad minima con la que se construye un software, si es un software grande, usualmente distintos equipos trabajaran de forma sincronizada en distintas funcionalidades.

Para desarrollar un software primero necesitamos los requisitos, saber que es lo que se necesita hacer y revisar con los expertos para corregir cualquier mal funcion o recibir feedback respecto a las ya existentes.

Hay una disciplina de la ingenieria dedicada exclusivamente a los requisitos, su interpretacion, como se obtienen y como se piensa y razona sobre ellos, su nombre es *requierements engineering*.

Existe otra disciplina que conforma el **diseño** del software, se refiere a la calidad que se coloca en el codigo de modo que le permita ser mantenible, reusable, escalable, etc. 

Un diseño se puede estudiar de dos formas:
- Viendo las clases, modulos, funciones, unidades del codigo en cuestion.
- Utilizando una herramienta de diagramas que te permita modelar tu codigo.

*Me parecio interesante como hace mencion del diseño como la disciplina en la cual se le da forma al codigo para que sea de calidad / mantenible, es decir, que sea facil de escalar, de entender, de probar, de cambiar, es como lo que nos comentaba el profesor Luis en el curso de Recurrencia en el Desarrollo de Software. Lo que se busca finalmente es REDUCIR SU COMPLEJIDAD*.

No son las unicas tareas que debe hacer un ingeniero de software, usualmente se agregan dos que son las **pruebas** y el **despliegue**.

Se podria decir entonces que la Ingenieria del Software es una disciplina replicable y evolucionable, que busca convertir las necesidades de un cliente en requisitos claros, para que desarrolladores con las habilidades sociales como para comunicarse y escribir codigo de calidad (es decir, en modulos que tengan alta mantenibilidad) lo diseñen, lo desarrollen, lo prueben, reciban feedback, lo corrigan y repitan, hasta lograr el producto deseado por los clientes, en ese momento, ocurrira el despliegue.




### Resumen - From Programming to Software Engineering
Programar es muy diferente a desarrollar software, de hecho, la programacion es solo una actividad del desarrollo, un ciclo completo del desarrollo de Software se veria asi:
- Disciplina de Requisitos
- Disciplina de Analisis y Diseño
- Disciplina de Programacion
- Disciplina de Pruebas
- Disciplina de Despliegue

La Ingenieria del Software no es mas que la integracion de discplinas de la ingenieria al proceso del desarrollo de software, esto con el fin de que sea una actividad replicable, mejorable, organizada y facil de llevar.

Existe una diferencia muy clara entre **desarrollo profesional** y el **"hacking"**, la ultima se refiere a cuando se utiliza codigo de forma casi aleatoria sin saber lo que hace hasta lograr obtener el resultado esperado, la primera ocurre cuando analisas y escribes el codigo de forma clara, de modo que, cuando lo integres con el resto del codigo sepas que es lo que esta haciendo.

El conocimiento de la jerga que se encuentra en el dominio de la empresa para la que trabajas es fundamental para comunicarse de forma efectiva con los expertos.

Conforme se avanza en la industria del desarrollo del Software (Es decir, se incrementa el Seniority) las habilidades de comunicacion juegan un rol cada vez mas importante. Entre ellas podemos decir que resaltan el liderazgo de un equipo y la comunicacion con los Stakeholders (o expertos) para la toma de requisitos.

La toma de requisitos puede ocurrir de distintas formas, ya sea que se te pida copiar a otro software, que se te de un papel o una simple idea. De hecho es tan cambiante e interesante que hay una disciplina de la ingenieria dedicada a ello, *requierements engineering*.

Debido a que los requisitos se encuentran en constante cambio, el diseño del codigo del software debe de ser muy modular, con piezas que sean altamente mantenibles (faciles de entender, reusables, probables y cambiables).

Las pruebas toman un rol extremadamente importante, escribirlas garantiza que aunque tu te vayas de la empresa en un futuro tu unidad de trabajo pueda seguir siendo matenible sin problemas.

El despliegue usualmente no es llevado acabo por desarrolladores, sin embargo, puede serlo, este proceso es cuando se coloca el software en un servidor o en produccion para que los usuarios finales puedan hacer uso de el.

### Software Engineering Methods and Practices
Este capitulo busca introducir a la estandarizacion de las practicas y metodos utilizados en el desarrollo de software. Principalmente se abordaran tres temas:
- Problemas que enfrenta nuestra industria
- Metodologias de Desarrollo en los ultimos 40 años
- Motivaciones para la esencia

#### Software Engineering Challenges
Existen retos en la industria, principalmente los podemos ver en noticias de sucesos que ocurren respecto a fallos en el Software que se encuentra detras de cosas tan importantes como sistemas de seguridad o sistemas financieros.

Errores como estos pueden tratar ser prevenidos pero nunca nunca sera completamente cierto que dejaran de ocurrir o que podran ser evitados del todo.

#### The Rise of Software Engineering Methods and Practices
Esta claro que la "Crisis del Software" no solo ocurrio por mala programacion, principalmente porque como ya vimos, un desarrollo de software no solo ocurre con programar y ya, tiene sus requisitos, comunicacion, equipos, pruebas, etc.

A traves de la historia han surgido metodos de desarrollo que han servido para cumplir distintas necesidades. A las partes comunes entre un metodo y otro se le ha estandarizado como **practicas**, estas definen la esencia de las metodologias de desarrollo.

Estas practicas pueden ser de distintos tipos para el equipo (ambiente agradable, de facil codificacion, de facil colaboracion), para el cliente (buena toma de requisitos, conocimiento del dominio, conocimiento de la jerga) entre otras.

##### There Are Lifecycles
*Al estar leyendo sobre la introduccion a la metodologia de cascada note una similitud con lo que estamos viendo en Informatica V. En la clase vimos el proceso de Planificar, Hacer, Verificar y Actuar, en la metodologia de cascada tenemos Requisitar, Diseñar, Implementar y Verificar.*

Hubieron dos grandes cambios en las metodologias de la industria del Software.

La primera fue la introduccion de la metodologia de cascada, esta concebia al desarrollo de software como un proceso lineal en el cual se llevaba acabo la toma de requisitos, el analisis y diseño, la coficiacion y las pruebas. Era muy malo seguirla a rajatabla debido a que muchas veces en un proyecto de software los requisitos desde un inicio no llegan a estar completamente claros. Por tanto, al momento de probar y darle a tus usuarios el software se denota que le falta muchisima funcionalidad, le sobran muchisimas cosas cuando parecia que estabas por terminar!

La segunda fue la introduccion de iteraciones, esta dictaba que solo se tomaban pocos requisitos, se analizaba, se programaba y se probaba, de modo que, en lapsos de tiempo mucho mas cortos se pueda recibir feedback del usuario final para saber como mejorar el producto, y asi avanzar de forma iterativa

Esta ultima fue tomada por metodologias agiles y la metodologia de gestion mas popular hoy en dia es SCRUM, combinada con Agile (iteraciones) forma una potente forma de desarrollar software

##### There Are Technical Practices
Desde los inicios del software, los problemas con la toma de requisitos, el analisis, las pruebas, comunicacion, manejo de proyectos y liderazgo han sido recurrentes. Sin embargo, antes estos problemas eran atacados desde la perspectiva del codigo y no se le prestaba mucha atencion a lo demas. Hoy en dia, nos enfrentamos a todos los retos de forma conjunta y constante, es por eso, que surgieron nuevas metodologias para tener un marco de trabajo sobre el cual estructurar los proyectos.

###### The Structured Methods Era
El desarrollo se basaba en metodologias estructuradas, esto quiere decir que se percibian las funciones por un lado y los datos por otro. Surgieron marcos de trabajo y grandes proyectos bajo esta metodologia, sin embargo, al mantenimiento y la escalabilidad del software era casi nula, eso fue lo que acabo con esta era.

###### The Component Methods Era
El desarrollo se basaba en metodologias por *componentes* (modulos, clases, objetos, espacios, unidades, etc) principalmente influenciado por el paradigma orientado a objetos que concebia a los datos e informacion por igual. Surgieron muchos enfoques, hasta que en 1990 se unifico el modelado creando el UML (Unified Modeling Language) y se impulso la metodologia RUP (Rational Unified Process), todas las demas murieron. 

Esta era culmino con la creacion de practicas mas avanzadas como las arquitecturas EA - Enterprise Architecture, SOA Service-Oriented Architecture, PLA - Product-Line Architecture. Hoy en dia las podemos ver con Web Development, Cloud Services, Mobile Development, etc.

###### The Agile Methods Era
El desarrollo conservo los conceptos traidos desde la era anterior, se estandarizo practicas tecnicas y humanas para crear un marco de trabajo que funcionara sobre la metodologia iterativa, integro la idea de la mejora continua (Esto lo vemos con la creacion de backlogs, refactoring, TDD, etc) para continuar mejorando el desarrollo agil.
##### There Are People Practices
Anterior a las metodologias agiles no se le tomaba importancia al capital humano, se consideraba que eso era parte de R.H. Sin embargo, tras la llegada de Agile al mundo de desarrollo se pasaron a crear nuevas practicas (Como el pair programming, las daily standups) que se enfocaban mas en darle las herramientas a los desarrolladores para que pudieran trabajar de forma continua. Es por eso que es el paradigma mas popular hoy en dia.

##### Consequences
Ya vimos todos los cambios que ocurrieron entre paradigmas, ciclos de vida. los proyectos, por que scrum es popular pero hay que pensar en las consecuencias que ha traido (y probablemente traera) hacer cambios por cambiar:
- Necesidad de nueva capacitacion. Principalmente debido al cambio de vocabulario, de ideologia, de forma de desarrollar, de metodologias, de cambios en el codigo, etc, etc.
- Creacion de 10000 metodologias bajo la misma idea, monolitos. Cada autor busca que te cases con su "forma definitiva de desarrollar software basada en agiles" sin tomar en cuenta las malas ideas que tienen ni nada
- Innovaciones incitan cambios. Que bajo cada innovacion que se haga en la industria se necesitaran cambios y dependiendo la metodologia sera de mayor o menor perdida para todos.

¿Todo esto en que concluye? En perdidas de tiempo, dinero, capital de todos los tipos, tiranias de gobierno en metodologias, etc. En una industria tan grande como el desarrollo de software esto es imperdonable. Para solucionar estos problemas esque se ha la organizacion del SEMAT (Software Engineering Method And Theory)

#### The SEMAT Initiative
Fue una inciativa iniciada por Ivar Jacobson en 2009 para lograr abstraer una serie de practicas bases (llamadas kernel) sobre las cuales se pudieran desarrollar metodos orientados al desarrollo de software basados en la disciplina de la ingenieria.

Los principales problemas que busca atacar son:
- Adaptarse a los problemas de nuestra industria (cambio de requerimientos, de gente, de tecnologias)
- Formar un conjunto de practicas base llamado kernel que sea altamente extensible.
- Apoyado por gente con relevancia en la industria, empresas, universidades, etc.

#### Essence: The OMG Standard
Una vez fueron establecidas como acuerdo todas estas practicas, se busco que fueran altamente adoptadas por todos los desarrolladores del mundo. Para conseguir esto se busco una estandarizacion y en este caso se opto por la OMG.

La OMG acepto la iniciativa de SEMAT y a todo su conjunto de practicas, consejos y terminos le denomino "Essencia".

### Resumen - Software Engineering Methods and Practices
Se busca introducir un poco de historia sobre los metodos y practicas que se han llevado acabo en los ultimos años de la Ingenieria del Software. Esto con el fin de justificar la creacion del conjunto de practicas, conceptos e ideas propuestos por el SEMAT en 2009 (Estandarizado por la OMG como "escencia" en el 2014) de la cual hablará el resto del libro.

**Metodo**. conjunto de tareas que se deben realizar para lograr conseguir el desarrollo de un software.

**Practicas**. conjunto de recomendaciones enfocadas a un aspecto de cualquier metodo de desarrollo.

#### Ciclo de Vida
Entre las practicas del ciclo de vida tenemos los metodos de: Cascada e Iterativas.

El ciclo de vida en cascada sirvio para dar guia y salir de la crisis del software, concebio las primeras ideas de como se tenia que hacer un ciclo de desarrollo, sin embargo no tomo en cuenta el contexto de nuestra industria, en el cual todo cambia y te piden que implementes nuevas funcionalidades, que mantengas, que cambies. 

Fallo al hacerse un estandar debido a que no supo adaptarse a la industria, sin embargo logro su objetivo de introducir un poco de orden en el caos que habia en el mundo de desarrollo

El ciclo de vida iterativo concibe que no se tiene que realizar una gran casacada si no que se tiene que ir haciendo por ciclos, se requisita un poco, se diseña un poco, se programa un poco, se prueba un poco y se despliega para recibir feedback y volver a empezar.

Hoy en dia un ciclo de vida como este es el que se sigue empleando debido a que se adapta a nuestra industria, sin embargo, el problema que enfrentamos esque no hay un conjunto de estandares para referirse a los terminos comunes entre distintos metodos.

#### Tecnicas
Entre las practicas tecnicas tenemos dos formas: Estructuradas, Componentes

Los metodos estructurados se basan en la programacion estructural, en la cual se separan los datos de las funciones y se perciben como conjuntos separados en el cual cualquier dato puede interactuar con cualquier funcion y viceversa. Uno de los metodos mas populares fue el SADT (Tecnica de Analisis y Diseño Estructurado)

Se desecho debido a que surgieron grandes proyectos de ella pero muchisimos fallaban y tenian problemas, principalmente de matenibilidad (Creaba codigo que era dificil de leer, dificil de escalar, dificil de cambiar y no se podia probar).

Los metodos en componentes se basan en la programacion orientada a objetos, en la cual se perciben a datos y funciones como un modulo y estos modulos interactuan entre si mediante interfaces publicas. Aqui en vez de permitir que existieran muchos metodos de desarrollo se busco una estandarizacion y se creo UML y RUP.

No se ha desechado todavia, solo se dejo en el pasado UML y RUP por lo fuerte que era respecto a como se tenian que hacer las cosas, siempre como ellos decian.

#### Agiles
El conjunto de practicas mas utilizado hoy en dia son las agiles, se basa en las ideas de desarrollo iterativas, usualmente una escritura basada en componentes e incorpora practicas mas alla de solo el desarrollo. Practicas humanas para permitir un buen flujo de trabajo mediante reuniones, backlog, pair programming, etc. Practicas tecnicas permitiendo elegir lenguajes comodos para todo el equipo, con buen hardware. Practicas de codigo como el TDD, BDD, DDD, etc. Ademas de esto simplifica todo lo que se ha aprendido a lo largo de la historia y lo conjunta con un desarrollo por prototipos.

#### Escencia y SEMAT
Debido a la poca estandarizacion, el exceso de reinvencion de practicas con 1000 metodologias agiles, la perdida de tiempo, la perdida de dinero y otros capitales, con el SEMAT se busca crear un conjunto de practicas base (kernel le llaman ellos) que sirvan para que todos puedan crear sus propias variaciones de un metodo que sirva como marco de trabajo para que cada equipo pueda desarrollar software a su manera.

Fue aceptado por la OMG en 2014 y fue estandarizado como "Escencia". Es de lo que se hablará el resto del libro.