---
title: "Java GUI Course [Swing]"
date: "2022-09-14 09:15"
tags: 
  - java
  - programming
draft: true
---
## 🌱 Idea Principal

## 🌌 Impacto

## ✍ Mejores Frases

## 📔 Resumen + Notas

#### 5. BorderLayout
Es un gestor de tamanio de componentes que sirve para establecer posiciones de forma sencilla en un contenedor. 

En el ejemplo que vimos, se utilizaba el LayoutManager por defecto, llamado `BorderLayout`.

Para aplicarlo consiste en dos pasos sencillos:
1. Agregarlo a la configuracion del contenedor (JFrame, JPanel, etc).
2. Agregar los componentes dandole una direccion desde el metodo `.add`

Ejemplo: 

```Java
public static void main(String[] args) {
	// Definicion del contenedo principal  
	JFrame frame = new JFrame();
	frame.setSize(500, 500);
	frame.setVisibility(true);
	frame.setLayout(new BorderLayout()) // Se configura el Layout Manager

	// Definicion de dos componentes con tamanio y color
	JPanel panel = new JPanel();
	panel.setPreferredSize(new Dimension(100, 100));
	panel.setBackground(Color.red);

	JPanel panel2 = new JPanel();
	panel2.setPreferredSize(new Dimension(100, 100));
	panel2.setBackground(Color.blue);

	// Se agregan al contenedor principal dandoles una direccion mediante el layout manager
	frame.add(panel, BorderLayout.NORTH);
	frame.add(panel2, BorderLayout.EAST);
}
```