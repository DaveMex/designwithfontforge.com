---
published: true
layout: bookpage_es-MX
weight: 69
category: Appendices
title: Cuando las cosas salen mal con FontForge mismo
---

FontForge se desarrolla en GitHub.
El equipo de FontForge utiliza GitHub Issues para discutir problemas, errores e ideas para mejoras, y luego alguien desarrolla una solución y la propone como un _Pull Request_.

NOTA: Los usuarios que buscan consejos generales sobre cómo usar FontForge y otras herramientas, o cómo hacer fuentes, deben usar la [lista de correo de FontForge](https://sourceforge.net/p/fontforge/mailman/fontforge-users/)

Para aprender más sobre GitHub, consulta [Buenos recursos para aprender Git y GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/).

## Pagando por soporte

Esto podría ser una sorpresa, pero es posible y se recomienda pagar por el [soporte](https://www.reddit.com/r/opensource/comments/g5ip5f/is_it_ethical_to_pay_someone_to_develop_a_feature/) de FontForge cuando las cosas salen mal.

Cuando otros editores de fuentes con características completas similares cuestan cientos de dólares estadounidenses, si cada uno de nosotros paga una cantidad similar a los desarrolladores de FontForge para arreglar nuestros errores más molestos, FontForge se volverá cada vez mejor.

Hay varios sitios web que proporcionan recursos para usuarios y partidarios que
están dispuestos e interesados en proporcionar [recompensas](https://en.wikipedia.org/wiki/Bug_bounty_program) (bounties), [premios](https://www.google.com/search?q=bug+bounty+reward), y trabajo [por contrato](https://www.google.com/search?q=open+source+feature+for+hire).

Entonces, ¿cómo harías para hacer esto?

Encuentra un sitio web de buena reputación según las listas sugeridas anteriormente que pueda proporcionar el tipo de servicio que estás buscando. Luego, sigue pasos similares a este (sitio web ahora desaparecido - FreedomSponsors = ¿circa~2012?):

1. Crea un issue en FontForge describiendo lo que quieres que se cambie (ver abajo). Copia la URL del issue al portapapeles.
2. Visita FreedomSponsors y patrocina un nuevo issue, usando la URL que copiaste anteriormente.
3. Vuelve a visitar el issue y agrega un comentario con el enlace a la página del issue de FreedomSponsors, con una nota personal de que estás ofreciendo una recompensa pagada para que se cierre este issue.

NOTA: En lugar de eliminar y reemplazar el sitio web de Freedomsponsor enumerado anteriormente, tenía más sentido dejarlo enumerado arriba como un reconocimiento para ti/nosotros/todos, de que algunos sitios web aparecerán y eventualmente se desvanecerán con el tiempo, por lo que vale la pena tu tiempo elegir un sitio de buena reputación que se espera que permanezca un tiempo.

## Reportar un error (Bug)

1. Visita el [Rastreador de Issues de GitHub de FontForge](https://github.com/fontforge/fontforge/issues) e inicia sesión en GitHub (después de crear una cuenta, si aún no tienes una).
2. En el cuadro de búsqueda de Issues, intenta buscar problemas similares, para ver si el problema que enfrentas ya fue reportado. Si lo fue, y tu problema está relacionado pero no es exactamente el mismo, por favor comenta en ese issue con tu propia versión del problema.
3. Si no fue reportado ya, abre un nuevo issue. Haz clic en el botón verde "New Issue", y luego describe tu pregunta, qué hiciste para provocar un cierre inesperado, o tu idea para una mejora.

Incluye detalles relevantes, tales como:

* tu Sistema Operativo y versión,
* tu versión de FontForge y de dónde la obtuviste,
* **qué sucede, paso a paso, para producir el problema**
* **qué mensajes de error ves,** y
* **qué esperas que suceda**.

Puedes arrastrar y soltar capturas de pantalla u otras imágenes directamente en la página del issue para incluirlas.

Una manera fácil de reportar problemas es grabar un video de screencast en el que expliques con voz en off las cosas que te interesan a medida que suceden, y luego subirlo a YouTube e incluir un enlace a tu video.

Para reproducir el problema, puede ser útil compartir con la comunidad de desarrolladores los archivos con los que estás trabajando.
Si puedes hacer un archivo que sea pequeño y solo contenga lo necesario para reproducir el problema, por favor haz un fork del repositorio de fontforge y agrega estos archivos a [/tests/fonts](https://github.com/fontforge/fontforge/tree/master/tests/fonts) y envía un pull request.
También puedes colocar archivos en tu propio sitio web o en un servicio de intercambio de archivos temporalmente (como MegaUpload, DropBox, Google Drive, etc.).
Finalmente, si no deseas hacer tus archivos públicamente disponibles, puedes proporcionar una dirección de correo electrónico para que un desarrollador de FontForge te contacte para obtener una copia privada del archivo.

Por favor, no cierres los issues de otras personas &mdash; pídeles que cierren el issue si está cerrado a su satisfacción.

## Cómo reportar un cierre inesperado (Crash)

El proceso es el mismo para reportar un cierre inesperado u otros tipos de errores que para nuevas características o preguntas.
¡Enviar un buen informe de cierre inesperado a los desarrolladores de FontForge realmente les ayuda mucho a mejorar la estabilidad del programa para todos!
No te sientas tímido al reportar tales problemas, porque un cierre inesperado que no se reporta es un cierre inesperado que es mucho menos probable que se solucione.

Si encuentras que FontForge se cierra inesperadamente mientras está en uso, crea un issue como se indica arriba.
Si tienes un archivo de fuente particular (SFD, UFO, OTF, TTF, etc.) que desencadena el cierre, puedes subirlo a un nuevo repositorio de GitHub tú mismo (o Dropbox u otra plataforma) e incluir un enlace, o publicar tu correo electrónico y pedir a un desarrollador que te envíe un correo electrónico para obtener una copia en privado.

Con tu descripción, los desarrolladores de software de FontForge intentarán reproducir el cierre inesperado.
Si pueden hacer esto, entonces podrán averiguar dónde está fallando el código y crear una solución.

Después de que se fusione el Pull Request que aborda el problema, necesitarás obtener una versión posterior a esa.
Puedes hacer una de las siguientes cosas:

* recompilar desde el código fuente más reciente de GitHub (ver [Instalación de Fontforge](Installing_Fontforge.html)),
* verificar si hay una compilación diaria disponible (a menudo posible para [Mac OS X](http://fontforge.github.io/en-US/downloads/mac/)), o
* esperar hasta el próximo [lanzamiento](https://github.com/fontforge/fontforge/releases) (promedio de anual).

### Los mejores informes de cierre inesperado

Para ayudar a los desarrolladores a averiguar qué está saliendo mal y __realmente__ entender cómo solucionarlo, puedes hacer un poco más de trabajo para hacer un _backtrace_.
Un backtrace incluye una lista de qué funciones del programa han llamado a qué otras para llegar a donde el programa dejó de funcionar.
Un backtrace es más útil si también contiene los números de línea de las funciones.

Para hacer un backtrace, es posible que debas instalar desde la fuente con _información de depuración_ incluida.
Usa los comandos `type` y `nm` para encontrar la ruta y el estado de tu binario de fontforge.
Ejemplo:

```sh
$ type -all fontforge;
fontforge is /usr/bin/fontforge
$ nm /usr/bin/fontforge;
nm: /usr/bin/fontforge: no symbols
```

En este ejemplo vemos `no symbols` (sin símbolos), por lo que debemos actualizar nuestra instalación para incluir información de depuración.

#### Instalar información de depuración en Fedora

Fedora (y otras distribuciones) ofrecen en el repositorio estándar un comando para instalar fácilmente información de depuración para FontForge.
Ten en cuenta que esto podría requerir cientos de megabytes de descarga si aún no tienes instalados muchos de los paquetes dependientes de debuginfo.
Para instalarlo, ejecuta:

```sh
debuginfo-install fontforge;
```

## Usando el Depurador GNU para reportar cierres inesperados

Un backtrace se genera usando el Depurador del Proyecto GNU, `gdb`.
Puedes adjuntar gdb a un FontForge que ya se está ejecutando, o iniciar FontForge dentro de la sesión de gdb misma.
Aquí hay un ejemplo de lo último:

```
$ gdb fontforge;
GNU gdb (GDB) Fedora (7.3.50.20110722-16.fc16)
Copyright (C) 2011 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.  Type "show copying"
and "show warranty" for details.
This GDB was configured as "x86_64-redhat-linux-gnu".
For bug reporting instructions, please see:
<http://www.gnu.org/software/gdb/bugs/>...
Reading symbols from /usr/local/bin/fontforge...done.
```

Luego, una vez que emites el comando de ejecución al depurador, FontForge se abrirá en la pantalla:

```
(gdb) run
Starting program: /usr/local/bin/fontforge
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib64/libthread_db.so.1".
Copyright (c) 2000-2012 by George Williams.
 Executable based on sources from 14:57 GMT 31-Jul-2012-ML-TtfDb-D.
 Library based on sources from 14:57 GMT 31-Jul-2012.
```

Desde aquí puedes usar FontForge de la manera habitual, pero con la ventaja de poder capturar e informar eficazmente cualquier problema que FontForge pueda tener.

Una diferencia importante que hace ejecutar FontForge dentro de gdb es cómo se hace evidente un cierre inesperado.
Sin gdb, cuando FontForge se cierra inesperadamente, desaparecerá de tu pantalla. Cuando estás ejecutando FontForge dentro de gdb, sin embargo, un FontForge fallido permanecerá abierto junto con sus ventanas e interfaz de usuario.

Si encuentras que tu interfaz no responde, vuelve a la terminal donde ejecutaste gdb y podrías ver algo como `SIGSEGV` en el texto seguido por el aviso `(gdb)`.
Si ves el aviso `(gdb)`, entonces FontForge ya no se está ejecutando.

Ahora puedes (¡finalmente!) usar el comando `bt` para obtener un backtrace, y luego usar el comando `quit` de gdb para salir de gdb y cerrar el FontForge fallido.
Aquí hay un ejemplo:

```
Program received signal SIGSEGV, Segmentation fault.
0x00007ffff74a7c01 in ?? () from /lib/x86_64-linux-gnu/libc.so.

(gdb) bt
#0  0x00007ffff74a7c01 in ?? () from /lib/x86_64-linux-gnu/libc.so.6
#1  0x00007ffff6389a80 in copy (str=0x900000008) at memory.c:82
#2  0x00007ffff7a4aeb5 in KCD_AutoKernAClass (kcd=kcd@entry=0xe80c40, index=2, is_first=is_first@entry=1)
    at kernclass.c:236
#3  0x00007ffff7a51405 in KCD_FinishEdit (g=0xeb0fe0, r=1, c=, wasnew=1) at kernclass.c:2020
#4  0x00007ffff5effe2d in GME_SetValue (gme=gme@entry=0xeb0fe0, g=0xe94760) at gmatrixedit.c:988
#5  0x00007ffff5f00554 in GME_FinishEdit (gme=0xeb0fe0) at gmatrixedit.c:997
#6  0x00007ffff5f01c1a in GMatrixEditGet (g=g@entry=0xeb0fe0, rows=rows@entry=0x7fffffffcf78)
    at gmatrixedit.c:2214
#7  0x00007ffff7a4ea3c in KCD_Expose (event=0x7fffffffd1e0, pixmap=0x83ae00, kcd=0xe80c40)
    at kernclass.c:1446
#8  kcd_e_h (gw=0x83ae00, event=0x7fffffffd1e0) at kernclass.c:1762
#9  0x00007ffff5eabe8f in _GWidget_Container_eh (gw=gw@entry=0xe7f040, event=event@entry=0x7fffffffd1e0)
    at gcontainer.c:269
#10 0x00007ffff5eac385 in _GWidget_TopLevel_eh (event=0x7fffffffd1e0, gw=0xe7f040) at gcontainer.c:734
#11 _GWidget_TopLevel_eh (gw=0xe7f040, event=0x7fffffffd1e0) at gcontainer.c:606
#12 0x00007ffff5ef86ce in GXDrawRequestExpose (gw=0xe7f040, rect=0xef72b0, doclear=)
    at gxdraw.c:2687
#13 0x00007ffff5eea075 in gtextfield_focus (g=0xef72a0, event=0x7fffffffd2e0) at gtextfield.c:1888
#14 0x00007ffff5eaa857 in _GWidget_IndicateFocusGadget (g=0xe94760, mf=mf@entry=mf_normal)
    at gcontainer.c:143
#15 0x00007ffff5eaac97 in GWidgetIndicateFocusGadget (g=) at gcontainer.c:155
#16 0x00007ffff5f02b1e in GME_StrSmallEdit (event=0x7fffffffd670, str=0xe10e60 "A", gme=0xeb0fe0)
    at gmatrixedit.c:890
#17 GMatrixEdit_StartSubGadgets (gme=gme@entry=0xeb0fe0, r=1, c=c@entry=0, event=event@entry=0x7fffffffd670)
    at gmatrixedit.c:1472
#18 0x00007ffff5f03d69 in GMatrixEdit_MouseEvent (event=0x7fffffffd670, gme=0xeb0fe0) at gmatrixedit.c:1499
#19 matrixeditsub_e_h (gw=, event=0x7fffffffd670) at gmatrixedit.c:1735
#20 0x00007ffff5eabd98 in _GWidget_Container_eh (gw=0xeeb2e0, event=0x7fffffffd670) at gcontainer.c:393
#21 0x00007ffff5ef6555 in dispatchEvent (gdisp=gdisp@entry=0x769a50, event=event@entry=0x7fffffffd9b0)
    at gxdraw.c:3475
#22 0x00007ffff5ef7d1e in GXDrawEventLoop (gd=0x769a50) at gxdraw.c:3574
#23 0x00007ffff7ad353a in fontforge_main (argc=, argv=) at startui.c:1196
#24 0x00007ffff736676d in __libc_start_main () from /lib/x86_64-linux-gnu/libc.so.6
#25 0x00000000004006e1 in _start ()
(gdb) quit
A debugging session is active.

       Inferior 1 [process 19196] will be killed.

Quit anyway? (y or n) y
```

Un desarrollador puede ver en este backtrace de ejemplo que FontForge se ha cerrado inesperadamente dentro de la función `copy()`.
La función `copy()` fue llamada a su vez desde la función `KCD_AutoKernAClass`.
El backtrace le dirá a un desarrollador de software las líneas exactas en que se hicieron estas llamadas, y también usará el consejo de que el parámetro pasado a `copy()` era inválido (fuera de límites) para averiguar qué está haciendo mal el código.

Usa el comando quit de gdb en gdb para salir de gdb y cerrar el FontForge fallido.
