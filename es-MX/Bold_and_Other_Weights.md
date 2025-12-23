---
published: true
layout: bookpage_es-MX
weight: 54
category: workflow
title: Negrita (Bold)
---

Cuando hablamos del estilo "negrita" (bold), en realidad estamos hablando de una variable más amplia, que es el peso. El peso puede incluir cualquier cosa, desde letras "hairline" (pelo) muy, muy finas hasta letras enormemente pesadas. Esta variable se utiliza en la tipografía de texto para crear una fuerte separación entre cuerpos de texto, y se utiliza en el diseño gráfico ya sea para llamar la atención sobre una palabra o texto corto a través del contraste, o para dar al texto un sentimiento específico.

Si bien es posible que desees hacer una amplia gama de cosas con el peso, es probable que tu primera experiencia con el ajuste del peso sea tratar de crear una negrita para acompañar tu peso de texto regular.

Debido a que estás usando FontForge, tienes una ventaja distinta. A diferencia de muchos programas de edición de fuentes, los resultados que obtienes del filtro de estilo de FontForge pueden ser realmente adecuados para su uso &mdash; más que los que obtendrías en software de diseño de tipos comercial. Esto se debe a que el algoritmo que utiliza es excepcionalmente sofisticado.

La creación de una versión en negrita de una fuente se puede aproximar rápidamente ejecutando un filtro llamado <em>Change Weight</em> (Cambiar peso) (que encontrarás en el menú "_**Element**&nbsp;⇨&nbsp;**Styles**&nbsp;⇨&nbsp;**Change&nbsp;Weight**_") para añadir peso a tus glifos.

La naturaleza automática y la velocidad relativamente alta de este proceso lo hacen ideal para probar qué peso puedes desear para tu negrita. Puedes querer intentar ejecutar este filtro varias veces y guardar varias versiones para comparar en texto junto a tu regular. Dicho esto, es posible que aún necesites alterar el resultado más a fondo después de ejecutar el filtro, o ajustar manualmente glifos individuales para obtener un resultado satisfactorio.

También vale la pena recordar que los glifos que no tienen una densidad de trazos (como 1, i, l, I, L, j y J) pueden necesitar ser más pesados, mientras que los glifos que sí tienen una densidad de trazos (como a, e, g, x, B, R, 8 y &amp;) necesitarán ser menos pesados que los otros glifos.

## Interpolación de fuentes

FontForge tiene una función para interpolar entre fuentes separadas (ver "_**Element**&nbsp;⇨&nbsp;**Interpolate&nbsp;Fonts**_"). La interpolación de fuentes es una técnica que se puede utilizar para crear pesos intermedios a partir de otros dos pesos. Por lo tanto, una forma de decidir el peso de tu negrita es crear una negrita que sea definitivamente más pesada de lo que necesitas, y luego interpolar varios pesos diferentes entre este diseño excesivamente negrita y tu regular.

Usando esta técnica puedes encontrar más rápidamente el peso que sientes que es más apropiado para tu proyecto. La misma técnica se puede aplicar para ayudar a decidir sobre pesos aún más pesados como los estilos "heavy" y "black", así como los más ligeros como los estilos "book" y "thin". También puedes establecer valores negativos en la interpolación; por ejemplo, obtendrás un estilo "bold" si interpolas un "regular" con "thin" al -50%.

Por esta lógica, puede parecer que la mejor y más eficiente forma de hacer un peso regular y todos los otros pesos que puedas necesitar, sería hacer una fuente muy fina y una hiper-negrita, y luego generar todo lo que necesitas a partir de ellas. Sin embargo, el resultado de ese enfoque es probable que sea excesivamente soso. En cambio, a menudo es el caso que cada cambio significativo en el peso requerirá su propio diseño maestro a partir del cual se pueden hacer otros pesos medios.

## Tabla de Pesos

Una lista de algunos valores comúnmente utilizados y convenciones de nomenclatura

| Valor | dev.w3.org  | Google     | os2 IBM/Microsoft |
|-------|-------------|------------|-------------------|
| 100   | Thin        | Thin       | Thin              |
| 200   | Extra Light | ExtraLight | Extra-Light       |
| 300   | Light       | Light      | Light             |
| 400   | Normal      | Regular    | Normal            |
| 500   | Medium      | Medium     | Medium            |
| 600   | Semi Bold   | SemiBold   | Semi-Bold         |
| 700   | Bold        | Bold       | Bold              |
| 800   | Extra Bold  | ExtraBold  | Extra-Bold        |
| 900   | Black       | Black      | Black             |

Referencias:
* http://dev.w3.org/csswg/css-fonts/#font-weight-numeric-values
* https://fonts.google.com/noto/specimen/Noto+Sans?preview.layout=grid&stroke=Sans+Serif
* https://learn.microsoft.com/en-us/typography/opentype/spec/os2#usweightclass

## Lecturas adicionales

* [Sobre el peso de la fuente (On Font Weight)](http://bigelowandholmes.typepad.com/bigelow-holmes/2015/07/on-font-weight.html)
* [Nombres comúnmente utilizados para valores de font-weight de CSS](https://gist.github.com/lukaszgrolik/5849599)
