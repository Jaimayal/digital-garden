---
title: "Buenas Practicas API REST"
date: "2022-10-08 19:07"
tags: 
  - softwaredev
draft: false
---
A continuacion una lista de buenas practicas recomendadas al desarrollar una RESTful API
- Rest es orientado a recursos, por tanto, poner plurales en las URI
- Entregar codigos HTTP adecuados
- No anidar mas de tres niveles de recursos
- Tener un JSON claro de maximo dos - tres niveles de anidacion
- Integrar paginacion
- Integrar Sorting
- Integrar filtros
- Documentar la API
	- Preferentemente OPEN API - Swagger
- Generar links de Navegacion
	- Preferentemente siguiendo HATEOAS
- Asegurar la API definiendo roles (seguridad)
- Exportar clientes de demostracion
	- Preferentemente usando POSTMAN
- Entregar errores definidos y verbosos
- Validacion de Campos
- Versionado de la API
