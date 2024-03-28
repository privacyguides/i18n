---
title: Traducciones
---

Crowdin posee una buena documentación, y sugerimos consultar la guía de [Inicio Rápido](https://support.crowdin.com/crowdin-intro). Nuestro sitio se encuentra escrito en gran parte en [Markdown](https://en.wikipedia.org/wiki/Markdown), por lo que debe ser fácil contribuir. Esta página contiene algunos consejos útiles para la traducción de algunas sintaxis específicas que puedes encontrar en nuestro sitio.

Por favor, únete a nuestra sala de localización en Matrix ([#pg-i18n:aragon. h](https://matrix.to/#/%23pg-i18n:aragon.sh)) si tienes alguna pregunta adicional, y lee nuestra [publicación del blog](https://blog.privacyguides.org/2023/02/26/i18n-announcement) para obtener información adicional sobre el proyecto.

Tome en cuenta que la versión en Inglés del sitio es la versión primaria, lo que significa que los cambios se producen primero en esta. Si nota que un lenguaje está rezagado detrás de la versión en Inglés, por favor colabore. No podemos garantizar la exactitud de todas nuestras traducciones. Si tiene una sugerencia sobre contenido específico de su región, por favor abra un issue o pull request en nuestro [repositorio principal](https://github.com/privacyguides/privacyguides.org).

## Resultado de la traducción

El programa de traducción obtiene la traducción con mucha precisión; sin embargo, debes asegurarte que la cadena traducida es correcta.

Por ejemplo:

```text
![Software logo](assets/img/path/to/image.svg){ align=right }
```

Algunas veces encontramos que en la sintaxis para insertar una imagen, como se mostró previamente, falta el `![` o un espacio extra es ubicado entre el texto y la ruta, ej: `](`. Si una cadena de traducción no es correcta, te solicitamos **eliminarla** presionando el ícono del basurero [o votando](https://support.crowdin.com/enterprise/getting-started-for-volunteers/#voting-view) por la que consideres correcta. Cuando una cadena de texto no válida es eliminada, esta es removida de la [memoria de traducción](https://support.crowdin.com/enterprise/translation-memory) de la organización, lo que significa que cuando una cadena de código es vista nuevamente, esta no sugiere la traducción incorrecta.

## Puntuación

Para ejemplos como el anterior de los avisos, las comillas (por ejemplo, `" "`) deben ser utilizadas para especificar una cadena de texto. McDocs no interpreta correctamente otros símbolos como `「 」` o `« »`. Otros signos de puntuación sirven para marcar citas regulaes dentro del texto.

## Alternativas de ancho completo y sintaxis de Markdown

Los sistemas de escritura CJK tienden a utilizar variantes alternativas de "ancho completo" de símbolos comunes. Estos son caracteres diferentes y no pueden ser utilizados para la sintaxis de Markdown.

- Los enlaces deben usar paréntesis regulares como `(` (paréntesis izquierdo U+0028) y `)` (paréntesis derecho U+0029) y no ` (` (paréntesis izquierdo de ancho completo U+FF08) o `) ` (paréntesis derecho de ancho completo U+FF09)
- El texto indentado debe utilizar `:` (dos puntos U+003A) y no `：` (dos puntos de ancho completo U+FF1A)
- Las imágenes deben utilizar `!` (signo de exclamación U+0021) y no `! ` (signo de exclamación de ancho completoU+FF01)
