---
title: "Spring Core"
date: "2022-10-29 15:26"
tags: 
  - 
draft: true
---
Modulo base de Spring, contiene multiples conceptos sobre los cuales se basa y desenvuelve las partes del framework.

## Spring IoC Container
Primero debemos entender el concepto de la [[notes/Inversion de Control]]Posteriormente, una forma de este, muy important en Spring es la  [[notes/Inyeccion de Dependencias]].

Estos conceptos estan implementados en Spring mediante los contenedores
- [[notes/ApplicationContext]]
- [[notes/BeanFactory]]

Adicionalmente, para construir los beans Spring necesita de determinada configuracion en formas de metadatos para saber de donde crearlos, su ciclo de vida, scope y algunos otros datos. Todos estos pueden ser proporcionados de dos formas:
- XML (Archivos de Configuracion). Un poco mas legacy pero perfectamente soportado.
- @Anotaciones. Uso moderno de Spring.

Una vez los beans han sido instanciados, sus ciclos de vida han sido definidos y el alcance que tienen a las clases tambien, el contenedor procede a satisfacer las dependencias en los lugares que reconoce como requeridos. 

Antes de proseguir veamos que son los [[notes/Spring Beans]] exactamente.

## Formas de Inyeccion de Dependencias
Las tres formas son:
- Campo directo
- Constructor
- Setter

Para realizarlo de forma explicita podemos utilizar la clasica anotacion @Autowired asi como:
~~~Java
// Via Campo directo
public class SomeClass {
	@Autowired
	private SomeDependency dependency;
}
~~~

~~~Java
// Via Constructor
public class SomeClass {
	private SomeDependency dependency;

	public SomeClass(SomeDependency dependency) {
		this.dependency = dependency;
	}
}
~~~

~~~Java
// Via Setter
public class SomeClass {
	private SomeDependency dependency;

	// constructor

	@Autowired
	public void setDependency(SomeDependency dependency) {
		dependency = dependency;
	}
}
~~~

Los tres modos tienen sus ventajas y desventajas, veamos algunos puntos clave:
- La inyeccion mediante el constructor es la forma mas comunmente utilizada, no necesita anotaciones y por tanto remueve las dependencias de utilizar Spring Framework para que la aplicacion funcione.
- La inyeccion mediante setter es una forma utilizada cuando se busca que solo algunos campos sean actualizados mediante el Spring IoC y al momento que se busca (Es una especie de forma de satisfacer la dependencia Lazy).
- La inyeccion mediante el campo directo no es muy recomendada
