---
title: "Implementacion de una Clase"
date: "2022-10-28 16:55"
tags: 
  - oop
draft: false
---
### Cohesion
- Cohesion de Metodos
- Principio de Unica Responsabilidad (S de SOLID)
- Responsabilidad fuera de Lugar. La responsabilidad no esta donde deberia de estar
	- Condigo Sucio por Envidia de Caracteristicas
	- Codigo Sucio por Clase de Datos
	- Codigo Sucio por Cambios Divergentes
- Sin clase para una Responsabilidad. Sin nadie puede asumir la responsabilidad
	- Codigo Sucio por Cirugia a Escopetazos
	- Codigo Sucio por Grupo de Datos
	- Codigo Sucio por Obsesion de Tipos Primitivos
- Clase sin Responsabilidad. Existe una clase pero no tiene nada por hacer
	- Codigo Sucio por Clases Perezosas

#### Cohesion de Metodos
- Las funciones deberian hacer una sola cosa.
- Violaciones
	- Las funciones realizan mas de una operacion
	- Las lineas persiguen objetivos distintos a lo que espeifica el metodo
	- Falta de Cohesion en el metodo
- Solucion
	- Dividir las distintas lineas de distinto tipo en diferentes funciones
	- Evitar el acoplamiento entre distintas funcionalidades de una clase
**Pedirle Cohesion a un metodo**

#### Principio de Unica Responsabilidad
Una clase cohesiva (como deberia de estar hecha) solo **deberia tener un unico motivo de cambio**, es decir, solo se deberia ver afectada por una unica cosa (persistencia, vista, comunicacion solo uno pero no todos a la ves).

**Pedirle cohesion a una clase**.

#### Codigo Sucio por Envidia de Caracteristicas
Una clase que envidia a otra clase pidiendole todo el rato sus caracteristicas para hacer los calculos en vez de que la clase que tiene los datos hacerlos.

Es decir, no se respeta el Patron Experto en la Informacion.

#### Codigo Sucio por Clase de Datos
El otro lado de la moneda, en este caso la clase que permite que le pidan todo y queno calcula nada es la clase de Datos.

#### Codigo Sucio por Cambios Divergentes
Ocurre cuando una clase puede ser afectada por multiples cambios, es decir, si se cambia una tecnologia se cambiara una parte, si se cambia la persistencia otra parte, si se cambia la vista otra parte. Eso esta mal, una clase solo deberia ser afectada por una sola cosa.

La solucion seria dividir esta en diferentes clases.

#### Codigo Sucio por Cirugia a Escopetazos
Es el lado contrario al anterior, en vez de que exista una clase que se encargue de una responsabilidad, esta responsabilidad esta distribuida a traves de multiples clases y si es cambiada tiene que cambiar en varios lugares a la ves.

#### Codigo Sucio por Grupo de Datos
Hay grupos de datos que son utilizados en muchos lados y que en realidad deberia estar como una clase y no como datos separados.

La solucion es crear una clase que ademas de ser reusable puede asumir responsabilidad y aliviar a otras clases.

#### Codigo Sucio Obsesion por Tipos Primitivos
Ocurre cuando en vez de utilizar una clase (donde es necesario porque se requieren operaciones) se utiliza un primitivo con el argumento de que una clase de un atributo no existe.

#### Codigo Sucio por Clases Perezosas
Una clase que tiene muy pocos datos y ni siquiera hace operaciones, es perezosa. Puede ser como un holder nada mas de datos que no hace nada.


### Acoplamiento
#### Codigo Sucio Inapropiada Intimidad (Evita los ciclos). - No te acoples en ciclos
Una relacion bidireccional complica el codigo y muchas veces crea ciclos muy complejos que hacen al codigo dificil de manejar
- Para quitar una relacion bidireccional se debe abstraer eso que tienen en comun las dos clases (se debe cosificar) en otra clase aparte. Entre Compra y Venta se deben conocer, para eviarlo se crea la clase CompraVenta,

#### Codigo Sucio por Libreria Incompleta - No te acoples a librerias
Crea una clase para englobar una libreria, no hagas que la libreria interaccione con todos y despues, cuando quieras cambiar la libreria, se tenga que hacer una cirugia a escopetazos.

ENCAPSULA LA LIBRERIA EN UNA SOLA CLASE. PATRON FACHADA.

La libreria da las primitivas (en su interfaz) y es nuestro deber encapsular para reducir el acoplamiento que tenemos a ella.

### Tamaño
#### Codigo Sucio por Listas de Parametros Largas
Es una variacion del smell code de Grupos de Datos, cuando, en vez de utilizar una clase cohesivas que encapsule operaciones y datos se utilizan un grupo de valores primitivos, lo que incrementa mucho la complejidad de los metodos o clases.

En base a las heuristicas lo maximo serian 2 -3 parametros por metodo.

Para tener cero parametros se necesitan de establecer buenas relaciones entre las clases. Muchas veces no hay necesidad de tenerlas

#### Codigo Sucio por Metodos Largos
Todos los metodos deben ser pequeños 10 a 15 lineas

#### Codigo Sucio por Clases Grandes
Siguiendo las metricas tambien deben ser pequeñas 200 a 500 lineas
