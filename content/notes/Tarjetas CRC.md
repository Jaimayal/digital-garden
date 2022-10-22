---
title: "Tarjetas CRC"
date: "2022-10-21 20:18"
tags: 
  - softwaredev
draft: true
---
Las tarjetas CRC son una tecnica muy util que sirve para desarrollar y experimentar tu pensamiento en terminos de [[notes/Analisis y Disenio]] de Software. 

Los componentes principales de ella son
- Clase
- Responsabilidades
- Colaboradores

![[files/CRCCard.png]]

En la Clase anota el nombre del componente principal, bajo las responsabilidades, las funciones que debe de hacer y en los colaboradores las otras clases con las cuales debe interactuar para poder ejercer sus funciones.

## Ejemplo
Situacion: Un deportista quiere suscribirse a un club con membresia mediante una maquina automatizada.

class Deportista 
resp:
- suscribirse
- darse de baja
colab:
- Registrador

class Registrador
resp:
- validar una suscripcion
- mostrar tipos de membresia
- extender una suscripcion
- permitir una suscripcion
- aceptar tarjeta y efectivo
- permitir una baja
colab:
- Banca Electronica

