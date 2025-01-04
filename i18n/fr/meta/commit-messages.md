---
title: Messages de commit
description: Un guide pour les contributeurs de sites web sur l'utilisation de messages de commit Git utiles lors des demandes de modification de sites web.
---

Pour nos messages de commit, nous suivons le style fourni par [Conventional Commits](https://conventionalcommits.org). Toutes ces suggestions ne sont pas appropriées pour Privacy Guides, c'est pourquoi les principales que nous utilisons sont les suivantes :

## Mettre à jour le texte existant

Cet exemple peut être utilisé pour un article déjà présent sur le site, mais dont la description a été légèrement modifiée.

```text
mise à jour : ajout de la mention de l'audit de sécurité (#0000)
```

## Ajout ou suppression de recommandations/pages

Cet exemple concerne l'ajout ou le retrait d'un élément. Vous pouvez expliquer pourquoi il a été supprimé dans le paragraphe d'engagement ci-dessous. Notez le `!` supplémentaire pour attirer l'attention sur un changement majeur.

```text
mise à jour : Suppression de foobar (#0000)

Foobar a été supprimé car il présente de nombreux problèmes de sécurité et n'est pas maintenu.
```

Vous pouvez en fait ajouter un `!` à _tous_ les types de cette page pour indiquer des changements particulièrement importants, mais c'est généralement ici que cela sera le plus approprié.

## Fonctionnalité/amélioration

Pour les nouvelles fonctionnalités ou les améliorations du site, par exemple les choses qui ont le label `enhancements` sur GitHub, il peut être approprié de les signifier avec :

```text
feat: Ajouter blah blah (#0000)

Ce changement ajoute les sujets du forum à la page principale
```

## Modifications mineures

Petites modifications qui **n'affectent pas le sens** de l'article, par exemple la correction d'une coquille, la correction de la grammaire, la modification du formatage/de l'espace blanc, les mises à jour CSS, etc.

```text
style : Correction d'une faute d'orthographe dans la présentation du VPN
```

## Types d'activités liées au développement

Ces types de livraisons sont généralement utilisés pour les modifications qui ne seront pas visibles par le grand public.

Nous utilisons `fix:` pour les changements qui corrigent les bogues liés au site. Ces choses ont généralement le label `correction` ou `bug` sur GitHub.

```text
fix : Suppression des liens Invidious cassés (#0000)
```

Nous utilisons `docs:` pour indiquer les changements apportés à la documentation du développeur pour ce site web, y compris (mais sans s'y limiter) par exemple le fichier README, ou la plupart des pages dans `/docs/about` ou `/docs/meta` :

```text
docs : Mise à jour des directives pour les messages de commit Git (#0000)
```

Nous utilisons `build:` pour les commits liés à notre processus de construction, principalement les mises à jour de dépendances.

```text
build : Modification du module/mkdocs-material de 463e535 à 621a5b8
```

Nous utilisons `ci:` pour les commits liés aux actions GitHub, aux DevContainers, ou à d'autres plateformes de construction automatisées.

```text
ci : Mise à jour de la configuration de Netlify (#0000)
```

Nous utilisons `refactor:` pour les changements qui ne corrigent pas de bogues et n'ajoutent pas de fonctionnalité, par exemple la réorganisation des fichiers, l'ordre de navigation, etc.

```text
refactoriser : Déplacer docs/assets vers theme/assets
```
