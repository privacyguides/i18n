---
title: Messages de commit
---

Pour nos messages de commit, nous suivons le style fourni par [Conventional Commits](https://conventionalcommits.org). Toutes ces suggestions ne sont pas appropriées pour Privacy Guides, c'est pourquoi les principales que nous utilisons sont les suivantes :

## Message de commit avec correction

Nous utilisons `fix` pour des choses simples comme les fautes d'orthographe ou les bugs liés au site. Ces choses ont généralement le label `correction` ou `bug` sur GitHub.

```text
fix: Correct spelling on XYZ page (#0000)
```

## Mise à jour du site

Cet exemple concerne la suppression d'un élément (mais il pourrait également être utilisé pour un ajout) ; vous pouvez expliquer pourquoi il a été supprimé dans le paragraphe d'engagement ci-dessous. Il peut également être utilisé pour l'ajout de nouvelles pages.

```text
update: Remove foobar (#0000)

Foobar was removed due to it having numerious security issues and being unmaintained.
```

## Mise à jour d'un élément spécifique

Cet exemple peut être utilisé pour un article déjà présent sur le site, mais dont la description a été légèrement modifiée.

```text
foobar: Add mention of security audit (#0000)
```

## Fonctionnalité/amélioration

Pour les nouvelles fonctionnalités ou les améliorations du site, par exemple les choses qui ont le label `enhancements` sur GitHub, il peut être approprié de les signifier avec :

```text
feat: Add blah blah (#0000)

This change adds the forum topics to the main page
```

## Mise à jour de module

Les mises à jour des dépendances suivent les recommandations normales qui consistent à commencer par :

```text
chore: Bump modules/mkdocs-material from 463e535 to 621a5b8
```
