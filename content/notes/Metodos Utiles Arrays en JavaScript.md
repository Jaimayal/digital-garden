---
title: "Metodos Utiles Arrays en JavaScript"
date: "2022-09-18 15:29"
tags: 
  - javascript
draft: false
---
Algunos de los metodos mas basicos para trabajar con arrays en JavaScript:
- push. Apende un elemento al final del array
- unshift. Apende un elemento al **inicio** del array.
- pop. Remuve un elemento al **final** del array
- shift. Remueve un elemento al **inicio** del array
- indexOf. Retorna el indice de un elemento o -1 si no existe
- includes. Retorna un booleano, true si incluye un elemento, false si no.

```JavaScript
const array = ['elem1', 'elem23', 'elem98']

array.push('elem3') // ['elem1', 'elem23', 'elem98', 'elem3']
array.unshift('elem0') // ['elem0', 'elem1', 'elem23', 'elem98', 'elem3']
array.shift() // ['elem1', 'elem23', 'elem98', 'elem3']
array.pop() // ['elem1', 'elem23', 'elem98']

array.includes('elem0') // false
array.indexOf('elem23') // 1
```