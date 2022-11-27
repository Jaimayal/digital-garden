---
title: "Azure"
date: "2022-11-27 09:30"
tags: 
  - cloud
draft: true
---
Plataforma de Microsoft
Soluciones para cumplir
- Infraestructura
- Plataforma
- Servicio

Sigue un modelo Pay as you Go. Se te permite elegir las especificaciones de una computadora y pagar solo por lso servicios que utilizas. Alguien mas se encarga de su mantenimiento.

Algunas de las caracteristicas principales que ofrece Azure son:
- Azure Functions. Servicios Event Driven
- Azure kubernetes. Azute containers.
- Soporte para BD Relacional y en Memoria
- Soporte para BD No relacionales mediante CosmosDB
- Manejo y Soporte para modelos de IA, Data scientists y ML.

Al utilizar cualquiera de estos servicios se te permite distribuir tus aplicaciones globalmente dejando que la plataforma de microsoft gestione la escalabilidad, seguridad, disponibilidad y mantenimiento de tus maquinas en la nube.

Esta basada en la Virtualizacion que separa el hardware y el sistema operatio utilizando un hiper visor. Este hipervisor puede correr multiples maquinas virtuales con diferentes sistemas operativos.

Esta tecnologia se corre en los centros de microsoft (racks), se orquesta y se satisfacen las peticiones de los usuarios con una gran infraestructura por detras que permite orquestrar toda la asignacion, creacion y manejo de maquinas virtuales dentro de uno de los centros de datos de microsoft.

## Azure Portal
Es una Interfaz Grafica de Usuario que permite a un usuario comun gestionar, dar de alta, de baja y controlar los recursos que utilizan sus distintas instancias de maquinas. 

Mediante estas puedes manejar tus recursos desde la creacion hasta sus configuraciones mas especificas 

## Azure Marketplace
Permite la extension y uso de las capacidades de una maquina virtual para permitir a usuarios comunes acceder a conjuntos de configuraciones creadas por grupos de desarrolladores o desarrolladores independientes.

## Azure Resource Manager
Es el servicio de administracion para Azure, permite administrar grupos de recursos, suscripciones y otros grupos relacionados con una cuenta de azure.

Esta plataforma sirve como interfaz para acceder a todos los recursos detras de una cuenta. Realiza la autenticacion y autorizacion y expone diferentes APIs y SDKs para permitir itneraccion externa.

![[files/AzureResourceManager.png]]

## Cuentas
Para usar Microsoft Azure se requiere de una suscripcion. Existe una suscripcion gratuita que te permite explorar una cantidad limitada de recursos. 
Te da acceso a 20 productos de forma gratuita

Adicionalmente, las lecciones de la plataforma de aprendizaje de azure te proveen un espacio aislado que te permite entender la funcionalidad de una de las caracteristicas en especifico. Estas no incurren en ningun costo y son limpiadas de forma automatica tras terminar un modulo.

## Estructura Organizativa
Un recurso de Azure cuenta con cuatro niveles particulares:

![[files/EstructuraOrganizativaAZURE.png]]

- Grupos de Administracion. Ayudan a administrar autorizacion y autenticacion. 
- Suscripciones. Sirve como modelo para establecer limites en la cantidad de recursos para crear y usar. Sirven para administrar costos y recursos creados por usuarios individuales, equipos o proyectos enteros. Ademas se pueden especificar distintas formas de facturacion para separar de forma logica los servicios de una empresa.
- Grupos de Recursos. Los recursos individuales son a su vez agrupados como contenedores logicos que sirven para representar una aplicacion especifica, esto sirve para preservar el orden dentro de una cuenta.
- Recursos. Son instancias especificas de un servicio como una base de datos, una aplicacion web, una maquina virtual u otras. Todo recurso debe pertenercer como minimo y maximo a un grupo de recursos.

Como nota importante debemos notar que elimintar un grupo de recursos incurrira en eleminitar todos los recursos que este contenga.

## Suscripciones
Una suscripcion es un modelo logico que sirve para limitar la cantidad de recursos que una cuenta puede crear respecto a un servicio en especifico. Cada una de estas suscripciones puede manejar por separado su forma de facturacion, su nivel de acceso y los recursos disponibles en ella.

Mediante estas podemos reflejar una estructura organizativa, los diferentes entornos en un equipo de desarrollo (produccion, pruebas, desarrollo) o simplemente para separar la facturacion entre distintos servicios.

Uno de los usos principales es la gestion de facturacion para ver bien un desgloce por departamento o por seccion. La jerarquia de como funciona esto la podemos ver a continuacion:

![[files/JerarquiaFacturacionAzure.png]]

## Grupos de Organizacion
Son necesarios cuando una cuenta tiene muchas suscripciones. Sirven para adminsitrar con mayor eficacia el acceso y las directivas de cada suscripcion.

Son solo otro nivel que permite heredar multiples permisos a diferentes suscripciones, otro modelo mas para organizar tus suscripciones individuales.
## Regiones de Azure
Como se sabe, los centros de datos de Microsoft se encuentran distribuidos por todo el planeta. Es importante tener en mente esta informacion al gestionar grupos de recursos y recursos individuales debido a que estos se deben encontrar forzozamente en uno o distribuido a traves de distintos centros de una region.

Cuando se crea un nuevo recursos dentro de Azure se debe elegir una region en la que se busca implementarlo. Los centros se encuentra distribuidos por todo el plaenta y estan conectados mediante redes de baja latencia.

La distribuciona ctual a fecha del 11/27/2022 es la siguiente:
![[files/DistribucionCentrosAzure.png]]

Estas sirven para identificar la ubicacion fisica de un recurso en el planeta.

Un ejemplo de una region podria ser Oeste de EU. Centro de Canada. Centro de Mexico. Norte de China.

## Zona de Disponibilidad de Azure
Para asegurar la disponibilidad de un recurso en especifico se debe de garantizar que esta se encuentre duplicada de forma redundante en mas de un entorno en una region.

Las zonas de disponibilidad son creadas usando uno o mas centros de datos. Existen un minimo de tres zonas en una sola region.

Azure provee esta funcionalidad utilizando las Zonas de Disponibilidad. Esta es un centro de datos separado de una region de Azure, se modo que, si una region deja de funcionar, sus recursos se encontraran disponibles en otras zonas.

Para lograr esto se debe colocar el grupo de recursos de la aplicacion critica dentro de una zona y posteriormente debe ser replicada en otra. 

Como es logico, el uso de estos requiere de un costo extra.

Algunas de las categorias de recursos disponibles para una zona de disponibilidad son:
- Servicios de Zona. Se puede aclarar un recurso a una zona especifica (Usualmente maquinas virtuales, direcciones IP u otras).
- Servicios de Redundancia de Zona. La plataforma se replica entre zonas.
- Servicios no Regionales. Resistentes a las interrupciones de la zona y de las de toda la region.

## Pares de Regiones de Azure
Ante riesgos graves en los cuales se afecte a dos o mas centros de datos se utilizan los Pares de Regiones.

Un Par de Regiones existe debido al emparejamiento que ocurre entre dos zonas de la misma area geografica que se encuentre como minimo a 500km de distancia fisica.

Esto permite reducir la probabilidad de tener interrupciones ante cualquier desastre o disturbio que pueda ocurrir a gran escala.