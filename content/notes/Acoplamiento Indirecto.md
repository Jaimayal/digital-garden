---
title: "Acoplamiento Indirecto"
date: "2022-10-22 15:00"
tags: 
  - softwaredev
draft: false
---
Es un tipo de [[notes/Acoplamiento]] dado por la visibilidad. Es aquel que dificulta mucho su identificacion, debido aque esta dado de forma implicita en una interaccion entre clases.

Uno de los ejemplos mas evidentes es cuando:
1. Clase A tiene una dependencia directa con la clase B. Y ademas, esta 
2. Clase B en uno de sus metodos retorna una clase C
3. Clase A utiliza este metodo de la Clase B
4. Ahora la clase C es utilizada en la clase A de forma indirecta

```Java
class A {
	void main() {
		new B().getClassPerformer().someMethod(); // Acoplamiento indirecto
	}
}

class B {
	classC getClassPerformer();
}

class C {
	//...
	void someMethod();
}
```

