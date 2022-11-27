---
title: "Grafos"
date: "2022-11-26 19:46"
tags: 
  - algorithms
draft: true
---
Un grafo es un modelado que representa un conjunto de nodos con conexiones entre ellos. Cada nodo es una parada, un movimiento, una posibilidad a la cual podemos dirigirnos mediante sus conexiones con otros nodos.

A las conexiones en un grafo tambien se les llama "edges" (bordes).

Todos los nodos que se encuentran conectados a otro en particular son llamados sus "neighbors" (vecinos).

Las conexiones existentes entre multiples nodos pueden ser clasificadas en niveles. Los vecinos inmediatos de un nodo son llamados de "primer nivel", los vecinos de los vecinos del mismo nodo son llamados de "segundo nivel" y asi sucesivamente.

![[files/GrafosNivelesConexiones.png]]

## Tipos
Existen dos tipos principales de grafos
- Directos. Las conexiones tienen una direccion, por lo que nodo A puede tener una conexion con nodo B pero no necesariamente es al reves a menos que se indique de forma explicita.
- Indirectos. Las conexiones son bidireccionales por lo que nodo A se conecta con nodo B y nodo B con nodo A

![[files/TiposGrafos.png]]

Existen otros tipos especiales en los cuales las conexiones solo van hacia un solo lado. Este tipo de grafos son llamados arboles.
