---
title: "Curso de Diseño Orientado a Objetos"
date: "2022-09-12 17:18"
tags: 
  - oop
  - programming
draft: true
---
## 🌱 Idea Principal

## 🌌 Impacto

## ✍ Mejores Frases

## 📔 Resumen + Notas
51:15 Inicio de Clase 1.

### Overview
En este curso se trataran tres grandes temas
**Diseño**. Codigo bien inspirado del Modelo del Dominio y Bien legible.
- Modelo del Dominio. Estrategias para obtenerlo y relaciones entre clases (Composicion, Asosiacion, Agregacion, Uso, Dependencia).
- Legibilidad. Principios de buen codigo

**Diseño modular**. No solo codigo bien inspirado y legible, ahora modulos bien cohesivos y poco acoplados.
- Cohesion, Acoplamiento y Tamaño
- Modularidad. Modulos y Reparto de Responsabilidades
- Jerarquizacion.
- Interfaz publica
- Diseño por Contrato
- Implementacion
- Patron de Indericcion

**Diseño Orientado a Objetos**. No solo lo anterior, sino aprovechando las caracteristicas del modelo orientado a objetos (Herencia y Polimorfismo).
- Teoria de Lenguajes. Polimorfismo con exactitud
- Principio Open/Closed
- Reusabilidad. Mediante herencia, composicion y parametrizacion.
- Flexibilidad. Polimorfimo. Clases abstractas e interfaces, inversion de control, inyeccion de dependencias, sustitucion de liskov y jerarquizacion. Cualquier herencia por composicion (delegacion).

### Introduccion
#### ¿Por qué necesitamos el Diseño?
Debido a que se busca realizar un software de calidad para cumplir con todos los aspectos de un proyecto de software.
- Cumplir con los requisitos (el ambito) en tiempo, cumpliendo el coste establecido.
- Con una implementacion efectiva
- Con un codigo bien legible

Nos ayuda a crear codigo de calidad en todos los aspectos (seguridad, legibilidad, mantenibilidad).
- Que se puede probar
- Que se puede leer
- Que se puede evolucionar
- Que se puede reutilizar

#### ¿Qué se busca hacer?
##### Analisis
Esta disciplina busca **analizar los requisitos y simplificarlos**, es como una vista general sin hablar todavia de las tecnologias implicadas en ello.

Como resultado se busca simplificar de forma clara y consisa los requisitos en un lenguaje comun para los implicados en el proyecto, de modo que sean faciles de comprender y por tanto, prepare el camino para obtener un diseño adecuado.

Esto utilizando algunos diagramas que den el esqueleto sobre el software a desarrollar.

##### Disenio
Esta disciplina busca **formalizar los requisitos obtenidos de un Analisis, integrando tecnologias** (sistemas operativos, lenguajes de programacion, bases de datos, interfaces de usuario, etc).

*A partir de los requisitos, me pienso como voy a hacer mi software*.

#### ¿Para qué?
Cumplir en tiempo y forma los proyectos, crear codigo de calidad y ser efectivos al desarrollar software.

*Cumplir con una buena cohesion, un poco acoplamiento y con un tamaño adecuado son los principios que subyacen un buen diseño*.

Se busca:
- Analizar el problema mediante diagramas
- Repartir modulos y responsabilidades a un equipo

### Indice
**Estrategias de clasificacion:**
1. Descripcion Informal
2. Analisis Clasico
3. Analisis del Dominio
4. Analisis del COmportamiento
5. Analisis de Casos de Us

**Relaciones entre Clases**
- Tipos de Relaciones
- Relaciones por Colaboracion
	- Composicion / Agregacion
	- Asociacion
	- Dependencia / Uso
- Relaciones por Transmision
	- Herencia por Especializacion
	- Herencia por Extension
	- Herencia por Limitacion
	- Herencia por Construccion

**Antipatron "Descomposicion Funcional"**.

### Modelo del Dominio
*Se busca que el codigo refleje el mundo real, como si fuera una metafora, por tanto, se busca traer conceptos e ideas desde el modelo del dominio para ver todo el universo de objetos*.

#### Descripcion Informal
Esta estrategia que consiste en tomar los requisitos en un documento escrito (regularmente informal) del cual se substraen los sustantivos y los verbos. 

Una vez extraido se dice que *todo sustantivo puede ser una clase y que todo verbo puede ser un metodo*.

Problemas del enfoque: 
- **Ambiguedad del lenguaje natural** par anosotros, cone l uso de sinonimos, antonimos, metaforas, diferentes personas pueden interpretar cosas diferentes del mismo texto.
- **Cosificacion** del lenguaje (Todo verbo puede ser un sustantivo y viceversa). La accion *correr* no solo puede ser un metodo de una persona, cosificado puede ser un *corredor*. Y la clase *Deportista* puede ser transformada a *hacer deporte*.

Razones para entenderlo:
- Ayuda a identificar los nombres y acciones clave que **deben terminar dentro del codigo si o si**.
- Ayuda a **identificar el vocabulario comun entre desarrolladores y cliente** mediante el uso de las palabras que vienen del documento de requisitos.

#### Analisis Clasico
Se formalizan las principales fuentes principales de clases y objetos:
- Tangibles 
- Intangibles

Y tienen dos fuentes principales:
- Problema
- Solucion

Teniendo en mente todo el tiempo la **cosificacion**.

#### Analisis del Dominio
Se busca traer todos los objetos, acciones y relaciones **directamente de la boca de un experto del dominio**, que sea el el que diga las cosas que hay en el sistema.

Caracteristica de un Experto:
- No suele desarrollar Software
- Debe estar fuertemente implicado con el problema, como un usuario final.
- Conoce el vocabulario que se utiliza en el entorno
#### Analisis del Comportamiento
Explica que no solo las clases surgen del dominio del problema, sino las operaciones dinamicas que ocurren en un sistema tambien son una fuente principal de clases y mas especificamente, las operaciones.

*Un objeto es conformado por conocimiento y operaciones que puede realizar. Su responsabilidad recae en la cantidad de contratos que satisface mediante sus operaciones*

Lo anterior no solo se aplica a un objeto, un paquete tambien tiene un conocimiento y una serie de operaciones que debe cumplir. Tambien un subsistema, tiene un conocimiento y una serie de operaciones a cumplir. Eso es el comportamiento, es mas abstracto y se aplica a distintas partes del sistema

**De las primeras tres se obtienen las clases y los datos de palabras directas del experto y de la cuarta se obtiene un flujo de mensajes que se deben mandar las clases para satisfacer las operaciones que necesitan entre ellos y lograr el objetivo del software.**\

##### 

#### Analisis de Casos de Uso
*se lo salta*


#### Antipatron "Descomposicion Funcional"
