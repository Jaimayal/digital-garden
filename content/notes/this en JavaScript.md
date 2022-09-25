---
title: "this keyword"
date: "2022-09-25 08:58"
tags: 
  - javascript
draft: true
---
Es una referencia creada para referirse al objeto actual (En el caso de [[notes/JavaScript]], al [[notes/JavaScript Execution Context]] actual).

En JavaScript esta referencia es dinamica y cambia dependiendo de la forma en que se llame a una funcion. 

### Metodo
Si se llama como metodo (propiedad de un objeto) la keyword 'this' hara referencia al objeto que la contiene y por tanto, tendra acceso a sus otras propiedades (otras funciones  y otros atributos.)

### Llamada simple
Si se llama una funcion simple desde cualquier punto esta tendra el valor de 'undefined' en el caso del strict mode y Window en caso contrario.

![[files/thisUndefinedOrWindow.png]]

### Arrow Function
El arrow function no tiene keyword this, por tanto, es como si todo el tiempo estuvieramos hablando del this desde donde se le declaro. Por ejemplo, si la tratamos de utilizar dentro de un objeto literal lo mas seguro esque si usamos 'this' nos refiramos al objeto window (debido a que desde ahi se esta declarando al objeto) y si utilizamos el strict mode, obtendremos undefined.

![[files/thisArrowFunc.png]]

Por eso esque es **buena practica no utilizar arrow functions como metodos**.

### Llamada desde cualquier otro elemento
Si se trata de una expresion funcional y se le llama desde cualquier otro elemento menos una llamada simple la keyword this apuntara al objeto que la llamo.  

![[files/thisDesdeBoton.png]]

En este caso, el codigo devuelve el elemento 'boton', por tanto, es posible modificar su lista de clases.

### Resumen
![[files/thiskeywordjavascript.png]]
