---
layout: post
title: "Consejos certificación MongoDB"
description: "Consejos por si estás pensando en certificarte en MongoDB"
category: articles
tags: [certificacion, examen, MongoDB]
comments: true
share: true
---

**Actualización**: ¡He aprobado! Supongo que ahora ya os podéis creer un poco más los consejos :D

**Exención de responsabilidad**: Estos consejos deben ser tomados con precaución, ya que cuando me presenté por primera vez el año pasado suspendí, y aún no conozco el resultado del examen que realicé la semana pasada ¡No las tengo todas conmigo!

## Cómo llegué a MongoDB

Primero un poco de historia personal sobre cómo llegué yo, desarrollador de C# actualmente trabajando con aplicaciones de escritorio, a conocer MongoDB e intentar certificarme.

En realidad es muy sencillo, llevaba tiempo oyendo hablar de las bases de datos NoSQL, pero sin tener claro cómo funcionaban, ni qué era eso de una base de datos documental. 

La mejor forma que encontré de despejar todas las incógnitas fue apuntarme a los [cursos online gratuitos que ofrecía MongoDB en su web](https://university.mongodb.com/).

Podría haber sido cualquier otra, pero creo que es de las más conocidas. Forma parte del llamado *[stack MEAN](http://en.wikipedia.org/wiki/MEAN)*, y el curso gratuito, de siete semanas de duración, resultó decisorio en la elección.

![MEAN stack]({{ site.url }}/images/mean.png)

Además no había versión en .Net, así que pensé que sería una buena ocasión para desempolvar mis habilidades javeras.

Por cierto, ¡acabo de descubrir en la web que en Marzo habrá una primera [edición en .Net](https://university.mongodb.com/courses/M101N/about)!

Bueno, puestos en situación, el curso resultó ameno y muy facilito, así que me interesé por la certificación.

## ¡Es una trampa!

Al apuntarte al curso, en la descripción de los objetivos pone:

> After completing this course, you should have a good understanding as to how applications are built on top of MongoDB using the .NET framework. This course should also prepare you to take the C100DEV: MongoDB Certified Developer, Associate Level exam. Register for next exam session to become a MongoDB Certified Professional.

Bien, siguiente paso, ver los requisitos del examen:

> There are no prerequisites. Anyone may take the exam but we do recommend you take M101J, M101JS, or M101P in preparation and achieve familiarity with the MongoDB Documentation.

Vale, ahora el nivel:

> The MongoDB Certified Developer, Associate Level exam is intended for individuals with knowledge of the fundamentals of designing and building applications using MongoDB. We recommend this certification for software engineers that know the basics, but may not yet have substantial professional experience developing applications with MongoDB.

Iluso de mí, el año pasado me lo creí.

Y eso que antes de lanzarme a la piscina, me aseguré de repetir el curso en las ediciones en Python y Node.js, para aprender algo por el camino y que no se me hiciera aburrido.

![It's a trap!]({{ site.url }}/images/trap.png)

Entonces, ¿el curso te prepara para la certificación?

No.  :D

Como ya sabéis, suspendí.

Lo cierto es que por poco, viendo los resultados y haciendo unos pocos cálculos, ví que había que acertar como el 70% de las preguntas y acerté el 66%. Además me quedé sin tiempo en el final.

Así que bueno, seguro que muchos de vosotros sólo con el curso lo conseguiríais, sólo digo que yo no, y que me ha supuesto un esfuerzo bastante mayor al esperado la preparación de este intento, así que si estáis con dudas quizá podáis ahorraros el desembolso.

Por suerte tuve acceso a un segundo intento gratuito, que por cierto ya no existe.

## Preparación básica: Consiguiendo fluidez

Si aun así decidís continuar, os cuento lo que creo que en realidad es necesario para aprobar, a falta de ver si lo consigo.

Aunque el curso es una buena introducción para aprender a usar MongoDB, debemos tener fluidez en todo lo que se expone, y en la última versión del sistema.

En el primer examen recuerdo preguntas de agregación que me llevaron mucho tiempo. Conocía los conceptos pero tardaba en hacerlo.

Esta segunda vez han sido 66 preguntas en 90 minutos. Esto es algo menos de minuto y medio por pregunta.

En esta ocasión todas las preguntas fueron de elección (simple o múltiple) de la respuesta, no me tocó ninguna de rellenar. No sé si se lo han replanteado porque eran difíciles de corregir o sólo es que me tocó de esta forma, pero esta vez me sobró algo de tiempo.

## No hay pregunta fácil

La fluidez se puede conseguir con un poco de práctica con el curso, pero el siguiente paso es conocer los recovecos.

Tened en cuenta que no hay "preguntas regalo", todas tienen algo.

No son preguntas para ver si conoces un concepto, como por ejemplo crear un índice, sino que son preguntas "para pillar", casi siempre pensadas en las excepciones a las normas, o en las cosas menos comunes.

Creo que ya os podéis ir dando cuenta de un patrón que creo que es la clave para el examen: 

Hay que pasar bastante tiempo por [la web de la documentación](http://docs.mongodb.org/manual/).

## Conoce la última versión del producto

Uno de los recursos que vienen recomendados para el examen es el libro [MongoDB: The definitive guide](http://www.amazon.es/MongoDB-Definitive-Guide-Kristina-Chodorow/dp/1449344682) segunda edición.

Lo compré, lo estudié pasando por encima por la última parte (más centrada en la administración) y la verdad, aun estando muy bien, se nota que ha quedado anticuado ya para la versión 2.6 de MongoDB. 

Por cierto, noticia de esta misma semana, han decidido que los cambios que van a meter en la siguiente versión son suficientes para [renombrarla de 2.8 a versión 3.0](http://www.mongodb.com/blog/post/renaming-our-upcoming-release-mongodb-30).

O sacan una tercera edición o yo personalmente no recomiendo el libro, ya que además hay preguntas que se centran únicamente en las novedades.

Un ejemplo:

> Pregunta: ¿Que valor es devuelto como resultado de una agregación? Respuesta: Un cursor a los resultados.

Si miramos en [la documentación](http://docs.mongodb.org/manual/reference/method/db.collection.aggregate/):

> Changed in version 2.6: The db.collection.aggregate() method returns a cursor and can return result sets of any size. Previous versions returned all results in a single document, and the result set was subject to a size limit of 16 megabytes.

Otro:

> Pregunta: Al usar el framework de agregación, ¿cómo evitamos que se realicen ordenaciones en memoria? Respuesta: Con la opción allowDiskUse

Si miramos en [la documentación](http://docs.mongodb.org/manual/reference/command/aggregate/)

> allowDiskUse. Boolean. Optional. Enables writing to temporary files. When set to true, aggregation stages can write data to the _tmp subdirectory in the dbPath directory. New in version 2.6

Dejadme insistiros en el uso de la documentación.

Yo me dí cuenta algo tarde incluso esta segunda vez.

## Desarrollo del examen

El examen se puede hacer a cualquier hora o día durante la semana disponible.

Es necesario hacer una reserva previa, con un mínimo de 24 horas de antelación, ya que durante ese tiempo tendrás a alguien observando que se cumplen las normas.

Una vez hecha la reserva no podrás acceder hasta un cuarto de hora antes de la hora reservada. 

Eso sí, puedes modificarla o cancelarla en cualquier momento.

Tendrán acceso a tu webcam y micrófono durante todo el examen, y control compartido de lo que sucede en la pantalla de tu PC.

No recuerdo si aceptas que se grabe la sesión, la verdad.

![Yo durante un examen]({{ site.url }}/images/examen.jpg)

Recomiendo conocimientos de inglés, no sólo porque es el idioma del examen y hay que entender lo que preguntan, sino porque tendréis que seguir los pasos que os indique la persona que os vigila.

No penséis en nada difícil, son tan sencillos como mostrarle la mesa donde tienes el ordenador, o mostrarle lo que tienes alrededor en la habitación.

Por lo menos que no os pille de sorpresa.

También debes tener a mano para mostrar cuando te lo pidan un documento acreditativo con tu foto (DNI, pasaporte, carné de conducir...).

Lo mejor es que lo puedes hacer en tu propia casa, pero debe ser una sala donde estés solo, sin móvil, sin material, sin interrupciones y sin salir durante la duración del mismo.

El día que tengas pensado hacerlo resérvate dos horas de tu tiempo por si acaso, ya que el examen son 90 minutos, pero el chequeo previo se lleva unos 10-15 minutos más.

En el PC sólo podras tener abierto un navegador con la web del examen.

En definitiva, un examen de verdad.

Y nada más, si váis a intentarlo, sólo me queda desearos suerte.

## Resumen de los recursos

* [Cursos online gratuitos](https://university.mongodb.com/).
* [Web de la documentación](http://docs.mongodb.org/manual/).
* [Sesión de estudio grabada](http://youtu.be/oS3rKWfOy2k). La versión en español la dió [Norberto](https://twitter.com/nleite), que como Technical Evangelist supongo que intentará responder a nuestras dudas técnicas en castellano. [@nleite](https://twitter.com/nleite).
* Blog con ejemplos de preguntas y respuestas (son para la edición de DBAs, pero válidas igualmente): [Parte 1](http://blog.cloudthat.in/sample-questions-for-mongodb-certified-dba-c100dba-exam/), [Parte 2](http://blog.cloudthat.in/sample-questions-for-mongodb-certified-dba-c100dba-exam-part-ii/). Ojo a los comentarios de las entradas porque el autor tiene algún fallo.
* Libro [MongoDB: The definitive guide](http://www.amazon.es/MongoDB-Definitive-Guide-Kristina-Chodorow/dp/1449344682).

Espero haber podido ayudar, y si puedo resolver alguna duda más, no dudéis en preguntar.
