---
title: "Nombres con Sentido"
date: "2022-10-19 17:56"
tags: 
  - programming
  - ooad
draft: false
---
Es una tecnica que se enfoca en el [[notes/Diseño en Codigo]] de bajo nivel. 

Debido a que los nombres se encuentran presentes en las funciones, las variables, los argumentos, las clases, los paquetes y las aplicaciones; utilizar nombres adecuados, descriptivos y detallados se vuelven muy relevantes.

Elegir un buen nombre lleva tiempo al decidir, requiere de buenas habilidades descriptivas y de un conocimiento de palabras comunes. Sin embargo, este pequeño detalle ahorra mucho mas tiempo a futuro.

Es importante tomar en consideracion que, si un nombre necesita un comentario, entonces no es un buen nombre.

Utilizar un buen nombrado reduce la implicidad en el codigo e incrementa su expresividad para que todos puedan entenderlo.
## Caracteristicas de Buen Nombrado
### Revelan su Intencion
Los nombres son capaces de responder por si mismos las preguntas basicas que cualquiera tendria:
- Por que existe
- Que hace
- Como es utilizado

```Java
// mal nombrado
int x = 189 // days elapsed since creation

// buen nombrado
int daysElapsedSinceCreation = 189; 
```

### Evitan Desinformacion
Los nombres no dejan pistas que podrian ser malinterpretadas si son leidas en cualquier contexto a futuro. 

Por tanto, un nombre que no desinforma:
- Evita el uso de palabras reservadas
- Evita abreviaciones
- Evita nombres que tienen ligeras variaciones
- Evita incoherencia

### Distinciones Claras
- No informan de nada
- No tienen palabras que solo hacen ruido
- No se parecen a otros nombres ya existentes
- Son pronunciables
- Son faciles de buscar
- En caso de ambiguedad, la que es conocida por mas clientes debe ser la mas clara.
- Se apegan a palabras del dominio o de la solucion. Evitan que se les de interpretacion manual.
- Los nombres de las clases deben ser sustantivos
- Los nombres de los metodos deben ser verbos y entenderse por si solos
- No son tontos o graciosos
- Son homogeneos a lo largo de toda la aplicacion.