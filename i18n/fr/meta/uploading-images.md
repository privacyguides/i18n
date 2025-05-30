---
title: Uploading Images
description: A guide for website contributors on uploading images in the proper format and location.
---

If you make changes to this website that involve adding new images or replacing existing ones, here are a couple of general recommendations:

## Images

- We **prefer** SVG images, but if those do not exist we can use PNG images. Additionally, for cover images, we prefer that they are obtained from [Unsplash](https://unsplash.com) and are in the WebP format.

Company logos should be square if possible, and at least 200x200px if they are PNGs (non-vector images).

## Optimisation

### PNG

Use the [OptiPNG](https://sourceforge.net/projects/optipng) tool to optimize PNG images:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[Scour](https://github.com/scour-project/scour) toutes les images SVG.

Dans Inkscape :

1. File > Save As...
2. Set type to: Optimized SVG (*.svg)

Dans l'onglet **Options** :

- **Nombre de chiffres significatifs pour les coordonnées** > **5**
- [x] Activez **Raccourcir les valeurs de couleur**
- [x] Activez **Convertir les attributs CSS en attributs XML**
- [x] Activez **Réduire les groupes**
- [x] Activez **Créer des groupes pour des attributs similaires**
- [ ] Désactivez **Conserver les données de l'éditeur**
- [ ] Désactivez **Conserver les définitions non référencées**
- [x] Activez **Contourner les bugs du moteur de rendu**

Dans l'onglet **Sortie SVG** sous **Options du document** :

- [ ] Désactivez **Supprimer la déclaration XML**
- [x] Activez **Supprimer les métadonnées**
- [x] Activez **Supprimer les commentaires**
- [x] Turn on **Embedded raster images**
- [x] Activez **Activer le viewboxing**

Dans le document **Sortie SVG** sous **Pretty-printing** :

- [ ] Désactivez **Formatage de la sortie avec sauts de ligne et indentation**
- **Caractères d'indentation** > Sélectionnez **Espace**
- **Profondeur de l'indentation** > **1**
- [ ] Désactivez **Supprimer l'attribut "xml:space" de l'élément SVG racine**

Dans l'onglet **identifiants** :

- [x] Activez **Supprimer les identifiants inutilisés**
- [ ] Désactivez **Raccourcir les identifiants**
- **Préfixer les identifiants raccourcis avec** > `leave blank`
- [x] Activez **Préserver les identifiants créés manuellement ne se terminant pas par des chiffres**
- **Conserver les identifiants suivants** > `leave blank`
- **Préserver les identifiants commençant par** > `leave blank`

#### Invite de commande

La même chose peut être réalisée avec la commande [Scour](https://github.com/scour-project/scour) :

```bash
scour --set-precision=5 \
      --create-groups \
      --renderer-workaround \
      --remove-descriptive-elements \
      --enable-comment-stripping \
      --enable-viewboxing \
      --indent=space \
      --nindent=1 \
      --no-line-breaks \
      --enable-id-stripping \
      --protect-ids-noninkscape \
      input.svg output.svg
```

### WebP

Use the [`cwebp`](https://developers.google.com/speed/webp/docs/using) command to convert PNG or JPEG image files to WebP format:

```bash
cwebp -m 6 input_file -o output.webp
```
