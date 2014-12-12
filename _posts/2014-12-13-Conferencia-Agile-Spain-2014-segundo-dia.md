---
layout: post
title: "Conferencia Agile Spain 2014. Segundo día"
description: "Repaso a la CAS 2014 desde el punto de vista de un programador. Segundo día."
category: articles
tags: [eventos, CAS2014, CAS, CAS2K14, agile, craftsmanship, development]
comments: true
share: true
---

Tras [el resumen del primer día](http://ocana.github.io/articles/Conferencia-Agile-Spain-2014-primer-dia/), vuelvo con las charlas en mi segundo día en la [CAS 2014](http://cas2014.agile-spain.org/), contadas desde mi punto de vista como informático y programador.

### Keynote Beyond Budgeting – [Bjarte Bogsnes](https://twitter.com/bbogsnes)

Bjarte abrió el segundo día explicándonos los conceptos de gestión que expone [Beyond Budgeting](http://bbrt.org/about/what-is-beyond-budgeting/).

Nos hizo reflexionar sobre las situaciones absurdas que produce manejar las cosas con presupuestos, como no poder presentar un nuevo proyecto en diciembre por el hecho de ser diciembre, o tener que gastar todo el presupuesto para que no nos asignen menos la próxima vez.

![Bjarte Bogsnes, Traffic lights vs roundabouts](http://www.managementexchange.com/sites/default/files/media/posts/wysiwyg/stat1.png)

Una de las metáforas de gestión que utiliza es la gestión del tráfico mediante semáforos o mediante rotondas, haciendo ver que el tráfico es mucho más fluido con rotondas y que se producen menos accidentes. 

Como pega a la comparación, creo que a Bjarte le faltaba conocer cómo se toman las rotondas en España...

Por último nos contó su experiencia en [Statoil](http://www.statoil.com/en/about/pages/default.aspx) (Compañía energética noruega), y lo que supuso el cambio a un modelo más ágil. 

De hecho la compañía expone de manera gratuita [un libro sobre cómo realizan ellos la gestión: The Statoil Book](http://www.statoil.com/en/About/TheStatoilBook/Pages/TheStatoilBook.aspx).

Si queréis más información sobre la charla os recomiendo [este artículo](http://www.managementexchange.com/hack/end-performance-management-we-know-it) y por supuesto [su libro](http://www.amazon.es/Implementing-Beyond-Budgeting-Unlocking-Performance/dp/0470405163).

### Generando tests – [Rafael de Castro](https://twitter.com/rafadc)

En esta charla aprendí algo que me era completamente desconocido, además el título no me decía mucho, así que me llevé una gran sorpresa con todo el provecho que saqué.

Descubrí la existencia y uso de [tests basados en propiedades o post-condiciones, en este caso con Scala](http://www.scalatest.org/user_guide/property_based_testing).

Rafa nos ilustró con un ejemplo sencillo cómo se nos pueden colar cosas no probadas al hacer los test unitarios.

Abundó en la idea lanzada por [José Armesto el día anterior](http://ocana.github.io/articles/Conferencia-Agile-Spain-2014-primer-dia/) de la seguridad que deben aportarnos los tests de los que disponemos.

![Rafa de Castro, Property testing / Piñata bug hunting]({{ site.url }}/images/management30.jpg)

Si nos encontramos con el caso, disponemos de esta técnica, un poco a modo de "Piñata bug hunting", donde probaremos propiedades o postcondiciones que deben ser cumplidas, como por ejemplo que aplicar una operación y después la operación contraria debe dejar el sistema en el estado inicial.

Se nos presentó para ello [ScalaCheck](http://www.scalacheck.org/) con Scala, y otras alternativas como [test.check para clojure](https://github.com/clojure/test.check), o [Rantly para ruby](https://github.com/hayeah/rantly).

Mediante el uso de [Generadores](https://github.com/rickynils/scalacheck/wiki/User-Guide#generators) crean entradas aleatorias para probar las propiedades. Los generadores pueden ser de tipos simples o clases propias. 

Esto hace que no sean test unitarios, ya que no son repetibles, y dependiendo de la prueba pueden ser lentos.

Vimos un ejemplo de postcondición en una aplicación de una tienda donde los productos y el total nunca deben tener valor negativo.  En el ejemplo se veía su pontencial al generar comandos aleatoriamente.

Todo esto hace que sean test que van muy bien para ejecutar en la integración continua, o en builds nocturnas.

Por supuesto no sustituye a TDD, Rafa dejó ahí su sutil [crítica a DHH](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html).

Por último la recomendación del libro [ScalaCheck, the definitive guide](http://www.amazon.es/Scalacheck-Definitive-Guide-Rickard-Nilsson/dp/0981531695).

### CQRS y los beneficios surgidos de la necesidad – [Ricardo Borillo](https://twitter.com/borillo)

Ya [está disponible su presentación](https://speakerdeck.com/borillo/cqrs-y-los-beneficios-surgidos-de-la-necesidad)

Fue una exposición muy interesante sobre [el patrón Command Query Responsibility Segregation](http://martinfowler.com/bliki/CQRS.html), sus usos, lo que aporta a la resolución de qué problemas, y sus desventajas.

### Delivery at Scale – [Adrian Perreau de Pinninck](https://twitter.com/eidrien), [Manu Cupcic](https://twitter.com/cupcicm)

Habitualmente la capacidad de producción disminuye conforme aumenta el número de desarrolladores, sobre todo en aplicaciones grandes con más de 40 desarrolladores y largos tiempos de compilación

Nos presentaron su caso sobre una aplicación .Net, y pudimos ver la progresión y evolución del sistema.

Muchos de los problemas que contaban me sonaban muy familiares:

*	Builds cada vez más largas.
*	División en ramas por funcionalidad y problemas de mezclado de código.
*	Validación de la rama principal cada vez en más tiempo, llegando a acumularse o producir bloqueos.
*	Implantación de [NuGet](https://www.nuget.org/) para tratar el código como componentes independientes (Para los que no lo conozcan es el equivalente a [Maven](http://maven.apache.org/), pero en .Net).
*	Encontrarse con nuevos problemas, como funcionalidades que afectan a varias cosas, interdependencias, grupos que no actualizaban ciertos componentes.

### Testing en equipos infectados de test – [Juan Gabardini](https://twitter.com/jgabardini)

En principio también iba a participar Juan Diego Vasco Moncada, pero no pudo asistir.

Por mi parte yo también tenía interés en la charla, pero sólo asistí a los primeros veinte minutos, ya que no quise perderme la charla de Pablo Domingo.

En resumen, no puedo contar sobre la charla, así que os pido yo información sobre ella. Tendré que ver el vídeo si en algún momento está disponible.

### Flow Product Development – [Pablo Domingo de La Orden](https://twitter.com/pavleras)

### Vis-a-vis de [Cristóbal Colón](https://twitter.com/fageda) y [Pedro Serrahima](https://twitter.com/serrahim) moderado por [Jorge Uriarte](https://twitter.com/jorgeuriarte)

Gran cierre para la CAS 2014



Por último quiero decir que este recopilatorio de las charlas me ha supuesto un esfuerzo considerable, así que no quiero ni pensar lo que les habrá costado preparar sólo una de ellas a cada uno de los ponentes. De verdad que detras de estos dos días ha habido mucho trabajo, muchas gracias a todos.

Personalemnte he tenido un beneficio inmediato escribiendo, he reforzado mucho de lo aprendido, y ya de paso espero que pueda servir como pequeño granito de arena en forma de aportación a la comunidad, y que anime a los que tenían interés o ayude a los que no han podido asistir.

Bueno, ¡y queda lo mejor! tras este resumen me siento libre para contaros al fin lo verdaderamente importante de la conferencia, los momentos y experiencias vividas, desde un punto de vista mucho más personal. ¡Nos vemos pronto!