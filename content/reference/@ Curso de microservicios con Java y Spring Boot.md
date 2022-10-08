---
title: "Curso de microservicios con Java y Spring Boot"
date: "2022-10-07 07:43"
tags: 
  - 
draft: true
---
## 🌱 Idea Principal

## 🌌 Impacto

## ✍ Mejores Frases

## 📔 Resumen + Notas
1. Arquitectura Orientada a Microservicios
2. Integracion y Despliegue continuo
3. Java 
4. Spring Boot
5. API REST CRUD
6. Postman Consumo
7. Lombok
8. Externalizacion de Parametros

## Arquitectura Orientada a Microservicios
Monolitico. Software que contiene toda la solucion integra.

Causa dependencias entre cada modulo.

Microservicios. 
- Dividir toda la solucion en multiples modulos llamados microservicios en el que cada uno resuelve una funcionalidad.
- Los microservicios se comunican regularmente mediante REST o sistemas de mensajeria como RabbitMQ.
- Se logra muy bajo acoplamiento afernte y eferente.
- Aumenta la complejidad de despliegue{
- Desarrollo puede ser agnostico al lenguaje
- Permite reutilizarse en distintas soluciones para problemas.

Anatomia de un Microservicio
![[files/ComponentesMicroservicio.png]]

La capa Controller solo debe encargarse de enviar los datos que recibe del mundo exterior a la capa Service.

La capa Service debe contener toda la logica de negocio.

La capa DAO unicamente debe encargarse de comunicarse con la persistencia de la aplicacion

## CI/CD
Docker. Te permite crear un contenedor en el cual puede existir cada microservicio con su sistema operativo. 
- Cada contenedor puede heredar de una imagen base que ya tiene instalada todas las dependencias necesarias para que los microservicios corran

OpenShift. Es un orquestador de maquinas Docker (PaaS) que te permite desplegar cada container de acuerdo a las necesidades que tiene cada uno (load balancing)., es decir, te permite escalar cada microservicio de acuerdo a las necesidades que se tienen.

Spring Specification sirve para meter filtros a los recursos de forma estandarizada.

Una buena practica esque en post se devuelva la ruta donde se puede recuperar el usuario creado.

Otra buena practica es retornar el header Location despues de crear un recurso.

Los controladores normales no deberian de tener recursos anidados, para ellos se debe de crear otro aparte y a su vez para los recursos anidados se debe hacer otro por si se necesitan hacer operaciones mas alla de lectura (CRUD).

Dependiendo del Dominio un JSON deberia o no contener lo relacionado con un recurso y sus anidaciones. Si se requiere, se pueden enviar links para poder recuperar mas informacion del usuario.
## Rest Buenas Practicas
- Rest es orientado a recursos, por tanto, poner plurales en las URI
- Entregar codigos HTTP adecuados
- No anidar mas de tres niveles de recursos
- Tener un JSON claro de maximo dos - tres niveles de anidacion
- Integrar paginacion
- Integrar Sorting
- Integrar filtros
- Documentar la API
	- Preferentemente OPEN API - Swagger
- Generar links de Navegacion
	- Preferentemente siguiendo HATEOAS
- Asegurar la API definiendo roles (seguridad)
- Exportar clientes de demostracion
	- Preferentemente usando POSTMAN
- Entregar errores definidos y verbosos
- Validacion de Campos
- Versionado de la API

## Externalizacion
La externalizacionc es un proceso en el cual se pasan las propiedades que son ajenas al codigo a archivos de texto plano que pueden ser importados hacia el codigo.

En Spring la externalizacion se hace a archivos de texto plano con terminacion .properties (app.properties, config.properties, etc).

Para acceder a ellos se utiliza SpEL y regularmente se crean Beans a partir de estas propiedades en texto plano. 

## OpenAPI - Swagger
Es un conjunto de aplicaciones que sirven para generar codigo y documentacion interactiva siguiendo el estandar de OpenAPI.

En Spring puede ser integrada para hacer ingenieria inversa, es decir, generar un documento Swagger a partir de una API ya establecida. Para ello existe una libreria llamada springfox

La libreria nos añade anotaciones para poder documentar la interfaz generada de Swagger.
- @ApiModel - Documentacion para el modelo
- @ApiModelProperty - Documentacion para un atributo del modelo
- @Api - Documentacion para un controlador
- @ApiOperation - Documentacion para un metodo de un controlador
- @ApiResponse - Documentacion para un metodo de un controlador, pero especifico para los codigos de respuesta
- @ApiParam - Documentacion para los parametros de un metodo


Ademas, es buena practica guardar el YAML que te da esta ingenieria inversa como documentacion para referencias futuras.
## HATEOAS
Es una integracion que sirve para hacer Restful APIs navegables entre los distintos endpoints de la API.

## Java Bean Validation - JSR 380
Sirve para validar los datos que son insertados por un usuario, regularmente estos validadores se mantienen en el DTO y se manejan con anotaciones.
- @Regex
- @Positive
- @Min
- @Max
- @Size
- @NotNull
- @NotBlank

Gracias a estas y otras se nos permite hacer validaciones a los datos de entrada de un usuario.

La mejor practica es construir los mensajes de los validadores mediante una externalizacion, es decir, en un archivo .properties.

Adicionalmente, tambien se debe de crecar un POJO para poder enviar los errores a traves de JSON al cliente.

### Externalizacion e Internacionalizacion
Los mensajes de las constraints de validacion pueden (y deben) ser externalizados aun archivo .properties en resources. De esta forma, aseguramos que la API tenga consistencia atraves de archivos planos.

Ademas, gracias a ellos podemos agregar internacionalizacion al API para que dependiendo del RequestParam ?lang=  se pueda recibir un mensaje externalizado.

### Custom Validators
Adicionalmente tambien existe la forma de crear tus propios validators por anotaciones.

Para ello se necesitan dos clases
- @Interface la anotacion que sirve para decorar los atributos.
- un Validador que implementa ConstraintValidator\<@interface, K\> que contenga toda la logica.


### Validacion por Grupos
Permite validar ciertas anotaciones cosas solo si la entrada de validacion se hace por determinado grupo por ejemplo, en creacion se hace una validacion y en actualizacion se hace otra.

- Para crear un grupo se crean interfaces con el nombre del grupo
- Despues se especifica en las anotaciones mediante su propiedad 'groups' bajo que grupos (.class) tienen que ser validados
- Se debe aplicar la validacion utilizando @Validated y especificar el grupo por el que se va a aplicar la validacion (.class)

Debido al punto 3. ahora solo se van a aplicar todas las validaciones que esten marcadas con ese grupo

## Capa Servicio
- Se implementan las reglas de negiocs
- Residen los algoritmos complejos
- Un Controller puede usar uno o mas Servicios
- Los servicios manipulan los repositorios o DAO

- NO el acceso a datos
- NO la comunicacion con servicios externos (consumo de datos)
- NO algoritmos de controladores, nada de lo que tenga que ver con requests ni mecanismos de comunicacion

### IoC
Patron Hollywood jajaja, no nos llames nosotros te llamaremos.

Se utiliza la Inyeccion de Dependencias, de esta manera se evita la construccion de objetos y se delega la construccion a Spring

Estyo reduce el acoplamiento entre interfaz e implementacion. Ademas permite tener un punto de control para cambios de implementacion

Anotaciones interesantes para la Inyeccion de Dependencia
- @Autowired. Deja al contenedor de spring insertar el bean de forma automatica
- @Qualifier. Especifica al contenedor de spring el bean a insertar por nombre, en un bean permite especificar el nombre que tiene
- @Primary. Marca un bean como el primario para ser elegido en caso de ambiguedad.
- @Lazy. Especifica que la inyeccion no se realizara sino hasta que sea neesario
- @ConditionalOnProperty. Es mucho mas potente, permite colocar expresiones que permiten elegir un bean o otro basado en ellas.

## Consumo de Servicios Externos
Muchas veces es parte de la capa de negocios pero debe de estar separada de la logica dura de negocio para mantener una modularidad. Para ello se crea una capa "Cliente" que es la que se encarga de consumir los servicios.

- La capa cliente es un segmento de codigo que se enfoca en recuperar datos de otras APIs, cloud, web scrapping, etc.

![[files/LayerClient.png]]

Regularmente se utiliza **RestTemplate** para implementar la logica del consumo a otros servicios REST.

Estas RestTemplate se añaden a clases concretas usualmente construidas a partir de interfaces para establecer contratos y aprovechar Spring. Se mapean a DTOs especificos y son utilizadas desde la logica fuerte en la capa de Servicio

### Feign
Hay otra forma de hacerlo utilizando el Stack de Netflix y se hace mediante todo anotaciones y se puede utilizar tambien para consumir servicios

## Librerias Utiles
- Apache POI. Permite interactuar con cualquier programa de Office (Powerpoint, Word, Excel, etc)
- iTEXT. Libreria para trabajar con PDF y otros formatos de texto planos.

## Optional
Una de las nuevas cosas que ofrece Java 8, Permite especificar que un objeto puede estar o no presente (es  opcional), de tal modo que las comprobaciones, excepciones y el trabajo con la API stream es mucho mas facil.

## Sistema de Trazas - Logback
Presente en Spring, es subyacente, es decir, se utiliza en Spring. 
- Logback viene a reemplazar a log4j
- Es la forma de guardar informacion del programa
- Permite trazar errores
- Pueden ser persistidas en archivos planos, bases de datos, u otros.

Frameworks 
- Log4j
- Logback
- JUL

Niveles de Trazas
- Debug
- Info
- Warn
- Error
- Fatal

Medios para persistencia (Appenders)
- Console
- File
- FTP
- Kafka
- Cassandra
- 

### Recomendaciones generales
- Configurar un Logger Manager
- Implementar logs Info en las acciones mas signifcativas
- Implementar debug en las acciones criticas (riesgosas, las que me dan mas miedo)
- Implementar error lo mas verbosos posible

### Configuracion
Para cambiar la configuracion de logback (incluido con Spring) podemos utilizar el archivo logback.xml dentro de resources
- ConsoleAppender - Apende las trazas a la consola
- FileAppender - Apender a un archivo
- RollingFileAppender - Apender a un archivo que reinicia cada que cumple determinada expresion (cada x tiempo, cada cantidad de lineas, etc). Ademas tambien puede eliminar cada ciertas lineas, cada cierto peso y cada cierto tiempo
- SiftingAppender - Apender que sirve para logear hacia un archivo pero con la ventaja que permite colocar condiciones logicas para agregar a los archivos bajo determinadas situaciones, aplicaciones o contextos


Aparte de definir un Appender se tiene que especificar en el rel los distintos appenders a utilizar.

Existe la anotacion @Slf4j para hacer logging evitando escribir toda la parte verbosa del logging

Ademas, nos permite establecer condicionales con la etiqueta \<if\> lo que nos permitira cambiar los appender, la configruacion, las trazas y todo con solo cumplir o cambiar una variable de un archivo .properties!. Esto se hace gracias a la libreria **Janino**.

Ademas, tambien podemos definir estrategias para loggear diferentes paquetes. Para ellos podemos utilizar la etiqueta \<logger\> en donde podemos especificar el paquete, el nivel de tracing, los appenders y asi a cada uno que queramos!

### Infraestructura de Logging
- Logs
- Logstash para Data Processing
- Elasticsearch para Storage
- Kibana para Visualizar





## Capa de Persistencia
Spring utiliza Hibernate como motor ORM.
- Jpa es un estandar que envuelve a Jdbc.

dockercompose es una solucion YAML que permite declarar las imagenes necesarias para una solucion fullstack (Base de datos, Back, Front, etc).

docker brinda mucha practicidad para trabajar con bases de datos y programas complejos

### Dependencia
Se necesita de dos dependencias escenciales
- La spring boot starter de JPA
- El driver de la base de datos a utilizar

Posteriormente se necesita de agregar configuracion al application.properties

initialization.mode=always. Es un parametro importante debido a que permite tener una inicializacion de tablas mediante un script sql. Se pueden tener multiples y se seleccionara el que coincida con el especificado en el platform de application;properties

jpa.hibernate.ddl=update|create-drop|validate|none. Similar al anterior pero en este claso se realiza de acuerdo a los cambios en las clases marcadas con @Entity.

### Queries con Wildcards
La clave esta en los nombrados que se les puede dar a los metodos, expresado de esta manera se pueden obtener los datos sin problema.

Se puede obtener mas informacion en la [documentacion oficial](https://docs.spring.io/spring-data/jpa/docs/1.3.0.RELEASE/reference/html/jpa.repositories.html#jpa.query-methods).

### Queries con @Query
Tambien se pueden hacer queries cutomizadas utilizando la anotacion @Query, escribir la consulta y utilizar wildcards en ella que son pasados al metodo como parametro.

### Pageable y Sort
Pageable es un objeto especial que nos sirve para limitar la cantidad de elementos que deben de mostrarse en una pagina.

Los datos de Pageable llegan desde la URI mediante @RequestParam, requiere de un valor de 'page' y un valor de 'size' que determina cuantos elementos tendra la pagina.

Podemos darle valores por defecto a un Pageable para que no sea necesario que el frontend lo tenga que enviar.
- @PageableDefault(size, sort, direction). En caso de no ser suministrados

Sort es otro objeto especial

### Repositorios NoSql
JPA tambien tiene soporte para bases de datos NoSQL como Mongo o Cassandra basadas en Documentos.

Para añadir soporte a ellos solo es necesario;
- Agregar la dependencia
- Crear unos beans para Mongo
- Añadir un Repositorio
- Las entities ahora son decoradas con @Document

## Mapping
### Dtos vs Entities
Los entities deben interaccionar con la base de datos y servir como objetos de transferencia

Los DTOs deben ser los objetos utilizados para la comunicacion con clientes externos

Al proceso de pasar un DTO an un Entity o viceversa es el Mapping

La libreira de MapStruct provee una forma de convertir entre entities y DTOs de forma automatica.

1. Agregar Dependencia
2. Agregar plugin para integracion con Lombok
3. Crear una interfaz para hacer el mapping

## Testing
Todas las capas deben de ser testeadas, cada una de forma aislada de las otras. Hacer estas pruebas no asegura que el software este 100% libre de errores.
### Testing de Software
### Testing Unitario
Se escribe codigo para probar otro codigo. Un test Unitario como su nombre indica, busca probar una unica unidad de codigo.

Los mocks nos sirven para desacoplar las capas y poder testear de forma verdadera la capa.

### Testing de Integracion
Cucumber

## Diseño del Software
Autores Importantes
- Edsger Dijkstra
- Edward Yourdon
- Ivar Jacobson
- Grady Booch
- James Rumbaugh
- Erich Gamma
- Martin Fowler
- Robert Martin
- Kent Beck

