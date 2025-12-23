---
published: true
layout: bookpage_es-MX
weight: 82
category: Appendices
title: Historia de las herramientas de edición de fuentes
---

Adam Twardoch ofreció una breve historia de las herramientas de tipografía en la [lista de correo fonttools](https://groups.google.com/d/topic/fonttools/2gghQU7NbZU/discussion) en septiembre de 2017, la cual con permiso se añade a este libro y puede ser editada y ampliada libremente.

En 1975, la compañía con sede en Hamburgo URW publicó Ikarus, el primer sistema computarizado para diseñar fuentes basadas en contornos. Ikarus evolucionó durante bastantes años. Peter van Blokland lo portó al Mac como Ikarus M. El sucesor de URW, URW++ junto con Dutch Type Library continuaron el desarrollo de herramientas basadas en Ikarus bajo la marca DTL FontMaster. Hay algunas aplicaciones muy capaces en el paquete, aunque la interfaz de usuario de algunas puede estar un poco anticuada.

En 1985, Altsys, una compañía con sede en Texas, desarrolló Fontographer, la primera aplicación para Macintosh que permitía dibujar con curvas de Bézier, y el primer editor de fuentes PostScript Type 1. Altsys extendió más tarde Fontographer en Freehand, un editor de gráficos vectoriales completo, luego fue adquirida por Macromedia y más tarde por Adobe.

El desarrollo de Fontographer se estancó durante una década. Porciones del software terminaron como parte de Flash, Freehand fue abandonado pero Fontographer fue vendido a FontLab.

Alrededor de 1990, FontLab se formó como una colaboración entre EE. UU. y Rusia. Desarrolló el editor de fuentes FontLab y algunas otras herramientas (TypeTool, ScanFont, TransType).

También a principios de la década de 1990, Peter van Blokland, Erik van Blokland y Just van Rossum crearon RoboFog, una versión extendida de Fontographer 3.5 que incluía soporte para Python, un lenguaje de scripting creado por el hermano de Just, Guido van Rossum.

Uno de los ingenieros que originalmente creó el formato de fuente TrueType en Apple, y el inventor del lenguaje de hinting de TrueType, Sampo Kaasila, comenzó su propia compañía Type Solutions, más tarde adquirida por Bitstream y finalmente por Monotype. Entre otras cosas, creó TypeMan, una aplicación para hinting de TrueType. La aplicación fue adquirida por Microsoft y extendida por Beat Stamm para convertirse en VTT, la herramienta visual de hinting de TrueType, que está disponible de forma gratuita.

En 2001, FontLab 4.0 añadió soporte para Python, y unos años más tarde el equipo de RoboFog creó una biblioteca de Python llamada RoboFab que permitía ejecutar scripts escritos para RoboFog dentro de FontLab.

Todas estas aplicaciones eran comerciales y se ejecutaban principalmente en Mac OS o Windows.

A finales de la década de 1990, Just van Rossum escribió fontTools/TTX, un kit de herramientas de análisis y manipulación de código abierto en Python puro para fuentes OpenType.

A principios de la década de 2000, un ex-programador de Netscape, George Williams, comenzó a desarrollar FontForge (originalmente bajo un nombre diferente), el primer editor de fuentes GUI de código abierto. Tomó muchas ideas de la interfaz de usuario de FontLab y Fontographer, pero también incluyó muchas ideas originales y también tenía un soporte notablemente completo para varios formatos de fuentes y sus aspectos técnicos. También incluía soporte para Python.

También desde finales de la década de 1990, David Turner y Werner Lemberg han estado desarrollando FreeType, una biblioteca de rasterización de fuentes de código abierto.

También a principios de la década de 2000, Adobe publicó un kit de herramientas basado en C y Python, el AFDKO, que ha sido utilizado por casi todos los editores de fuentes GUI para construir fuentes OpenType con sabor CFF. Originalmente propietario, AFDKO ahora es de código abierto excepto algunas partes.

FontLab publicó FontLab Studio 5 para Mac OS X y Windows, un editor de fuentes GUI que se había utilizado para crear la mayoría de las fuentes OpenType que se envían actualmente. Incluía una interfaz de usuario simplificada para hinting de TrueType inspirada en VTT, soporte para Python y AFDKO y herramientas tanto para diseño de tipos como para trabajo técnico de fuentes.

Adobe también contribuyó recientemente con su código de rasterización y hinting a FreeType, y Werner Lemberg escribió ttfautohint, una herramienta muy capaz para crear instrucciones de hinting TrueType automáticamente.

Desde finales de la década de 2000, el grupo detrás de RoboFog y RoboFab, junto con Tal Leming y Frederik Berlaen, han estado trabajando en UFO, un dialecto XML para describir datos de fuentes fuente, y varias herramientas que se basaban principalmente en RoboFab y fontTools/TTX.

Ese trabajo resultó en más aplicaciones geniales basadas en UFO, principalmente para Mac OS X: Metrics Machine, Prepolator, Superpolator y finalmente RoboFont — un editor de fuentes GUI basado en Python bastante delgado inspirado en partes de Fontographer, RoboFog y FontLab, con un conjunto de características mínimo pero infinitamente extensible con complementos. Muchos de los complementos y bibliotecas subyacentes que impulsan RoboFont, Superpolator y las otras aplicaciones UFO son de código abierto, mientras que las aplicaciones reales son comerciales.

Un proyecto de código abierto notable de la comunidad UFO es la biblioteca MutatorMath de Erik van Blokland y el formato designSpace, ambos ayudando a la interpolación de fuentes y la construcción de fuentes variables. Otras bibliotecas de esta comunidad son defcon (para tratar con proyectos de fuentes basados en UFO en aplicaciones GUI), ufoLib (para tratar con estructuras de archivos UFO), y más recientemente fontParts (un reemplazo para el anticuado RoboFab).

Hace unos años, Adrien Tetar había comenzado a trabajar en TruFont, un editor de código abierto inspirado fuertemente por defcon y RoboFont pero escrito en PyQt, aunque este trabajo se ha estancado.

También hace unos años, un desarrollador alemán Georg Seifert ha comenzado a desarrollar Glyphs, un editor de fuentes GUI para Mac OS X que también es extensible por complementos y bastante popular. También incluye soporte para Python.

FreeType originalmente tenía un soporte mínimo para procesar el modelado (shaping) OpenType (aplicando características al texto para una fuente dada y obteniendo la serie resultante de glifos y sus posiciones) llamado FT Layout. Ese código había sido tomado por los proyectos Qt y Pango y extendido, y más tarde Behdad Esfahbod lo convirtió en HarfBuzz, que ahora es una biblioteca de diseño OpenType de código abierto completa utilizada por muchas aplicaciones y plataformas, incluyendo Firefox, Chrome y Android.

Behdad (que ahora es parte del equipo de i18n de Google) también se hizo cargo del mantenimiento de fontTools/TTX y junto con varios contribuyentes lo extendió enormemente para soportar prácticamente todo OpenType.

El equipo de FontLab ha estado desarrollando durante un tiempo FontLab VI — una reescritura completa del editor de fuentes GUI para macOS y Windows que hace un uso intensivo de muchos de los componentes que han sido creados por la comunidad: Python, RoboFab, fontTools/TTX, AFDKO, UFO, designSpace, HarfBuzz, FreeType, ttfautohint, MutatorMath, y también combina las partes más fuertes de FontLab Studio 5, Fontographer, ScanFont y TransType.

El equipo de i18n de Google ha desarrollado glyphsLib, un analizador de código abierto para el formato de fuente Glyphs, y fontmake que permite la conversión de archivos Glyphs y UFO en fuentes TTF estáticas o variables, utilizando muchos de los componentes de código abierto de la comunidad. El paquete fontTools/TTX se ha extendido para incluir un subconjunto de fuentes, un compilador de características (feaLib) que puede servir como una alternativa a AFDKO, y varLib que ayuda a construir fuentes variables.

También hay una oleada de herramientas y bibliotecas relacionadas con fuentes basadas en JavaScript (opentype.js, fontkit, ufo.js, Metapolator, etc.) pero parece que su desarrollo es algo separado del mundo C/Python.

Esto probablemente omite algunas partes importantes pero con suerte da algo de orientación.

Echa un vistazo a https://twardoch.github.io/fontsurgery-tools/ que incluye enlaces a muchas de las bibliotecas de código abierto.
