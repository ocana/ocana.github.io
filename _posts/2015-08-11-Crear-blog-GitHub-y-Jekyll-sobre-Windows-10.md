---
layout: post
title: "Crear un blog en GitHub y Jekyll sobre Windows 10"
description: "Tutorial para crear un blog en GitHub e instalar en local Jekyll sobre Windows 10"
category: articles
tags: [Blog, Windows 10, GitHub, Jekyll, Markdown]
comments: true
share: true
---

Ya que he instalado *Windows 10* en el equipo de casa y he tenido que reinstalar cosas, aprovecho para hacer un mini-tutorial de puesta en marcha de [Jekyll](http://jekyllrb.com/) en local, el generador de blog y sitios web estáticos basado en [Ruby](https://es.wikipedia.org/wiki/Ruby) y que utilizo para este humilde sitio.

Para los que usáis *Windows 7* o *Windows 8* este tutorial también es válido.

## Un blog en GitHub

[GitHub](https://github.com/) no sólo permite alojar nuestro código fuente, sino que también nos proporciona de forma gratuita:

 * Alojamiento para un sitio asociado a nuestra cuenta de usuario, con el dominio *username.github.io*.
 
 * Alojamiento para un sitio por cada proyecto, de forma ilimitada. 
 
Toda esta gestión de páginas es lo que han tenido a bien llamar [GitHub Pages](https://pages.github.com/).

![GitHub Pages](http://localhost:4000/images/github-pages.png)

Sirva como ejemplo de múltiples sitios este blog, que está alojado en el proyecto asociado a [mi usuario de GitHub: ocana](https://github.com/ocana), dando lugar a *ocana.github.io*, y cuyo código fuente podéis consultar (e incluso modificar o corregir, sois bienvenidos) [aquí](https://github.com/ocana/ocana.github.io).

Por otra parte, tengo [una sección de Katas](http://ocana.github.io/katas/) actualmente acumulando un poco de polvo, donde cada *kata* es un proyecto de *GitHub*, y enlaza con su correspondiente sitio web, generado con la herramienta automática, como cuento más adelante.

Si por ejemplo echáis un vistazo a la [kata de Gilded Rose](http://ocana.github.io/articles/kata-Gilded-Rose/) (muy divertida, os la recomiendo), veréis que enlazo [con la página del proyecto](http://ocana.github.io/GildedRose/), página cuyo código fuente también podéis [consultar en GitHub](https://github.com/ocana/GildedRose/tree/gh-pages).

Una de las ventajas de exponer el código fuente, además de para aplicar el patrón ["Exponer la Ignorancia" del libro Apprenticeship Patterns](http://ocana.github.io/articles/Libro-Apprenticeship-Patterns/), sirve para que cualquiera pueda ayudarme a corregir cosas, pongo como ejemplo un link roto que encontró [Álvaro García](http://alvarogarcia7.github.io/), y aquí [su Pull Request](https://github.com/ocana/ocana.github.io/pull/1) para corregirlo.

## Markdown

Uno de los motivos por el cuál usar GitHub y Jekyll para nuestra web es poder usar Markdown como lenguaje para escribir las entradas. Esta es [la definición de la Wikipedia](https://en.wikipedia.org/wiki/Markdown):

> **Markdown** is a lightweight markup language with plain text formatting syntax designed so that it can be converted to HTML and many other formats using a tool by the same name.
*Markdown* is often used to format readme files, for writing messages in online discussion forums, and to create rich text using a plain text editor.

La verdad es que es un lenguaje muy cómodo que me ayuda a concentrarme en el texto que escribo, sin tener que prestar atención al *HTML* o a si quedará bien.

Una vez asimilada la sintaxis básica nos valdrá cualquier editor de texto para generar nuevas entradas, no necesitamos nada más.

La sintaxis la podéis consultar en [la página web de su creador](http://daringfireball.net/projects/markdown/syntax), [John Gruber](https://en.wikipedia.org/wiki/John_Gruber).

## Creando un sitio asociado a nuestra cuenta

Si el sitio que queremos crear es el sitio principal asociado a nuestra cuenta y no un sitio asociado a un proyecto concreto, lo que deberemos hacer es crear un repositorio con el nombre de nuestro usuario de *GitHub*, del siguiente estilo: *username.github.io*

En mi caso el nombre de usuario es *ocana*, por lo que el nombre del repositorio debe ser: *ocana.github.io*

No puede ser ningún otro, o *GitHub* no se enterará de que debe *compilarlo* para crear una web.

## El generador automático de páginas

Si no queréis nada muy avanzado, la propia web de *GitHub* incluye un [generador/editor automático de páginas](https://help.github.com/articles/creating-pages-with-the-automatic-generator/).

Su uso es muy sencillo, aunque os aconsejo seguir [las instrucciones oficiales](https://help.github.com/articles/creating-pages-with-the-automatic-generator/).

Básicamente se trata de ir a la sección de *Opciones*, darle al botón del generador automático, y nos aparecerá un editor para escribir nuestro artículo:

![Editor GitHub Pages](http://localhost:4000/images/github-editor.png)

El siguiente paso consistirá en elegir un layout de entre los disponibles:

![Layouts GitHub Pages](http://localhost:4000/images/github-layouts.png)

Un click más y ya tendremos nuestra página funcionando.

## Las ventajas de Jekyll en local

El corazón de las *GitHub Pages* es [Jekyll](http://jekyllrb.com/), que como hemos mencionado antes permite hacer fácilmente páginas estáticas y blogs, por lo que instalarlo en nuestra máquina local nos reportará ciertas ventajas, como por ejemplo:

* Utilizar un diseño o tema diferente a los que proporciona *GitHub* por defecto. Hay muchos disponibles en internet, como los de la página [jekyllthemes.org](http://jekyllthemes.org/).

* Realizar cambios en las plantillas para almodarlas a tu web. Por ejemplo yo añadí las sección de *Katas*.

* Previsualizar el aspecto de tus artículos en local antes de subirlos. Lo que permite hacernos una idea de cómo quedarán los textos tras incluir imágenes.

* Editar los textos con nuestro editor favorito. En mi caso utilizo [Notepad++](https://notepad-plus-plus.org/), pero podéis explorar miles de opciones.

Aprovechando la instalación desde cero, he estado probando a editar el blog con *Visual Studio 2015* que, aunque evidentementemente es mucho más pesado, instalando [Web Essentials](http://vswebessentials.com/download) nos da utilidades como el marcado de la sintaxis o permitirnos ver en tiempo real cómo va quedando el diseño. Os dejo una imágen del resultado:

![Editor GitHub Pages](http://localhost:4000/images/blog-vs2015.png)

## Instalando Jekyll en Windows 10

Empiezo con un *disclaimer*, ya que no he inventado nada ni pretendo atribuirme ningún mérito en el tutorial, además es un proceso muy sencillo, pero lo mismo ayudo a que no perdáis tiempo buceando entre la documentación.

Por si os falla algo, os remito a las páginas utilizadas  para la elaboración:

* La sección de *Jekyll* en Windows de la propia página web: [http://jekyllrb.com/docs/windows/](http://jekyllrb.com/docs/windows/).

* El siguiente tutorial, al que también referencia la página anterior: [http://jekyll-windows.juthilo.com/](http://jekyll-windows.juthilo.com/).

### 1 - Instalar Ruby

Vamos al lío, hemos dicho que *Jekyll* funciona sobre [Ruby](https://es.wikipedia.org/wiki/Ruby), por lo que el primer paso es instalarlo en Windows 10.

Descargamos la última versión desde la página web [http://rubyinstaller.org/downloads/](http://rubyinstaller.org/downloads/), en mi caso la versión [Ruby 2.2.2 (x64)](http://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.2.2-x64.exe):

![Instaladores Ruby](http://localhost:4000/images/ruby-installer.png)

Seguimos las instrucciones del instalador marcando la opción de añadir al PATH:

![Instalar Ruby](http://localhost:4000/images/ruby-windows.png)

Una vez completado, instalamos el kit de desarrollo de Ruby desde la misma página. Debemos ser cuidadosos instalando la versión apropiada para la versión de ruby instalada.

![Instalar Ruby Development Kit](http://localhost:4000/images/ruby-devkit.png)

En mi caso es la versión de 64 bits para el uso desde Ruby 2.0 en adelante.

La descarga es un archivo comprimido auto-extraíble, por lo que al ejecutarlo nos pedirá el *path* de extracción. En la web recomiendan dar el nombre de un *path* que no contenga espacios en blanco, por ejemplo:

    C:\RubyDevKit\
	
Una vez extraido iremos a la carpeta que contiene el resultado:

![Carpeta de Ruby Development Kit](http://localhost:4000/images/ruby-devkit-folder.png)

Y con un truco que supongo que todos conoceréis, abrimos una ventana de ejecución de línea de comandos directamente en ese *path* escribiendo *cmd* y pulsando *Enter* en la barra del explorador de ficheros:

![Carpeta de Ruby Development Kit](http://localhost:4000/images/ruby-cmd.png)

Allí ejecutaremos nuestros dos primeros comandos de *Ruby*:

    ruby dk.rb init
    ruby dk.rb install

El resultado debe ser este:

![Carpeta de Ruby Development Kit](http://localhost:4000/images/ruby-cmd-result.png)

¡Y ya tenemos instalado *Ruby* en *Windows 10*!

### 2 - Instalar Jekyll

Con nuestra reciente y flamante instalación de *Ruby* ya podemos instalar *Jekyll*, y por suerte es facilísimo, ya que sólo requiere instalar su [gema](https://en.wikipedia.org/wiki/RubyGems) correspondiente.

Una *gema* no es más que un paquete de software distribuible, si venís del mundo *Microsoft* como yo es lo más parecido a instalar un [paquete de NuGet](https://en.wikipedia.org/wiki/NuGet), o el equivalente a instalar un módulo desde el [npm](https://en.wikipedia.org/wiki/Npm_%28software%29) si usáis node.js.

Pues bien, desde la misma línea de comandos anterior, ejecutamos:

    gem install jekyll

Posiblemente el firewall de windows os pida permiso para que ruby pueda abrir conexiones al exterior, en cuyo caso debemos permitirlo.

Un minuto después tendremos instalado en nuestro ordenador *Jekyll* y todas sus dependencias:

![Jekyll instalado](http://localhost:4000/images/jekyll-installed.png)

### 3 - Instalar un marcador de sintaxis

¡Aún no hemos acabado! Nos falta un pequeño paso, el *syntax higlighter*, y aquí viene un pequeño problema:

Jekyll por defecto viene con [Pygments](https://github.com/tmm1/pygments.rb) como marcador de sintaxis, y éste está basado en [Python](https://es.wikipedia.org/wiki/Python)... ¡otro lenguaje más!

Esto nos obligaría a realizar otra serie de pasos que [vienen en el tutorial original](http://jekyll-windows.juthilo.com/3-syntax-highlighting/) para instalar Python en Windows, después instalar [Pip](https://en.wikipedia.org/wiki/Pip_%28package_manager%29) (otro gestor de paquetes como los mencionados antes, pero esta vez para *Python*), para por último poder instalar *Pygments*.

Durante un tiempo seguí este método pero después tuve problemas debido a la instalación de otra versión de *Python* en local, y acabé explorando otra opción mucho más sencilla: Instalar otro marcador de sintaxis.

En mi caso esta vez instalé [Rouge](https://github.com/jneen/rouge), que es un marcador de sintaxis escrito en *Ruby*, sin delegar en procesos de *Python* ni nada por el estilo, y cuya instalación, al venir también distribuido mediante una *gema*, es tan sencilla como teclear en la linea de comandos:

    gem install rougue

![Instalar Rouge](http://localhost:4000/images/rouge.png)

Ahora sólo queda configurar el marcador de sintaxis en nuestro fichero de configuración del sitio. 

Si hemos descargado un tema por internet, el fichero estará en la raíz y se llamará *_config.yml*, si lo editamos encontraremos (o si no viene la tendremos que añadir) una línea que indica el marcador:

![Configurar highlighter](http://localhost:4000/images/highlighter.png)

Como véis yo he comentado con una almohadilla la línea original que seleccionaba el marcador *Pygments*, y he seleccionado el marcador *Rouge*.

> ¡Importante! A la hora de subir el fichero de configuración a *GitHub* recordar volver a poner *Pygments* como marcador o excluir el fichero en el *commit*. Si no lo hacéis obtendréis un fallo de compilación ya que *GitHub* sólo permite *Pygments*

¡Hora de probar!

### 4 - Iniciando nuestro blog en Jekyll en local

Os recomiendo empezar [descargando un tema de los disponibles en internet](http://jekyllthemes.org/) para partir como base, ya que os proporcionará la estructura de ficheros de todo sitio en *Jekyll*, y es un buen punto de partida para empezar a modificar a nuestro gusto. 

Si os pica la curiosidad, también podéis [descargar desde aquí este blog](https://github.com/ocana/ocana.github.io/archive/master.zip) en un zip directamente a vuestro ordenador para trastear.

La estructura básica, así como la función de algunos archivos como el *_config.yml* del que hablamos anteriormente, se puede [consultar en la web](http://jekyllrb.com/docs/structure/).

Puede que el primer día gastemos bastante tiempo modificando configuraciones para dejarlas a nuestro gusto, pero lo importante, el contenido de la web, se encontrará en la carpeta *_posts*

![Carpeta _posts](http://localhost:4000/images/posts.png)

Crear un nuevo post será tan sencillo como crear un nuevo archivo con extensión *md*, cuyo nombre especificará de forma estática la fecha de publicación y la url de publicación.

Una vez que tengamos algún post, podemos ejecutar por fin el comando para lanzar jekyll en local y ver en el navegador el resultado de nuestro esfuerzo.

Usando el truco que he comentado anteriormente, abrimos una ventana de línea de comandos desde la carpeta raíz donde esté nuestro blog, y ejecutamos el siguiente comando:

    jekyll serve
	
Automáticamente se inicia la compilación del sitio a *HTML*, para los curiosos podéis ver el resultado de la compilación en la carpeta *_site* que se habrá generado en la raíz del blog, y lo más importante, nos indicará que nuestro sitio ya está disponible en la dirección por defecto: http://localhost:4000/

Ya podéis ver el resultado en el navegador, y si dejáis el proceso lanzado en la línea de comandos, cualquier cambio que realicéis en los ficheros (recordad salvarlos) aparecerá automáticamente con sólo refrescar la página.

![Blog en local](http://localhost:4000/images/blog-local.png)

¡Vaya! es mi primer tutorial, y me ha quedado bastante largo, ¡no sabía que tanto! espero no haberos aburrido mucho y que haya valido la pena, si queréis que entre en más detalle en algún punto en concreto admito peticiones, ¡y recordad que si encontráis algún fallo también admito *pull requests*!