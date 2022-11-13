---
title: "Patron Controlador"
date: "2022-10-28 17:00"
tags: 
  - oop
  - ooad
draft: false
---
Es uno de los patrones que le dio vida a la arquitectura MVC. En este, se indica que las Entidades del dominio de tu problema deberian estar desacopladas de las reglas de negocio que van a ser aplicadas a ellas. Ademas, sirven como un intermedio de comunicacion entre estos objetos entidad y las vistas generadas por el [[notes/Patron de Vista Separada]].

**Un controlador maneja el evento proveniente de una vista, se encarga de mantener la logica**

Las vistas son con lo que el usuario final interactua, este unicamente se encarga de recibir datos que pueden provenir desde multiples fuentes (una API, un archivo, un usuario u otro).

Los controladores son aquellos que se encargan de procesar un pedido SIN IMPORTAR EL MEDIO DEL QUE PROVENGA, debido a que las vistas ya prepararon todo para que llegue como me tiene que llegar por el contrato.

Los modelos se encargan de ejecutar y administrar las peticiones ya evaluadas, son los datos sensibles y no pueden estar siendo modificadas asi sin mas.

