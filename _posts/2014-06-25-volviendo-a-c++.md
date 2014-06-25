---
layout: post
title: Volviendo a C++
description: "Volviendo a C++"
category: articles
tags: [C++, personal]
comments: true
share: true
---

Para los que no me conocen llevo ya unos 6 años programando en C#, así que seguro que más de uno se sorprende al ver que lo primero que he subido a GitHub es código en C++. 

###Una pequeña explicación

No hace mucho leí [The Pragmatic Programmer](http://pragprog.com/the-pragmatic-programmer) y con una de las cosas que me quedé es con la sugerencia de aprender al menos un lenguaje de programación cada año, aunque me gusta más el matíz que da [Martin Fowler sobre el tema](http://martinfowler.com/bliki/OneLanguage.html).

El caso es que hablando sobre las ventajas multiplataforma de los lenguajes *"menos abstractos"* o *"más cercanos a la máquina"* y sobre el desarrollo para móviles, me picó el gusanillo sobre volver a C++, recordar los tiempos del manejo de punteros, etc... y ver hasta donde podía llegar.

> Tienes más óxido encima que una moto de la Segunda Guerra Mundial -- <cite>[Alberto Chicote](https://twitter.com/frasesdechicote/status/347832596572565504)</cite>

Tengo que decir que la experiencia está resultando gratificante y dura a partes iguales. 
Lo más duro está siendo volver a [problemas que creía olvidados](http://stackoverflow.com/questions/895827/what-is-the-difference-between-tmain-and-main-in-c), desde conocer si la arquitectura de la máquina donde se va a ejecutar la aplicación es [Little Endian o Big Endian](http://es.wikipedia.org/wiki/Endianness), hasta cosas tan tontas como tener que declarar las funciones antes que usarlas, o recordar que [el tamaño de los enteros depende de lo que decida el compilador](http://stackoverflow.com/questions/2331751/does-the-size-of-an-int-depend-on-the-compiler-and-or-processor), normalmente basándose en la arquitectura en la que compila.

<figure>
	<img src="http://i.imgur.com/yQIp5tt.gif">
	<figcaption>Yo volviendo a programar en C++.</figcaption>
</figure>

Más tarde intenté volver a compilar los fuentes de la entrega final de mis prácticas de programación de informática gráfica, desarrollada en C++ y usando OpenGL, y fue un auténtico dolor ya no sólo ver el código escrito en castellano ( ¡En castellano! ) sino constatar que el código está completamente acoplado a Borland C++, y a sus librerías gráficas para creación de ventanas. 

> ¡Venga muévete! ¡Aunque sea para hacerlo mal! -- <cite>[Alberto Chicote](https://twitter.com/frasesdechicote/status/337681212086824960)</cite>

Intenté compilarlo con la última versión del software de [Embarcadero](https://www.embarcadero.com/es/products/cbuilder) que al parecer compró a Borland en 2008, pero por ahora no ha habido manera, me lo planteo como reto más adelante.

###Resultado
<figure>
	<img src="http://brianoverland.com/wp-content/uploads/2013/07/book3.jpg">
	<figcaption>For the impatient, pero 700 páginas el tocho.</figcaption>
</figure>{: .pull-right}

Tras la cura de humildad, fui directo a Internet a buscar un buen libro que me sirviera para ponerme al día, y tras ver unas cuantas opiniones me hice con [C++ for the Impatient](http://brianoverland.com/books/), y ahí estoy, pasito a pasito, desoxidándome y aprendiendo las novedades de C++11 mientras realizo ejercicios que subiré los voy considerando interesantes.

Espero poder escribir próximamente un poco más sobre las características nuevas de C++11 y la práctica del Quicksort.