---
title: "Clase Object vs Parametrizacion (Genericos)"
date: "2022-10-29 15:30"
tags: 
  - java
draft: true
---
En Java existen dos formas de hacer una clase que puede guardar cualquier elemento. 

La primera es la clase Object, la cual es insegura, nos requiere de utilizar constantes casteos y nos permite guardar cualquier elemento sin ningun error en compilacion, por tanto, podriamos guardar no solo los objetos que queremos sino quien sea puede meter un elemento arbitrario al deseado.

Por tanto, utilizar Object nos va a traer muchos problemas en runtime por utilizar mucho casting. 

Utilizar genericos es la mejor forma puesto que nos permite reutilizar una clase para cualquier objeto y a la vez levantar errores de compilacion cuando sea necesario.

Adicionalmente, nos provee una forma de reusabilidad alternativa a la del mecanismo de [[notes/Herencia]]. Esto lo podemos ver cuando las comparamos de forma directa ([[notes/Herencia frente a Parametrizacion (Genericos)]]).