---
title: "JavaScript Engine y Runtime"
date: "2022-09-23 12:45"
tags: 
  - javascript
draft: true
---
JS Engine. El programa principal de un solo hilo que ejecuta el codigo de JavaScript, cada navegador tiene el suyo propio.

Cada JS Engine esta compuesto por
- CallStack -> Execution Context
- Heap -> Memoria, donde los objetos son guardados

Todos los JS Engine modernos utilizan compilacion Just-In-Time, por tanto, podemos definir el ciclo de ejecucion de codigo en JavaScript mediante los siguientes pasos:

1. Entra codigo a un JS Engine
2. Parseo. Es convertido linea por linea a un Abstract Syntax Tree (AST), en donde se almacenan todas las keywords relevantes del lenguaje.
3. Compilacion. Es convertido a codigo maquina
4. Ejecucion. Se ejecuta el codigo maquina hacia el callstack.
5. Optimizacion. Debido a que se busca rapidez en la web, ocurre un ciclo de recompilacion y reejecucion para optimizar el codigo mejor optimizado sin detener la ejecucion.
