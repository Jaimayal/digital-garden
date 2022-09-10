---
title: "Mensaje"
date: "2022-09-01 19:46"
tags: 
draft: true
---
Es la forma de comunicacion utilizada en la programacion orientada a objetos. 

Un mensaje ocurre cuando un objeto (llamado objeto activo) le solicita una operacion a otro (llamado objeto pasivo).

En el ejemplo siguiente, el objeto activo 'this' de la clase 'Message' le envia un mensaje al objeto pasivo 'date' de la clase "Date": 

```Java {title="Message.java"}
class Message {
	public static void main(String[] args) {
		Date date = new Date();
		date.parseString("30/09/2002");
	}
}
```
___
