---
title: "Cloud Computing"
date: "2022-11-27 09:37"
tags: 
  - cloud
draft: true
---
Cloud Computing ofrece servicios informaticos para cualquier persona fisica o moral que este interesada en subir y mantener sus aplicaciones en computadoras con buenas capacidades a cambio de una renta por servicio individual.

Los servicios van desde servicios web basicos hasta la ejecucion de programas especializados (IA, Machine Learning, NLP, etc), pasando por Bases de Datos, Administracion de Datos, IoT entre otras.


- Poder de Computacion. Cantidad de procesamiento que esta puede hacer
- Almacenamiento. Volumen de datos que se puede guardar en una computadora

Todo de forma dinamica, solo pagas por lo que utilizas sin hacerte cargo de todo el mantenimiento (acutalizaciones, limpieza, pagos de software, etc).

La Computacion en la Nube ofrece los servicios necesarios para mantenerse a la vanguardia con el avance tecnologico.

## Tipos de Nube de Computacion
Existen distintos tipos de modelos que puede seguir una empresa para ofrecer servicios en la nube. En particular se identifican tres tipos:
- Publica. Los servicios se ofrecen a traves de la red publica y estan disponibles para quien sea que busque rentarlos.
- Privada. Los recursos informaticos solo son accesibles por un grupo restringido de personas dentro de una organizacion.
- Hibrida. Combina aspecots publicos y privados, es decir, se permite compartir y aparte gestionar de forma interna los mismos.

## Ventajas
- Disponibilidad. Los servicios siempre estan disponibles, sin tiempos de caida.
- Escalabilidad. Permite llevar las aplicaciones al siguiente nivel implementando funcionalidades, mejorando las existentes y manteniendo las viejas. Permite modelos de escalado vertical (mas recursos) y horizontal (mas instancias)
- Elasticidad. Las aplicaciones pueden autoajustarse para escalar cuando sea necesrio
- Agilidad. Agilidad de desarrollo, gestion y soporte.
- Soporte. Facil recuperacion de errores y soporte para muchas areas geograficas

## Gastos de Capital
- Gastos de Capital. Hacen referencia a inversion en infraestructura fisica que se deprecia o amortiza a traves del tiempo.
- Gastos Operativos. Hacen referencia a inversion en servicios o productos que son deducibles el mismo año que se utilizan-

La computacion en la nube es declarada como Gastos Operativos. Es un servicio en el cual se gasta conforme se utiliza y debido a que no son parte de la infraestructura de la organizacion no se ven afectados por depreciacion o amortizacion que redusca su vida util a traves del tiempo.

> En resumen, CapEx (Gastos de Capital) requiere unos costos financieros previos considerables, así como unos gastos continuos de mantenimiento y soporte técnico. En cambio, OpEx (Gastos Operativos) es un modelo basado en el consumo, así que una organizacion solo es responsable del costo de los recursos informáticos que utiliza.

No hay costos por adelantado, no se compra ni administra infraestructura. Se permite utilizar mas recursos conforme se necesiten y reducirlos conforme no se necesiten.

## Modelos de Servicio disponibles
Existen diferentes modelos de responsabilidad que se pueden delegar entre un cliente de la nube y un proveedor de computacion en la nube.

Clasificados por niveles tenemos:
- IaaS. Infrastructure as a Service
- PaaS. Platform as a Service
- SaaS. Software as a Service

Un resumen sobre como se ven los servicios disponibles para cada modelo seria

![[files/ModelosServicioCloud.png]]

### IaaS
*Infraestructura como Servicio - Infrastructure as a Service*.
Es un modelo en el cual se te brinda unicamente los recursos informaticos en hardware (servidores) para que puedas utilizarlos como necesites.

Las responsabilidades del proveedor recaen en el mantenimiento y actualizacion del hardware.

Las responsabilidades del cliente recaen en el uso que se le da a la infraestructura, la actualizacion de los sistemas operativos y otro software.

Entre sus principales ventajas tenemos:
- Evitas los Gastos por Infraestructura
- Se reparte las labores de administracion, el cliente se encarga de mantener el software y el proveedor mantiene la infraestructura
- Se basa en el consumo, unicamente paga por lo que utilizas y se utilizan Gastos Operativos
- Te permite tener el control de gestion y administracion del hardware

### PaaS
*Plataforma como Servicio - Platform as a Service. Tambien llamada Arquitectura **Serverless** en el [[notes/Desarrollo de Software]]*

Es un modelo en el cual se te brindan los recursos en hardware y el soporte en software para que puedas deployear tus aplicaciones software sin preocuparte por gestionar nada relacionado con el hardware y software fisico (SO).

Entre sus principales ventajas tenemos:
- Todas las ventajas del IaaS reduciendo un poco la cantidad de control que tiene el cliente sobre la infraestructura y parte del Software
- Menor necesidad de conocimientos tecnicos puesto que el proveedor ahora tambien administra los servidores
- El usuario se centra en el desarrollo de aplicaciones.

Sin embargo, te encuentras una serie de limitaciones que pueden llegar a afectar la funcionalidade de las aplicaciones, es un datoa  tener en cuenta.

#### Serverless
Es una forma de llamarle a un PaaS en la industria del software, se refiere a que los desarrolladores se pueden centrar en desarrollar aplicaciones software sin preocuparse por la administracionde servidores y todo lo que conlleva.

> Es importante tener en cuenta que los servidores siguen ejecutando el código. El término "sin servidor" procede del hecho de que las tareas asociadas a la administración y el aprovisionamiento de la infraestructura son invisibles para el desarrollador. Este enfoque permite a los desarrolladores centrar su atención en la lógica de negocios y ofrecer más valor al núcleo de la empresa. La informática sin servidor ayuda a los equipos a aumentar su productividad y a llevar los productos al mercado con más rapidez, y permite a las organizaciones optimizar mejor los recursos y seguir centrándose en la innovación.
### SaaS
*Software como Servicio - Software as a Service*
Es un modelo en el cual ya no solo se te brindan los recursos de hardware si no que se te brinda toda una plataforma de Software incluyendo maquinas virtuales, recursos de red, bases de datos y aplicaciones para que unicamente puedas centrarte en generar informacion y contenido mientras que todo es administrado por el proveedor de la nube.

Provee las mismas ventajas que el PaaS reduciendo todavia mas la cantidad de conocimiento tecnico necesario para gestionar y crear contenido.

La mayro desventaja que tiene es el fuerte acoplamiento que tienes con la plataforma de tu eleccion y la limitacion de aplicaciones que tienen, es decir, existe una gran posibilidad de que una aplicacion para un nicho o funcion muy especifica no este implementada.


Podemos observar la distribucion de responsabilidades en detalle entre estos tres modelos:
![[files/ResumenModelosCloud.png]]

