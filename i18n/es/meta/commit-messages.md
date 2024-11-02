---
title: Mensajes de commit
description: Una guía para colaboradores de sitios web sobre el uso de mensajes commit de Git útiles al realizar solicitudes de cambio de sitios web.
---

Para nuestros mensajes de commit, seguimos el estilo proporcionado por [Conventional Commits](https://conventionalcommits.org). No todas las sugerencias son apropiadas para Privacy Guides, así que las principales que utilizamos son:

## Actualización de texto existente

Este ejemplo se puede utilizar para un elemento existente en el sitio web, pero que incluye una pequeña actualización en la descripción.

```text
update: Se agrega una mención a la auditoría de seguridad (#0000)
```

## Adición o eliminación de recomendaciones/páginas

Este ejemplo es para añadir o eliminar un elemento. Puedes explicar por qué se ha eliminado en el párrafo de commit que figura a continuación. Nótese el "!" añadido para llamar la atención sobre un cambio importante.

```text
update!: Remove foobar (#0000)

Foobar was removed due to it having numerious security issues and being unmaintained.
```

En realidad, puedes añadir un `!` a _cualquiera_ de los tipos de esta página para denotar cambios particularmente grandes, pero aquí es donde generalmente será más apropiado.

## Característica/mejora

Para las nuevas características o mejoras del sitio, por ejemplo, las cosas que tienen la etiqueta `enhancements` en GitHub, puede ser apropiado destacar estos con:

```text
feat: Add blah blah (#0000)

This change adds the forum topics to the main page
```

## Cambios menores

Pequeños cambios que **no afectan al significado** del artículo, por ejemplo, corregir una errata, corregir la gramática, cambiar el formato/espacios en blanco, actualizaciones de CSS, etc.

```text
style: Typo correction in VPN overview
```

## Tipos relacionados con el desarrollo

Estos tipos de commit se utilizan normalmente para cambios que no serán visibles para el público en general.

Utilizamos `fix:` para los cambios que corrigen errores relacionados con el sitio. Estas cosas suelen tener la etiqueta `bug` en GitHub.

```text
fix: Remove broken Invidious embeds (#0000)
```

Usamos `docs:` para indicar cambios en la documentación para desarrolladores de este sitio web, incluyendo (pero no limitado a) por ejemplo el archivo README, o la mayoría de las páginas en `/docs/about` o `/docs/meta`:

```text
docs: Update Git commit message guidelines (#0000)
```

Utilizamos `build:` para los commits relacionados con nuestro proceso de compilación, principalmente actualizaciones de dependencias.

```text
build: Bump modules/mkdocs-material from 463e535 to 621a5b8
```

Utilizamos `ci:` para los commits relacionados con GitHub Actions, DevContainers u otras plataformas de compilación automatizada.

```text
ci: Update Netlify config (#0000)
```

Utilizamos `refactor:` para los cambios que no solucionan un error ni añaden una funcionalidad, por ejemplo, la reordenación de archivos, el orden de navegación, etc.

```text
refactor: Move docs/assets to theme/assets
```
