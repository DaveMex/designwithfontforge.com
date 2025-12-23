---
published: true
layout: bookpage_es-MX
weight: 9
category: Before You Begin
title: Planificación del proyecto
---

Ahora que tiene una idea de cómo puede variar el diseño de un tipo de letra, quizá quiera decidir si su proyecto tendrá un solo tipo de letra, o si será una colección de varios tipos de letra interrelacionados, o una familia tipográfica (ya tradicional) de tres o cuatro estilos, o quizá algo incluso mayor.

Los estilos más comunes de familias tipográficas son:

* Una Regular y una Negrita
* Regular, Negrita, Cursiva &mdash; eventualmente con Negrita Cursiva
* Thin, Light, Book, Regular, Semi-Bold, Bold, Extra-Bold, Heavy y Black.
* Regular, condensada, negrita y negrita condensada
* Estrecha, Condensada, Ancha y Extraancha
* Regular, Semi-floreada, Floreada, Muy Floreada y Extremadamente Floreada.

Aunque hay razones para que existan patrones típicos en las familias, puede que usted desee un tipo de agrupación muy diferente.

El alcance del proyecto puede venir determinado exclusivamente por su ambición y la cantidad de tiempo libre de que disponga. Pero el alcance del proyecto suele venir determinado por el uso previsto de la colección o familia de fuentes o, incluso más allá, por las necesidades de su cliente. Sin duda, para los diseñadores tipográficos profesionales, estos dos últimos aspectos suelen ser los factores determinantes.

## Sentimiento

Lo más importante de un diseño tipográfico es la sensación que evoca. Es difícil de expresar, pero es lo que hace que un tipo de letra se diferencie de otro.

Un diseñador tipográfico de Portugal, Natanael Gama, diseñó la [familia Exo](https://fonts.google.com/fonts/specimen/Exo) con FontForge.
En su página de inicio describe otro proyecto para el escultor [John Williams](http://ndiscovered.com/john-williams/) e incluye un gráfico que muestra su encargo en una matriz de continuos de sentimientos:

* Figurativo a abstracto: 50%
* Grácil a robusto: 30%
* Tranquilo a enérgico: 0%
* Enigmático a sencillo: 15%
* Experimental a estándar: 15%
* Prestigioso a ordinario: 15%
* Otras ideas: Bello, espacios exteriores, condición humana

## Cobertura de glifos

Un tipo de letra sigue siendo un tipo de letra aunque sólo tenga un glifo. Pero una fuente también puede tener varios cientos o incluso miles de glifos. Si su proyecto es de iniciativa propia, esta elección es, en última instancia, arbitraria. Puede decidir que sólo quiere mayúsculas, o que quiere incluir los glifos que se encuentran en las otras fuentes que utiliza. Si está trabajando para un cliente, puede que quiera aclarar qué idioma o idiomas admite la fuente. Su objetivo también podría ser ampliar una fuente existente, añadiendo algunos glifos para que funcione en una o más lenguas adicionales.

No cabe duda de que es una buena idea hacer esta elección deliberadamente, y pecar de incluir menos en lugar de más. A menudo, cuando se está creando un tipo de letra, puede ser tentador incluir más y más glifos &mdash; pero a menudo es más valioso seguir mejorando el conjunto básico de glifos que añadir otros nuevos.

## Flujo de trabajo de familias de varios estilos

Si sabes desde el principio que vas a tener más de una fuente, ahorrarás tiempo si planificas y construyes la familia tipográfica sistemáticamente, y trabajas en los estilos de alguna manera en paralelo, en lugar de completar un estilo cada vez.


Por supuesto, es imposible crear *todos* los estilos de forma completamente paralela, pero es posible completar un paso de diseño determinado para cada estilo. Esto permite revisar las relaciones entre los estilos al principio del proceso. Puede que le resulte útil completar un conjunto completo de letras de prueba (como “adhesión”) para una versión normal y, a continuación, crear el mismo conjunto de letras de prueba en los demás estilos. Sin embargo, también puede adoptar un enfoque más granular y tomar decisiones sobre partes específicas de las letras base (como la ‘n’ y la ‘o’) para todos los estilos.

Dependiendo del tamaño y la composición de la familia tipográfica que esté planificando, puede que le ahorre tiempo crear instancias de glifos que puedan interpolarse. Esto no sólo le permite interpolar estilos intermedios, sino que también le ayuda a tomar decisiones de diseño sobre las variables tipográficas que cambian entre los miembros de una familia.

Para obtener una visión general de las variables tipográficas que debe tener en cuenta, consulte el capítulo [“¿Qué es una fuente tipográfica?”](What_Is_a_Font.html).

## Técnica: Gestión de versiones

Deberías aprender a usar Git y GitHub para almacenar tus archivos, y usar el formato "SFDir" para tus fuentes.

* [Discusión sobre el uso de Git para gestionar archivos SFDir](https://groups.google.com/forum/#!topic/googlefonts-discuss/CQ-S8Y3ROqc)
* <https://help.github.com/articles/what-are-other-good-resources-for-learning-git-and-github>

## Proceso general

Allá por 2010, Dave Crossland, Eben Sorkin, Claus Eggers Sørensen, Pablo Impallari, Alexei Vanyashin, Dan Rhatigan y otros colaboradores anónimos desarrollaron un diagrama de proceso total para las fuentes latinas:

<img src="images/planning-process.png" width="584" height="1006">

Esto se hizo con Google Drawings y al igual que este sitio está bajo la licencia Creative Commons Attribution-ShareAlike.
La fuente original está disponible [aquí](https://commons.wikimedia.org/wiki/File:Latin_Typeface_Design_Process_Overview.pdf).

Una versión para proyectos no latinos (devanagari) también está disponible [aquí](https://commons.wikimedia.org/wiki/File:Devanagari_Typeface_Design_Process_Overview.pdf).

<!-- Editable versions of the above, with unknown stability, may be found in GitHub PR №225. -->

## Entornos de prueba

Al planificar tu proyecto, debes tener en cuenta los medios previstos para tu tipografía. Algunos ejemplos de medios son las plataformas web y móviles, los proyectores digitales, las impresoras láser y de chorro de burbujas baratas de oficina, las impresoras láser de alta gama de las imprentas, la impresión litográfica offset de revistas y la impresión de periódicos de gran volumen y alta velocidad.

A continuación, debe intentar adquirir o gestionar el acceso a esas tecnologías de composición tipográfica, para poder ver los resultados reales de su trabajo.

A lo largo del proceso de diseño tipográfico, le resultará muy útil previsualizar el texto configurado con su tipo de letra (prototipo) a una resolución superior a la de la pantalla de su ordenador portátil o estación de trabajo. Esto suele significar una impresora láser con 1200 PPP "true" y Adobe PostScript 3. Para particulares es posible adquirir algo así por unos 500 dólares, y algunas recomendaciones de 2013 fueron:

* HP P2055d
* Xerox Phaser 4510
* Xerox Phaser 5550
* Nashua/Ricoh P7026N

En mayo de 2013, el estudio [Production Type](http://productiontype.com) tenía una Xerox 7525 con un controlador "fiery", cuya compra costaba unos 12,000 euros. Se podía alquilar por 300 euros al mes con tóner, piezas y mantenimiento. A finales de 2015, Octavio Pardo alquiló una [Xerox Phaser 7100](https://www.xerox.com/en-us/office/printers/phaser-7100) de forma similar por 30 euros al mes.

## Funciones OpenType

Puedes planificar las características OpenType de tu proyecto antes de empezar a dibujar. Las características comunes incluyen:
* ligaduras `liga`
* numerales `onum`, `lnum`

Para algunos idiomas `locl` funciona pero para otros no, así que es mejor exponer las formas específicas de cada idioma mediante `locl` y `ssNN` o `cvNN`.

La especificación OpenType permite algunos tipos de características que no se recomiendan:
* `hist`. Lea más en esta [discusión sobre TypeDrawers](http://typedrawers.com/discussion/1358/what-are-the-best-practices-for-the-hist-feature-long-s).

## Lecturas Adicionales

* Presentación de Aoife Mooney sobre el proceso de diseño tipográfico en TypeCon 2014: <https://vimeo.com/107421895>
* Discusión en TypeDrawers sobre [Recomendaciones de impresoras para pruebas](http://typedrawers.com/discussion/314/printer-recommendations-for-proofing)
