---
published: true
layout: bookpage_es-MX
weight: 75
category: Appendices
title: Importando glifos de otros programas
---

Es posible dibujar glifos en una aplicación de ilustración de propósito general (Inkscape, Adobe Illustrator, etc.) e importarlos como EPS o SVG.

## SVG codificado a mano

### Cómo preparar

* El archivo SVG debe configurarse con `viewBox="0 0 1000 1000"`.

* El ancho en realidad no importa, siempre que sea más ancho que tu glifo. Pero, la altura en 1000 es importante para una importación más fácil.

* `y=0` será la línea ascendente y `y=1000` será la línea descendente.

* (Puede haber algunos glifos que vayan más allá de esas líneas; tal vez FontForge haga lo correcto pero esto no se ha probado).

* Por defecto, FontForge configurará tu línea base en `y=800`. En el sistema de coordenadas de FontForge, la línea base está en su punto `0` en su acceso vertical.

* Para establecer la línea base donde la quieres en FontForge, toma la coordenada y para tu línea base en SVG. Ese será el punto vertical de FontForge para la línea ascendente en su sistema de coordenadas. `1000 - y` para la descendente. Ve a Element > Font Info (Elemento > Información de la Fuente) y en el menú General, coloca el valor de ascendente en la entrada "Ascent" y el descendente en el menú "Descent". Ambos serán positivos. El tamaño Em debe permanecer en 1000 (ya que esa es la altura en unidades SVG).

* Al dibujar el glifo, es común usar coordenadas relativas. Comienza el glifo con `<path d="M Xvalue,Yvalue`. Si el glifo se puede dibujar comenzando en un punto completamente a la izquierda, entonces `Xvalue` será el LeftBearing (margen izquierdo) predeterminado que usa FontForge. Puedes ajustar esto fácilmente después de la importación del glifo (y puede que necesites hacerlo, de todos modos, después de probar la fuente). También es conveniente usar el valor de la línea base para el `Yvalue`.

* Siempre termina el atributo `d` de la ruta con una `z`. Importará sin él, pero sin una `z` después del último punto en la ruta, el glifo no se mostrará correctamente en la ventana principal hasta que reinicies FontForge.

* Al dibujar agujeros (como para la letra P), no inicies un nuevo nodo de ruta, solo usa una `z` al final de la primera ruta y comienza una nueva ruta con `mNewX,NewY` para luego comenzar a dibujar el agujero. Usa el atributo `fill-rule="evenodd"` para la ruta, y funcionará correctamente.

### Flujo de trabajo

Usa un navegador web para renderizar el SVG en el que estás trabajando. Puedes usar un archivo llamado `template.svg` que sea de 1200 por 1200 pero se renderice a 800 por 800 para que no se desplace en la ventana del navegador.

En esa plantilla, dibuja guías en `y=100, y=1100, y=(100 + {lineabase, alturamayúsculas, etc.}, x=100, x=1100`.

Luego importa el glifo SVG en el que estás trabajando en ese documento con `<image xlink:href="LC_p.svg" x="100" y="100" width="1000" height="1000" />`.

Ahora puedes codificar a mano tu letra en una ventana, y actualizar el navegador en la otra para verla dibujada encima de las guías.


## Listas de Glifos Personalizadas

Crea un archivo `namelist.txt`, tal vez usando una hoja de cálculo para enumerar los puntos de código Unicode y los nombres de los glifos. Por ejemplo:

```
0xEC00 octDotDhe
0xEC01 octDotDheDbl
0xEC02 octDotDheTrpl
0xEC03 octDotDheQdrpl
0xEC04 octDotLik
0xEC05 octDotLikDbl
0xEC06 octDotLikTrpl
0xEC07 minirLik
0xEC08 minirDhe
0xEC09 minirBawah
0xEC0A soroganDhe
0x-001 soroganLik
```

Para glifos sin un punto Unicode, usa un punto de código de -1, como en la última línea del ejemplo anterior.

Luego carga FontForge y ve a Encoding > Load NameList (Codificación > Cargar Lista de Nombres), y luego usa 'Rename glyphs' (Renombrar glifos), ya que 'Load NameList' solo agrega la lista de nombres personalizada al conjunto de opciones disponibles en los comandos de renombrado posteriores.
