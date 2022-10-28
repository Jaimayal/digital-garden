---
title: "Tecnica de Doble Despacho"
date: "2022-10-28 17:29"
tags: 
  - oop
draft: true
---
Esta tecnica se utiliza cuando un objeto A tiene que responder de una u otra forma dependiendo del tipo de objeto que es B dentro de una Jerarquia Polimorfica.

La mala solucion a este problema seria darle la responsabilidad al objeto A de checar el tipo del objeto polimorfico con el operador 'instanceof' o similar.

La solucion correcta recaeria en dejar que la responsabilidad recayera en cada uno de los objetos B polimorficos, de modo que ellos le pidan a el Objeto A ejecutar el metodo con ellos, pasandose a si mismos como parametro

```Java
abstract class Person {  
    void greet() {  
        System.out.println("Hi!");  
    }  
  
    abstract void accept(Global global);   
}  
  
class Men extends Person {  
    @Override  
    void accept(Global global) {  
        global.visit(this);  
    }  
}  
  
class Women extends Person {  
    @Override  
    void accept(Global global) {  
        global.visit(this);  
    }  
}  
  
class Global {  
    void greet(Person person) {  
        person.greet();  
        person.accept(this);  
    }  
  
    void visit(Men men) {  
        System.out.println("I accept a men");  
    }  
  
    void visit(Women women) {  
        System.out.println("I accept a women");  
    }  
}
```

Ahora para probarlo podriamos utilizar cualquier objeto polimorfico sin problemas

```Java
public class Main {  
    public static void main(String[] args) {  
        Global global = new Global();  
        Person men = new Men();  
          
        global.greet(men);  
    }  
}
```

Utilizar instanceof rompe el principio openclosed.

Ante cualquier mala herencia se debe de considerar la composicion.