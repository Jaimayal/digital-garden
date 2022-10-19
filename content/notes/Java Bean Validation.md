---
title: "Validacion de Datos en API REST"
date: "2022-10-08 19:22"
tags: 
  - softwaredev
  - java
draft: false
---
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