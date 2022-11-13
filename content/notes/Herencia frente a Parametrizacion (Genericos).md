---
title: "Herencia frente a Parametrizacion (Genericos)"
date: "2022-10-29 15:31"
tags: 
  - oop
draft: false
---
La parametrizacion es la programacion generica, en general se usa cuando se busca tener exactamente las mismas operaciones en una clase pero hablando de diferentes cosas. 

Por ejemplo una ColaDePersonas tiene las mismas operaciones que una ColaDeHormigas. Si quisieramos usar Jerarquia aqui tendriamos que hacer que la clase base utilizara Object, y todos los objetos que entraran serian objects y cuando necesitaramos obtener uno se tendria que hacer downcast preguntando el tipo y es un caos.

Por otro lado, con la programacion parametrizada no tenemos esa necesidad, podemos tener una pila de T, cualquier objeto y las operaciones ya sabrian por si mismas de que tipo de objeto se esta tratando.

La diferencia entre usar genericos y Object es que con genericos te ahorras todos los cast y poder guardar cosas que no se podrian.

Esta es un aspecto en que la herencia no sirve para hacer reusabilidad