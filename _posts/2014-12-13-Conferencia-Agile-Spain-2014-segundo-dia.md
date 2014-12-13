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

Una de las metáforas de gestión que utiliza es la gestión del tráfico mediante semáforos o mediante rotondas, haciendo ver que el tráfico es mucho más fluido con rotondas. De hecho en ellas se producen menos accidentes. 

Como pega a la comparación, creo que a Bjarte le faltaba conocer cómo se toman las rotondas en España...

Por último nos contó su experiencia en [Statoil](http://www.statoil.com/en/about/pages/default.aspx) (Compañía energética noruega), y lo que supuso el cambio a un modelo más ágil. 

La compañía expone de manera gratuita [un libro sobre cómo realizan ellos la gestión: The Statoil Book](http://www.statoil.com/en/About/TheStatoilBook/Pages/TheStatoilBook.aspx).

Si queréis más información sobre la charla os recomiendo [este artículo](http://www.managementexchange.com/hack/end-performance-management-we-know-it) y por supuesto [su libro](http://www.amazon.es/Implementing-Beyond-Budgeting-Unlocking-Performance/dp/0470405163).

### Generando tests – [Rafael de Castro](https://twitter.com/rafadc)

En esta charla aprendí algo que me era completamente desconocido, además el título no me decía mucho, así que me llevé una gran sorpresa con todo el provecho que saqué.

Descubrí la existencia y uso de [tests basados en propiedades o post-condiciones, en este caso con Scala](http://www.scalatest.org/user_guide/property_based_testing).

Rafa nos ilustró con un ejemplo sencillo cómo se nos pueden colar cosas no probadas al hacer los test unitarios.

Abundó en la idea lanzada por [José Armesto el día anterior](http://ocana.github.io/articles/Conferencia-Agile-Spain-2014-primer-dia/) de la seguridad que deben aportarnos los tests de los que disponemos.

![Rafa de Castro, Property testing / Piñata bug hunting]({{ site.url }}/images/pinatabug.jpg)

Si nos encontramos con el caso, disponemos de esta técnica, un poco a modo de "Piñata bug hunting", donde probaremos propiedades o postcondiciones que deben ser cumplidas, como por ejemplo que aplicar una operación y después la operación contraria debe dejar el sistema en el estado inicial.

Se nos presentó para ello [ScalaCheck](http://www.scalacheck.org/) con Scala, y otras alternativas como [test.check para clojure](https://github.com/clojure/test.check), o [Rantly para ruby](https://github.com/hayeah/rantly).

Mediante el uso de [Generadores](https://github.com/rickynils/scalacheck/wiki/User-Guide#generators) crean entradas aleatorias para probar las propiedades. Los generadores pueden ser de tipos simples o clases propias. 

Esto hace que no sean test unitarios, ya que no son repetibles, y dependiendo de la prueba pueden ser lentos.

Vimos un ejemplo de postcondición en una aplicación de una tienda donde los productos y el total nunca deben tener valor negativo, y vislumbramos el potencial de estos test al generar comandos aleatoriamente.

Todo esto hace que sean test que van muy bien para ejecutar en la integración continua, o en builds nocturnas.

Por supuesto no sustituye a TDD, Rafa dejó ahí su sutil [crítica a DHH](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html).

Por último la recomendación del libro [ScalaCheck, the definitive guide](http://www.amazon.es/Scalacheck-Definitive-Guide-Rickard-Nilsson/dp/0981531695).

### CQRS y los beneficios surgidos de la necesidad – [Ricardo Borillo](https://twitter.com/borillo)

Ya [está disponible su presentación aquí](https://speakerdeck.com/borillo/cqrs-y-los-beneficios-surgidos-de-la-necesidad).

Fue una exposición muy interesante sobre [el patrón Command Query Responsibility Segregation](http://martinfowler.com/bliki/CQRS.html), sus usos, su combinación con [Event Sourcing](http://msdn.microsoft.com/en-us/library/jj591559.aspx), lo que aporta a la resolución de qué problemas, y sus desventajas.

No es una 'bala de plata', pero viene muy bien en ejemplos como el mostrado, consistente en una web con una tienda típica donde sucede la siguiente situación:

La gente agrega cosas al carrito, en algún momento borra cosas del mismo, y efectúa la compra.

![Ricardo Borillo, CQRS / ES]({{ site.url }}/images/CQRS_ES.png)

CQRS viene al rescate cuando queremos además aprovechar la información de los productos que se borraron de la lista, y explotarla por ejemplo con un sistema de Business Intelligence.

Se puede empezar a usar el patrón simplemente como buena práctica de separación de responsabilidades, separando por un lado los Commands de las Querys, es decir, las peticiones de escritura de las de lectura.

Los commands serán por tanto peticiones que modifican el estado del sistema y que normalmente serán solicitadas por el usuario desde la interfaz.

Las querys no modificarán el sistema, pero servirán por ejemplo para alimentar cuadros de mando que nos den información de lo que pasa.

La combinación con Event Sourcing surge al guardar en nuestro almacen de datos los commands en forma de eventos (o peticiones de modificación), en lugar de almacenar directamente los datos.

Como ventaja añadida, al almacenar las acciones, podremos reconstruir el estado del sistema en cualquier momento del pasado, lo que puede venir muy bien incluso a la hora de reproducir bugs.

La gran 'desventaja', o más bien algo que debemos asumir desde el principio, es la [consistencia eventual](http://en.wikipedia.org/wiki/Eventual_consistency) entre el almacén de eventor y el almacén de datos que por ejemplo alimente a nuestro sistema de BI.

![Ricardo Borillo, CQRS Architecture]({{ site.url }}/images/CQRS.png)

Dependiendo de la solución también puede ser un buen sitio donde usar [Redis](http://redis.io/). Personalmente os dejo [este enlace al podcast de We Developers donde hablan sobre el tema](http://wedevelopers.com/2014/06/01/we-developers-032-redis/), por si queréis profundizar más.

Por último recomendación de teconologías a investigar para el tema, como son [Eventric](http://eventricjs.org/) y bases de datos NoSql como [MongoDB]().

### Delivery at Scale – [Adrian Perreau de Pinninck](https://twitter.com/eidrien), [Manu Cupcic](https://twitter.com/cupcicm)

[La presentación está disponible aquí](http://es.slideshare.net/aperreau/delivery-at-scale).

Habitualmente el coste del cambio aumenta conforme aumenta el número de desarrolladores, sobre todo en aplicaciones grandes con muchos desarrolladores y largos tiempos de compilación.

Nos presentaron su caso sobre una aplicación .Net, y pudimos ver la progresión y evolución del sistema.

Muchos de los problemas que contaban me sonaban muy familiares, ojalá hubiera tenido esta charla en el pasado. 

![Adrian y Manu, Merges disaster]({{ site.url }}/images/mergesDisaster.png)

Os dejo más o menos la progresión que mostraron:

*	Repositorio único y builds cada vez más largas.
*	División en ramas por funcionalidad y problemas de mezclado de código.
*	Validación de la rama principal cada vez en más tiempo, llegando a acumularse o producir bloqueos.
*	Uso de [NuGet](https://www.nuget.org/) para tratar el código como componentes independientes (Para los que no lo conozcan es el equivalente a [Maven](http://maven.apache.org/), pero en .Net).
*	Equipos de gente por componentes.
*	Encontrarse con nuevos problemas, como funcionalidades que afectan a varias cosas, interdependencias, grupos que no actualizaban ciertos componentes.
*	Trunk Based Development y [Branch by abstraction](http://martinfowler.com/bliki/BranchByAbstraction.html). Me quedo con la tarea de aprender más sobre esto.
*	Revisiones de código con [Gerrit](http://en.wikipedia.org/wiki/Gerrit_%28software%29), despliegues en sandbox, comprobaciones automáticas de métricas.

Por lo que nos contaron, la escal del proyecto debía ser ENORME, sin duda un reto brutal, y unas cuantas lecciones aprendidas por si nos encontramos alguna vez en algo parecido.

### Testing en equipos infectados de test – [Juan Gabardini](https://twitter.com/jgabardini)

En principio también iba a participar Juan Diego Vasco Moncada, pero no pudo asistir.

Por mi parte yo también tenía interés en la charla, pero sólo asistí a los primeros veinte minutos, ya que no quise perderme la charla de Pablo Domingo.

En resumen, no puedo contar nada, así que aquí soy yo el que os pide información. Tendré que ver el vídeo si se grabó y en algún momento está disponible.

### Flow Product Development – [Pablo Domingo de La Orden](https://twitter.com/pavleras)

Abandoné el track de Dev Practices and Craftsmanship para ver la charla de Pablo en el track de Delighting Products, al que le debo para empezar el haber podido asistir a las conferencias.

Se enfrentaba a un gran reto ya que apenas contaba con 20 minutos para la exposición, y creo que le fue muy bien, aunque yo no sea muy objetivo.

Si me pedís opinión creo que 20 minutos no son suficientes para una charla, apenas puedes soltar un par de ideas, y las charlas de una hora o más corren mucho peligro de resultar pesadas si no se llevan muy bien.

![Pablo Domingo, Flow Product Development]({{ site.url }}/images/pablo.jpg)

La charla proponía en primer lugar 'Tomar el pulso' a cómo fluía el trabajo, y para ello expuso técnicas de observación del sistema.

Con el análisis de lo captado y basándonos en estudios como la [Teoría de colas](http://en.wikipedia.org/wiki/Queueing_theory), propuso introducir cambios controlados (Si metemos cambios drásticos tendremos que volver a empezar a medir) para mejorar el flujo de trabajo.

Era sorprendente ver con los datos que expuso, cómo una pequeña limitación en el Work in Progress resulta en que el trabajo fluya de otro modo.

Es muy difícil que yo os pueda contar toda la teoría y técnica que hay detrás de esta exposición, pero conociéndole estará encantado de resolver todas las dudas.

Estoy seguro de que también le interesará conocer el feedback de los asistentes, así que si alguno pasa por aquí hacédselo llegar o yo mismo puedo transmitírselo.

### Vis-a-vis de [Cristóbal Colón](https://twitter.com/fageda) y [Pedro Serrahima](https://twitter.com/serrahim) moderado por [Jorge Uriarte](https://twitter.com/jorgeuriarte)

Gran cierre para la CAS 2014.

Cristóbal Colón es el presidente y fundador de La Fageda, os recomiendo encarecidamente que veáis [el programa de Salvados](http://www.lasexta.com/programas/salvados/mejores-momentos/fageda-cuando-negocio-etica-van-mano_2012061100307.html) donde es entrevistado.

Pedro Serrahima es Director ejecutivo de [Pepephone](http://es.wikipedia.org/wiki/Pepephone). Encontraréis un montón de entrevistas e información sobre él y la cultura de Pepephone en internet.

Con lo dicho debería ser suficiente para que viérais la calidad de la discusión, donde se trató el significado de la empresas con Valores y con Principios.

![Cristóbal Colón y Pedro Serrahima, vis-a-vis]({{ site.url }}/images/Fageda_Pepephone.png)

Sólo puedo remitiros al vídeo cuando salga porque es muy difícil decir algo que aporte.

Os dejo también un [enlace a los increibles apuntes visuales](**************) tomados por [Javier Alonso](https://twitter.com/oyabun) y que también incluyen lo acontecido en el vis a vis.

Sé que es alucinante, pero como él mismo pide en Twitter, hacedle caso al contenido y no sólo al increible envoltorio.

### Hasta el año que viene

Por último quiero decir que este recopilatorio de las charlas me ha supuesto un esfuerzo considerable, aunque personalemnte he tenido un beneficio inmediato escribiendo, ya que he reforzado mucho de lo aprendido.

Espero ya de paso que pueda servir como pequeño granito de arena en forma de aportación a la comunidad, animando a los que tenían interés o ayudando a los que no han podido asistir.

Y si a mí me ha costado escribir estos dos post, no quiero ni pensar lo que les habrá costado a los ponentes preparar sólo una de las charlas. 

De verdad que detrás de estos dos días ha habido mucho trabajo, muchas gracias a todos.

Gracias también a toda la organización por traernos todo este conocimiento, y a la ayuda de los voluntarios, que han conseguido coordinar y facilitar esos dos días de forma espectacular.

Bueno, ¡y queda lo mejor! tras este resumen me siento libre para contaros al fin lo verdaderamente importante de la conferencia, los momentos y experiencias vividas, desde un punto de vista mucho más personal. ¡Nos vemos pronto!