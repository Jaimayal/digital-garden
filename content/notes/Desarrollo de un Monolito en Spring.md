---
title: "Desarrollo de un Monolito en Spring"
date: "2022-10-08 19:42"
tags: 
  - 
draft: true
---
## Buenas Practicas Generales
Spring Specification sirve para meter filtros a los recursos de forma estandarizada.
En caso de enviar un request malo es buena practica devolver los tipos de request que un endpoint acepta

Una buena practica esque en post se devuelva la ruta donde se puede recuperar el usuario creado.

Otra buena practica es retornar el header Location despues de crear un recurso.

Los controladores normales no deberian de tener recursos anidados, para ellos se debe de crear otro aparte y a su vez para los recursos anidados se debe hacer otro por si se necesitan hacer operaciones mas alla de lectura (CRUD).

Dependiendo del Dominio un JSON deberia o no contener lo relacionado con un recurso y sus anidaciones. Si se requiere, se pueden enviar links para poder recuperar mas informacion del usuario.

Es una integracion que sirve para hacer Restful APIs navegables entre los distintos endpoints de la API.

## Capa Servicio
- Se implementan las reglas de negiocs
- Residen los algoritmos complejos
- Un Controller puede usar uno o mas Servicios
- Los servicios manipulan los repositorios o DAO

- NO el acceso a datos
- NO la comunicacion con servicios externos (consumo de datos)
- NO algoritmos de controladores, nada de lo que tenga que ver con requests ni mecanismos de comunicacion

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
### Testing Unitario
Se escribe codigo para probar otro codigo. Un test Unitario como su nombre indica, busca probar una unica unidad de codigo.

Los mocks nos sirven para desacoplar las capas y poder testear de forma verdadera la capa.

La anotacion @InjectMocks marca a la clase bajo test que se le van a inyectar los Mocks

La anotacion @Spy sirve para mockear parcialmente comportamientos, se utiliza en vez de @Mock

Anotaciones Utiles de JUnit Jupiter
- @DisplayName. Nombre que se va a mostrar como descripcion del test
- @Order. Orden de ejecucion
- @Disabled. Desactiva al test
- @EnabledOnOs(OS.VALUE). Test que solo se activa al sistema operativo

Cualidades un poco mas avanzadas, test parametrizados
- @ParametirzedTest marca que el test tiene parametros especificados por nosotros
- @ValueSource. Una de las formas de especificar valores de entrada para el test

Libreria muy util **Podam**. Sirve para poder crear multiples objetos de una misma clase y poder poblar listas u otras cosas, sirve mucho para proveer resultados para los metodos de los mocks. Sirve para poder generar informacion Dummy que puede ser utilizada para hacer tests u otras cosas.
- Se recomienda la base de datos H2 para hacer tests a la capa de persistencia
- @Import Hateoeas es necesario para importar la configuracion desde un bean
- 
### Testing de Integracion
Cucumber + Gherkin
