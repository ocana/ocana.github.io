---
layout: post
title: "[Libro] Refactoring - Martin Fowler"
description: "Notas sobre el libro Refactoring de Martin Fowler"
category: articles
tags: [libro, refactoring]
comments: true
share: true
---

Esta semana terminé el libro *[Refactoring: Improving the design of existing code](http://martinfowler.com/books/refactoring.html)* de Martin Fowler y quiero probar este formato de post, fusilado completamente de los que hace [Rubén Chavarría en su blog](http://rchavarria.github.io/readings/), pero no esperéis ni la mitad de lo que consigue él.

## Por qué lo he leído

Era uno de mis miles de "Must Read" pendientes, y de temática transversal, independiente del lenguaje.

Además me apunté a un curso de [Refactoring a Patrones](http://geekshubsacademy.com/courses/refactoring-xavi-gost.html) que usa como base el libro, así que no tenía más excusas.

## Qué esperaba

En realidad ya lo había hojeado en alguna ocasión, pero me pareció que "tampoco era para tanto" al verlo como una recopilación de refactors, quizá un tanto anticuada.

Lo que esperaba de esta lectura en profundidad era descubrir el secreto, mejorar mis habilidades de programación, y alguna ayuda para enfrentarme a código legado.

## Qué encontré

Pues no sólo la evidente colección de refactorizaciones.

Creo que la clave del libro está en que es un libro humilde. 

El autor se basa en la construcción paso a paso y siempre muy metódica de unos ladrillos, al principio muy básicos, pero sobre los que se va apoyando para conseguir los cambios más complejos.

La insistencia en el método permite ser capaces de compilar y pasar tests a cada instante, introduciendo los cambios en paralelo a las soluciones originales.

Cada refactor va acompañado de una motivación, de un problema que quiere resolver, y sin embargo también encontramos siempre el refactor contrario. En ocasiones necesitaremos uno u otro, nunca se nos dice: El diseño debe ser así para ser bueno.

También encontré ayuda para reconocer olores del código.

La parte más decepcionante ha sido no encontrar ayuda para introducir tests en código legado, cuando todos sabemos que es lo más habitual.

## Conclusiones

Además de ser justificadamente un 'Must Read' es un libro al que seguro que volveré cada cierto tiempo.

Tecnológicamente está desactualizado, pero su mensaje es asombrosamente vigente.

Los consejos y puntos claves están escondidos en la lectura en profundidad.

## Qué he aprendido

* Lo básico: Para refactorizar hacen falta tests, y un refactor no modifica el comportamiento observable del código.
* Todo refactor debe hacerse con una intención.
* No "perder el verde", tener siempre la capacidad de compilar y pasar tests en verde.
* No cortar código (prohibido el Ctrl + X).
* No exise un diseño bueno o uno malo, todo depende del problema a solucionar.
* Reconocer más *Smells*.
* Mucha terminología (envidia de características, reemplazar con query, etc...).

## Frases a destacar

* Refactoring means you never have to say you're sorry — you just fix it.
* Any fool can write code that a computer can understand. Good programmers write code that humans can understand.
* Don't let the fear that testing can't catch all bugs stop you from writing the tests that will catch most bugs.

## Tareas pendientes:

* Leer [Working Efectively with Legacy Code](http://www.amazon.es/Working-Effectively-Legacy-Robert-Martin/dp/0131177052) de Michael Feathers, que al parecer habla más del tema de introducir tests en código antiguo.
* ¡Tomarme en serio escribir notas de mis lecturas!

## Enlaces relacionados
* Mis prácticas con [el refactor propuesto en el primer capítulo del libro](http://ocana.github.io/articles/kata-Refactoring-Fowler-Primer-Capitulo/)
* [Serie de posts de Jose Manuel Beas](http://jmbeas.blogspot.com.es/search/label/refactor) sobre el tema. Él lo hizo en el 2008, apenas llego siete años tarde :D
