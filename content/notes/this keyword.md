---
title: "this keyword"
date: "2022-09-25 08:58"
tags: 
  - 
draft: true
---
Es una referencia creada para referirse al objeto actual (En el caso de [[notes/JavaScript]], al [[notes/JavaScript Execution Context]] actual).

En JavaScript esta referencia es dinamica y cambia dependiendo de la forma en que se llame a una funcion. 

Si se llama como metodo (propiedad de un objeto) la keyword 'this' hara referencia al objeto que la contiene y por tanto, tendra acceso a sus otras propiedades (otras funciones  y otros atributos.)

Si se llama una expresion funcional, la keyword this apuntara a quien lo llamo (Window, Boton, Click, Evento, etc)

Si se trata de un arrow function, la keyword this es heredada desde el scope del padre. 

Por tanto, si la tratamos de utilizar dentro de un objeto literal lo mas seguro esque si usamos 'this' nos refiramos al objeto window y si utilizamos el strict mode, obtendremos undefined.

![[files/thisArrowFunc.png]]

Por eso esque es **buena practica no utilizar arrow functions como metodos**.

Si se trata de una expresion funcional y se le llama desde cualquier otro elemento, la keyword this apuntara al objeto que la llamo.  

![[files/thiskeywordjavascript.png]]
