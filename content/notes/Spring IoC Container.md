---
title: "Spring IoC Container"
date: "2022-10-08 19:30"
tags: 
  - java
  - spring
draft: false
---
El IoC, tambien llamado patron Hollywood jajaja, "no nos llames nosotros te llamaremos". Es una forma de ceder el control del flujo del programa al framework en vez de al codigo.

Se utiliza la Inyeccion de Dependencias, de esta manera se evita la construccion de objetos y se delega la construccion a Spring

Estyo reduce el acoplamiento entre interfaz e implementacion. Ademas permite tener un punto de control para cambios de implementacion

Anotaciones interesantes para la Inyeccion de Dependencia
- @Autowired. Deja al contenedor de spring insertar el bean de forma automatica
- @Qualifier. Especifica al contenedor de spring el bean a insertar por nombre, en un bean permite especificar el nombre que tiene
- @Primary. Marca un bean como el primario para ser elegido en caso de ambiguedad.
- @Lazy. Especifica que la inyeccion no se realizara sino hasta que sea neesario
- @ConditionalOnProperty. Es mucho mas potente, permite colocar expresiones que permiten elegir un bean o otro basado en ellas.
