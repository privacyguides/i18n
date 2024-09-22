---
title: Mensajes de commit
description: A guide for website contributors on using useful Git commit messages when making website change requests.
---

Para nuestros mensajes de commit, seguimos el estilo proporcionado por [Conventional Commits](https://conventionalcommits.org). No todas las sugerencias son apropiadas para Privacy Guides, así que las principales que utilizamos son:

## Actualización de texto existente

Este ejemplo se puede utilizar para un elemento existente en el sitio web, pero que incluye una pequeña actualización en la descripción.

```text
update: Se agrega una mención a la auditoría de seguridad (#0000)
```

## Addition or removal of recommendations/pages

This example is for the addition or removal of an item. You may elaborate why it was removed in the commit paragraph below. Note the extra `!` to draw attention to a major change.

```text
update!: Remove foobar (#0000)

Foobar was removed due to it having numerious security issues and being unmaintained.
```

You can actually add a `!` to _any_ of the types on this page to denote particularly large changes, but this is generally where it will be most appropriate.

## Feature/enhancement

For new features or enhancements to the site, e.g. things that have the `enhancements` label on GitHub, it may be appropriate to signify these with:

```text
feat: Add blah blah (#0000)

This change adds the forum topics to the main page
```

## Minor changes

Small changes that **don't affect the meaning** of the article, e.g. correcting a typo, fixing grammar, changing formatting/whitespace, CSS updates, etc.

```text
style: Typo correction in VPN overview
```

## Development-related types

These commit types are typically used for changes that won't be visible to the general audience.

We use `fix:` for changes that fix site related bugs. These things will usually have the `bug` label on GitHub.

```text
fix: Remove broken Invidious embeds (#0000)
```

We use `docs:` to denote changes to the developer documentation for this website, including (but not limited to) for example the README file, or most pages in `/docs/about` or `/docs/meta`:

```text
docs: Update Git commit message guidelines (#0000)
```

We use `build:` for commits related to our build process, mainly dependency updates.

```text
build: Bump modules/mkdocs-material from 463e535 to 621a5b8
```

We use `ci:` for commits related to GitHub Actions, DevContainers, or other automated build platforms.

```text
ci: Update Netlify config (#0000)
```

We use `refactor:` for changes which neither fix a bug nor add a feature, e.g. rearranging files, navigation order, etc.

```text
refactor: Move docs/assets to theme/assets
```
