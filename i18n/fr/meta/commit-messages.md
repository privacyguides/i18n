---
title: Messages de commit
---

Pour nos messages de commit, nous suivons le style fourni par [Conventional Commits](https://conventionalcommits.org). Toutes ces suggestions ne sont pas appropriées pour Privacy Guides, c'est pourquoi les principales que nous utilisons sont les suivantes :

## Update to existing text

Cet exemple peut être utilisé pour un article déjà présent sur le site, mais dont la description a été légèrement modifiée.

```text
update: Add mention of security audit (#0000)
```

## Addition or removal of recommendations/pages

This example is for the addition or removal of an item. You may elaborate why it was removed in the commit paragraph below. Note the extra `!` to draw attention to a major change.

```text
update!: Remove foobar (#0000)

Foobar was removed due to it having numerious security issues and being unmaintained.
```

You can actually add a `!` to _any_ of the types on this page to denote particularly large changes, but this is generally where it will be most appropriate.

## Message de commit avec correction

Nous utilisons `fix` pour des choses simples comme les fautes d'orthographe ou les bugs liés au site. Ces choses ont généralement le label `correction` ou `bug` sur GitHub.

```text
fix: Correct spelling on XYZ page (#0000)
```

## Fonctionnalité/amélioration

Pour les nouvelles fonctionnalités ou les améliorations du site, par exemple les choses qui ont le label `enhancements` sur GitHub, il peut être approprié de les signifier avec :

```text
feat: Add blah blah (#0000)

This change adds the forum topics to the main page
```

## Development-related types

These commit types are typically used for changes that won't be visible to the general audience.

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

We use `refactor:` for changes which neither fix a bug nor add a feature.

```text
refactor: Move docs/assets to theme/assets
```
