---
layout: post
title: "Conferencia Agile Spain 2014. Primer día"
description: "Repaso a la CAS 2014 desde el punto de vista de un programador. Primer día."
category: articles
tags: [eventos, CAS2014, CAS, CAS2K14, agile, craftsmanship, development]
comments: true
share: true
---

Se acabó la [CAS 2014](http://cas2014.agile-spain.org/) y un fantástico puente en Barcelona.

Hay mucho que contar, y para que no me queden entradas muy largas, quiero hacer una primera aproximación aséptica, comentando por encima las conferencias a las que asistí, desde mi perspectiva de informático y programador.

Me dejo para más adelante la reflexión filosófica y contaros todas las emociones vividas.

## Primer día

En el mundo del desarrollo parece ser mucho más conocida la [Codemotion](http://2014.codemotion.es/), que este año contó con más de 2000 asistentes, que la CAS, con más de 500 personas. 

Entiendo que de primeras, una conferencia sobre Agilismo puede tirar bastante para atrás si pensamos que es un evento pensado exclusivamente para la gestión.

Sin embargo el gran acierto de la CAS es precisamente llegar a todo tipo de roles, y dividir las charlas en [tracks específicos](http://cas2014.agile-spain.org/agenda/), que van desde la iniciación a los métodos ágiles, a un track para desarrolladores llamado "Dev Practices and Craftsmanship", del que apenas me despegué.

Cada día tuvo además una keynote de apertura y otra de cierre comunes para todos los asistentes.

Intento dar unas pinceladas de lo visto por si os pica el gusanillo.

### Keynote de apertura: Management 3.0 – [Jurgen Appelo](http://www.jurgenappelo.com/)

Abre la conferencia con una charla para todos los asistentes en la que va desgranando su libro [Management 3.0](http://m30.me/site). 

![Jurgen Appelo, Management 3.0]({{ site.url }}/images/management30.jpg)

Lo bueno de la charla es que, aunque no da tiempo a que profundice mucho en los temas, sí que tuvo en cuenta el público tan variado que tenía, y consiguió dar consejos útiles, sencillos, y que se pueden empezar a poner en marcha desde el día siguiente. Algunos de ellos son: 

*	Hacer 'personal maps' para conocernos más

*	Kudo box

*	Replantearnos los sistemas de 'planes de carrera'

*	Trabajar con los niveles de delegación y los tableros de delegación

*	Consejo para mejorarnos poniéndonos objetivos y midiendo resultados. Si conseguimos entre un 60 y un 70% del resultado podemos sentirnos satisfechos

*	Trabajar la transparencia en las organicaciones con propuestas de asignación de un dinero extra para motivar decidiendo entre todos la asignación proporcional.

Me quedo con la tarea de leer su libro, y otro que mencionó: [Creativity Inc.](http://www.amazon.com/Creativity-Inc-Overcoming-Unseen-Inspiration/dp/0812993012) / [Creatividad S.A.](http://www.amazon.es/Creatividad-S-A-inspiraci%C3%B3n-infinito-CONECTA/dp/8493914525) sobre la creativo en Pixar. Alargo mi ya de por sí larga lista de lecturas pendientes.

### Software Crafstmanship – [Sandro Mancuso](https://twitter.com/sandromancuso)

Este era uno de los platos fuertes para mí. La charla fue un resumen muy rápido de su libro [Software Craftsmanship](https://www.goodreads.com/book/show/18054154-software-craftsmanship), aunque el tiempo se le echó encima. 

Si os interesa el libro os recomiendo [reservar o esperar a la nueva versión](http://www.amazon.com/The-Software-Craftsman-Professionalism-Pragmatism/dp/0134052501) que sale a final de año bajo el ala de las [Robert C. Martin Series de Prentice Hall](http://www.informit.com/imprint/series_detail.aspx?st=61246), no hagáis como yo, que lo compré y leí como una semana antes de que publicara la noticia...

![Sandro mancuso, Software Craftsmanship]({{ site.url }}/images/sandro.jpg)

Me quedo con la reflexión de que la calidad no se puede medir, y con la visión de que [SonarQube](http://www.sonarqube.org/) o la cobertura de código puede convertirse en una pistola en las manos de un niño.

Me hubiera gustado que estuviera frente a frente con los autores de la charla ["Niveles de calidad: el agujero de las metodologías del software"](http://www.javahispano.org/portada/2013/2/19/niveles-de-calidad-el-agujero-en-las-metodologias-de-softwar.html) a la que asistí ojiplático durante [la última Codemotion](http://ocana.github.io/articles/Codemotion-2014/) y que me parecio esperpéntica.

### Unit Testing sucks (and it’s our fault) – [José Armesto](https://twitter.com/fiunchinho)

Charla muy interesante sobre cómo mejorar los tests, consejos útiles y prácticos desde su experiencia, en una progresión en dificultad.

Lo mejor será que [echéis un ojo a las diapositivas que ha puesto disponibles](https://speakerdeck.com/fiunchinho/unit-testing-sucks-dot-dot-dot-and-its-our-fault), pero aun así dejadme contaros con lo que me quedé:

Nos recordó que el código de test es diferente al código habitual, aunque parezca una tontería, y sobre la calidad de los tests que hacemos.

Nos recomendó un gran indicador de que algo falla, y es cuando no nos fiamos o no nos sentimos seguros con los tests que tenemos.

> Esa sensación al fallar un test y pensar.. "Voy a lanzarlo otra vez a ver qué pasa". -- <cite>José Armesto</cite>

![José Armesto, Unit Testing]({{ site.url }}/images/tests_names.png)

Entre las recomendaciones que me apunto: 

* Elegir mejor el nombre de los tests, donde él exponía su propuesta. La tendré en cuenta aunque por ahora me ha ido bien con patrones parecidos a los de BDD, como "When...ItShould..."

* Eliminar lógica de los tests, nada de estructuras de control, de forma que si fallan sepamos el porqué, ya que no nos gusta depurar.

* Tener cuidado al intentar ahorrar escritura o ahorrar duplicidades extrayendo métodos comunes que pueden quitar legibilidad al test.

* Relacionado con lo anterior, explicitar el Set up cuando es importante.

* Uso del patrón builder para evitar tener que arreglar muchos tests por cambiar el constructor de un objeto.

* Si no es caro y no tiene consecuencias, plantearse usar clases reales y no dobles de algunas dependencias.

### Specification by Example. Historia de un equipo que no odia documentar – [Ruben Martín Pozo](https://twitter.com/rmarpozo)

Buena introducción a [BDD](http://en.wikipedia.org/wiki/Behavior-driven_development) contando su experiencia personal. 

Seguro que vino muy bien a los que no conocían [BDD](http://en.wikipedia.org/wiki/Behavior-driven_development), y a los que sí lo conocíamos nos vino bien conocer si los problemas a los que se enfrentó eran los mismos, y sus formas para resolverlos.

Desde el punto de vista personal yo he trabajado con [SpecFlow](http://www.specflow.org/), de la familia [Cucumber](http://cukes.info/), para aplicaciones .NET de escritorio.

![Ruben Martín Pozo, Specification by Example]({{ site.url }}/images/GivenWhenThen.jpg)

Estuvo muy bien conocer [Concordion](http://concordion.org/), que usa HTML, y que también tiene [versión .NET](http://concordion.org/dotnet/index.html).

Lo mejor de la herramienta es poder aprovechar la legibilidad que ofrece HTML, con las posibilidades de unir especificaciones mediante links.

Sin embargo lo que más me gustó fue que aunque enseñara la tecnología, se centrara en los beneficios de la interacción y la comunicación que se crea entre todas las partes, aunque al principio fuera problemático.

De hecho me quedo con el consejo de hacer el esfuerzo de intentar especificar todos los escenarios, pero no volverse loco intentando automatizarlos todos.

### La economía del refactoring. Una visión desde la gestión económica del proyecto – [Xavi Gost](https://twitter.com/xav1uzz)

Para mí el otro gran plato fuerte del día, tenía muchas expectativas tras su charla del año pasado, que comenté recientemente [en este post](ocana.github.io/articles/estado-del-arte/), y no me defraudó.

Es muy difícil perder la sonrisa durante su charla, con referencias a [Fino Filipino](http://finofilipino.org/) o a Chiquito de la Calzada, y sin embargo suele tratar temas bastante profundos y exponer muchas ideas. 

Esta vez todo el tema trataba sobre el refactor. Píldoras e ideas captadas:

*	Su participación en [No flop squad](http://www.noflopsquad.com/) y la iniciativa [devscola](http://www.devscola.com/).

*	Mandarnos tarea: me vuelvo a apuntar para leer con toda la atención posible el libro de [Refactoring del Dios (En palabras de Xavi) Martin Fowler](http://martinfowler.com/books/refactoring.html)

*	La importancia que tiene el refactor, porque no todos trabajamos en proyectos geniales, siempre desde cero, y a la última. Hay veces que toca proyecto-mojón.

> ¿Sabéis a lo que me recuerda a los que les toca un proyecto para trabajar con Legacy code? ¿Habéis visto Papillon? Que les envían a una isla.." -- <cite>Xavi Gost</cite>

*	La necesidad del refactor, porque el sistema "se oxida" y hay que cambiarlo, eso sí, todos esos cambios tienen un coste.

![Xavi Gost, Proyecto mojón]({{ site.url }}/images/mojon.png)

*	El 20% del software soporta el 80% del cambio.

*	Clasificación de los cambios por su alcance en "Cambios Bomba de profundidad", "Cambios Bomba de racimo", etc...

> Si os pasa eso es por ver el software como capas, ¡Por ingenieros! -- <cite>Xavi Gost</cite>

*	Visión del software como rebanadas verticales, más anchas o más estrechas y más altas o más cortas dependiendo de la funcionalidad.

* 	Aplicar la famosa "Regla del Boy Scout" de forma estricta, sólo por donde pasamos. No está justificado hacer cambios fuera de la rebanada.

*	Vender el refactor como un porcentaje de las tareas, un 10% o un 20%. Económicamente va a ir mejor un proyecto subiendo en ese porcentaje las estimaciones de las tareas.

*	Aplicar al refactor técnicas de Pair Programming o incluso Mob programming. Normalmente no se tienen en cuenta para esto, pero son incluso más importantes.

*	Nunca perder "el verde" durante los refactors, meter cambios en paralelo. Esto se convierte en todo un reto sólo apto para los más valientes si automatizas push a master cada treinta segundos. Por supuesto el consejo es amenizar la pérdida del verde con sonidos automáticos tipo MP3 de Chiquito.

> ¡El framework es tu amigo! Perdonad que me ría, es una frase que creía que nunca iba a decir -- <cite>Xavi Gost</cite>

*	Consejo: Usa bien los frameworks, no pongas un framework para luego hackearlo. Tenerlo siempre controlado de forma que se pueda cambiar por otro. Evitar ser "Monos en una nave espacial".

*	Consejo: Encapsular (o enwrappar, como sugería él) todo. El dominio está en las colecciones que no encapsulamos porque tenemos genéricos, también está en los value-Objects o en los controladores. Tenemos que darles entidad encapsulándolos como objetos de primer nivel.

Charla cargadita de contenido, ¿verdad?
	
### Pair Programming – [Pedro Gustavo Torres](https://twitter.com/_pedro_torres)

En esta charla no me entretengo mucho, la verdad es que fue la que menos me gustó del día ya que no aportaba ningún valor a los que ya conocíamos Pair Programming y los hemos practicado, era una primera aproximación introductoria. Flojita.

### Keynote PMI - [Ricardo Triana](https://twitter.com/rtriana)

Bufffff, esta no había por donde pillarla. Hablo por mí mismo, aunque el pulso general me pareció el mismo. 

Este señor será muy importante y representará a un montón enorrrrme de gestores y de gente, pero la charla que dió me aburrió y no aprendí nada. Siendo justos ni siquiera la terminé. 

Y quiero destacar que no tenía ninguna idea preconcebida sobre PMI, de hecho apenas lo conocía, pero como desarrollador no me aportaba nada. 

Lo digo porque buena parte del principio fue dedicada a decir por qué ellos también eran ágiles y no "el demonio".

Y hasta aquí el "Resumen" del primer día, !espero volver pronto con la segunda parte!