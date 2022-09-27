---
title: "Nullish Coalescing Operator en JavaScript"
date: "2022-09-27 15:50"
tags: 
  - 
draft: true
---
Este operador sirve para resolver las situaciones en las que hacer el [[notes/Short Circuiting en JavaScript]] llevara a tener errores debido a los falsy values raros (como 0 o '').

Veamos el problema que tiene el operador OR.

```JavaScript
const value = 0;
consle.log(value || 10); // 10
```

Esto debido a que trabaja con falsy values, debido a que 0 es falsy el shortcircuiting pasa a devolver 10.

Por otro lado, veamos al operador nullish coalescing.

```JavaScript
const value = 0;
consle.log(value ?? 10); // 0
```

Esto es debido a que trabaja con Nullish values en vez de Falsy values.

**Los nullish values son Null y Undefined**.
