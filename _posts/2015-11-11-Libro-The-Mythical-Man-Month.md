---
layout: post
title: "[Libro] The Mythical Man-Month"
description: "Notas sobre el libro The Mythical Man-Month: Essays on Software Engineering, un clásico básico"
category: articles
tags: [libro, Mythical, Man-Month]
comments: true
share: true
---

Volvemos al sabor añejo con uno de los grandes clásicos de la literatura alrededor del desarrollo de software, de manos de [Fred Brooks](https://en.wikipedia.org/wiki/Fred_Brooks), que entre otros galardones consiguió el [Premio Turing](https://en.wikipedia.org/wiki/Turing_Award) en 1999, y que también es conocido por su famosa [*Ley de Brooks*](https://es.wikipedia.org/wiki/Ley_de_Brooks):

> Adding manpower to a late software project makes it later.

## Por qué lo he leído

Porque es otro de los libros considerados *must read* que llevaba largo tiempo pendiente en [mi lista de lectura](http://goodreads.com/miguelocana), y porque otra vez estamos ante un libro de los que suele salir en las conversaciones sobre la profesión.

## Qué esperaba

No sabía muy bien qué esperar después de haberme sentido decepcionado por [Peopleware: Productive Projects and Teams](http://ocana.github.io/articles/Libro-Peopleware/), que es considerado otro de los *grandes clásicos*, así que quise acercarme al texto sin ideas preconcebidas.

## Qué encontré

Esta vez he encontrado un libro que para mi sorpresa fue escrito en 1975. 

Dejadme que lo repita: **1975**.

Compré la edición actualizada y revisada por el veinte aniversario, así que sabía que por lo menos tenía veinte años a sus espaldas, pero me sorprendió descubrir que habían pasado otros veinte años más desde entonces.

<p align="center">
  <img src='{{ site.url }}/images/man-month.jpg' alt='Tar Pits' />
</p>

*¿Y puede ser interesante en la actualidad un libro sobre software escrito hace cuarenta años?*

Claro que sí, ¡y no sólo interesante sino también actual!

Exactamente igual que cuando lees un buen clásico de ciencia ficción y compruebas que muchas predicciones se cumplen, podemos comprobar que las soluciones que tenemos ahora son evolución de las ideas que planteó entonces, y que los verdaderos problemas del desarrollo de software apenas han variado.

<p align="center">
  <img src='{{ site.url }}/images/dilbert-man-month.jpg' alt='Dilbert Man-Month' />
</p>

Os cuento algunas de esas ideas:

* Podemos leer cómo el autor detecta la necesidad de roles con una visión general del producto, que sepan equilibrar la simplicidad con el número de carácterísticas. Germen de la actual figura de [*Product Owner*](https://en.wikipedia.org/wiki/Scrum_%28software_development%29#Product_owner).

* Expone la necesidad de alinear estilos y objetivos entre las personas y los equipos, siempre mediante la comunicación, por lo que me gustaría saber su opinión de herramientas de estilo como [*StyleCop*](https://en.wikipedia.org/wiki/StyleCop), [*ReSharper*](https://www.jetbrains.com/resharper/), o herramientas de análisis de código estático como [*SonarQube*](http://www.sonarqube.org/).

* Cree firmemente en la figura de arquitecto, unos o varios, que den las directrices para el desarrollo. En el caso de que haya necesidad de varios propone reuniones de arquitectura periódicas para alinear visiones. Aunque probablemente el punto en el que más discrepo con él sea este rol de arquitecto, entiendo perfectamente el contexto en el que escribe, que es ni más ni menos que el desarrollo de un sistema operativo, donde la sincronización debe ser máxima.

* Se fija en otras industrias como la química donde se utilizan las [Pilot Plants](https://en.wikipedia.org/wiki/Pilot_plant) para conocer cómo se comporta el producto a una escala reducida antes de construir una versión más grande. Detrás de esta idea están los conceptos del fallo temprano y el desarrollo de [*MVPs*](https://en.wikipedia.org/wiki/Minimum_viable_product).

* Habla de programas auto-documentados y es inevitable que nos vengan a la mente herramientas como [Swagger](http://swagger.io/).

* Pone en cuestión la utilidad de cierta documentación como los diagramas de flujo.

<p align="center">
  <img src='{{ site.url }}/images/dilbert-man-month2.jpg' alt='Dilbert Man-Month' />
</p>

Por otra parte, el libro también dedica parte a explicar las dificultades del trabajo con las personas y lo que suponen los cambios en las organizaciones. Me arriesgo a decir que sus preocupaciones son la semilla de los principios y valores ágiles.

Valgan como ejemplo las siguientes ideas que encontraremos:

* Mentores para hacer crecer buenos programadores.

* No sólo debemos planear el código para adaptarse al cambio, sino planear la organización para el cambio.

* La necesidad de cambiar las estructuras de gestión.

* Necesidad de equipos multidisciplinares

* Dificultad del cambio: las barreras sociológicas, la pérdida de prestigio, incluso habla del problema de poner *job titles*.

Por último quiero comentar un poco los cambios introducidos en esta edición del veinte aniversario.

En los capítulos extra se expone a varias de las críticas que recibió el texto con el tiempo, y hace una reflexión sobre las diferentes innovaciones que han ido surgiendo con respecto a sus predicciones, como la importancia que cobran las interfaces gráficas, el fracaso de Waterfall y su visión hacia algo más iterativo, las técnicas de pruebas con objetos falsos, o la anécdota de James mcCarthy, por entonces trabajado en Microsoft, describiéndole las build nocturnas y la integración continúa.

También dedica tiempo a analizar los sorprendentes cambios que se produjeron realmente en el mercado, como la sorpresa de los microcomputadores, o el panorama de las *startups*. 

Sólo nos queda imaginar la sorpresa que se habrá llevado en estos últimos veinte años con el espectacular crecimiento de los móviles, o las redes sociales.

## Conclusiones

Seguramente influido por la contención de mis espectativas, he disfrutado mucho más de la lectura de éste que del mencionado [Peopleware](http://ocana.github.io/articles/Libro-Peopleware/).

El libro es un viaje al pasado del desarrollo de software, y una invitación a la reflexión.

Si queréis entender la raíz de los problemas de nuestra profesión y acercaros a la situación habitual a la época este es vuestro libro.

Resulta muy divertido leerle escribir predicciones sobre [Ada](https://es.wikipedia.org/wiki/Ada_%28lenguaje_de_programaci%C3%B3n%29), la programación orientada a objetos, la inteligencia artificial, o la verificación de programas y el testing.

Sólo puedo terminar diciendo que me encantaría una nueva revisión del texto con sus opiniones cuarenta años después, con todo el panorama actual del agilismo, con técnicas nuevas como [*BDD*](https://en.wikipedia.org/wiki/Behavior-driven_development) para los problemas relacionados con la documentación útil, la colaboración a comunidades de software libre con técnicas como los Pull Request, etc.

## Qué he aprendido

* He aprendido sobre el autor, que para mí era un desconocido hasta la lectura de su libro.

* He aprendido a plantearme cómo será de válido lo que conozco hoy dentro de veinte años.

* He aprendido que las limitaciones tecnológicas a las que se ha ido enfrentando nuestra profesión han sido fácilmente solventadas hasta ahora gracias al rápido avance de la tecnología, no así los problemas inherentes a las personas.

* Me quedo con la comparación de cocinar una tortilla en comparación a un desarrollo que va tarde: Puedes gastar el tiempo necesario para que la tortilla quede bien hecha, apagar el fuego y servirla cruda, o aumentar el fuego y que se queme.

## Frases a destacar

* A good workman is known by his tools.

* Adding manpower to a late software project makes it later.

* I think the most important single effort we can mount is to develop ways to grow great designers. 
No software organization can ignore this challenge. Good managers, scarce though they be, are no scarcer than good designers. Great designers and great managers are both very rare.

* The only constancy is change itself.