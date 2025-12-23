---
published: true
layout: bookpage_es-MX
weight: 16
category: Getting To Know FontForge
title: Configuración de FontForge
---

Nota: Este capítulo también puede estar desactualizado y diferir de la última versión de FontForge, pero puede aplicarse a versiones anteriores.

FontForge puede ser ajustado de varias maneras.
Aquí tienes algunos consejos y trucos para hacerlo.
Tienes muchas opciones para optimizar FontForge para tu plataforma y flujo de trabajo.

Por favor [avísanos](https://github.com/fontforge/designwithfontforge.com#how-to-contribute) si tienes algún consejo que quieras compartir.

#### Lo primero es lo primero

Al realizar cualquier cambio de configuración, asegúrate de seguir estos pasos:

1. Sal de FontForge (y de [X11](Glossary.md#X11))
2. Haz los cambios
3. Inicia FontForge y prueba tus cambios

## Windows

Actualmente no tenemos nada específico para la distribución de Windows.
Si se te ocurre algo, [avísanos](https://github.com/fontforge/designwithfontforge.com#how-to-contribute).

## GNU/Linux

Actualmente no tenemos nada específico para ninguna distribución GNU/Linux.
Si se te ocurre algo, [avísanos](https://github.com/fontforge/designwithfontforge.com#how-to-contribute).

## Mac OS X

Para abrir una ruta larga de archivo o carpeta, sigue las siguientes instrucciones:

1. Copia la ruta
2. `⌘ Tab` para cambiar al Finder
3. `⇧⌘G` para abrir el menú Ir&nbsp;&nbsp;→&nbsp;&nbsp;Ir a la carpeta
4. `⌘V` para pegar la ruta
5. `Ir` para abrir una nueva ventana del Finder en esa ubicación

#### Atajos de teclado

Muchos diálogos y elementos de menú tienen una letra s<span class="underline">u</span>brayada.
Se puede acceder a ellos inmediatamente pulsando <kbd>Ctrl</kbd> + <kbd>Alt</kbd> y esa tecla.
Por ejemplo, si un cuadro de diálogo le pregunta si está de acuerdo (<span class="underline">O</span>K), pulse <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>o</kbd>.

Si no utilizas un teclado en inglés de EE.UU., puede que encuentres que algunos de los atajos de teclado son tontos.
O simplemente quieras personalizarlos para que sean como tú esperas.
Para cambiar estas teclas abre y edita el archivo de texto `default`, situado aquí:

```
/Applications/FontForge.app/Contents/Resources/opt/local/share/fontforge/hotkeys/default
```

Cuando instales la próxima versión, todos los archivos dentro de `/Applications/FontForge.app` serán sobrescritos, así que guarda una copia duplicada de tu archivo `default` en otro lugar también.

#### Tamaño de la interfaz de usuario

Si la interfaz de usuario parece demasiado grande o demasiado pequeña, se puede escalar para que se adapte mejor a tu ordenador.
Abre y edita el archivo de texto `resources`, situado aquí:

```
/Applications/FontForge.app/Contents/Resources/opt/local/share/fontforge/pixmaps/resources
```

Añade la línea `Gdraw.ScreenWidthCentimeters: 34` si tu pantalla tiene 34 cm de ancho.
Prueba diferentes valores hasta que estés satisfecho.

#### Marcadores

En el diálogo de archivos hay un botón para `Bookmark Current Dir` (Marcar directorio actual), pero `Remove Bookmark...` (Eliminar marcador) no funciona [#2054](https://github.com/fontforge/fontforge/issues/2054).
Puedes editar la lista manualmente en la sección `FCBookmarks` del archivo `prefs` situado en

```
~/.config/fontforge/prefs
```

Restablece tus marcadores abriendo el Terminal y pegando el siguiente texto en el Terminal:

```
sed -i bak -e 's/^FCBookmarks.*/FCBookmarks:     ~\/Library\/Fonts\/;\/Library\/Fonts\/;\/System\/Library\/Fonts\//g' ~/.config/fontforge/prefs;
```

A continuación, pulsa Intro para ejecutar este comando.
Si no ves ningún error, ha funcionado correctamente.

#### Ratón de 3 botones

FontForge utiliza tres clics de los botones del ratón para algunas funciones extra.
Si no tienes un ratón de tres botones puedes emularlo habilitándolo en las preferencias de X11/Xquartz, en la opción `Emulate three button mouse` de la sección `Input`.

#### Cambiar el icono de X11/XQuartz por el de FF

Si utilizas principalmente [X11](Glossary.md#X11) para FontForge, puedes cambiar su icono. Copia y pega el siguiente texto en el terminal y sigue las instrucciones

```
sudo cp -f /Applications/FontForge.app/Contents/Resources/FontForge.icns /Applications/Utilities/XQuartz.app/Contents/Resources/X11.icns | sudo touch /Applications/Utilities/XQuartz.app
```

#### Gestión de ventanas

FontForge no es una aplicación nativa de Mac, por lo que el manejo de las ventanas puede ser ligeramente "raro", especialmente en sistemas de doble monitor.
Para recuperar el control de las posiciones de las ventanas, utiliza la utilidad gratuita, libre y de código abierto [ShiftIt](https://github.com/fikovnik/ShiftIt) para asignar atajos de teclado para establecer las posiciones de las ventanas.
