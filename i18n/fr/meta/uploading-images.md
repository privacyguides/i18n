---
title: Téléversement d'images
description: Un guide pour les contributeurs de notre site web pour téléverser des images dans le format et à l'emplacement appropriés.
---

Si vous apportez des modifications à ce site web qui impliquent l'ajout de nouvelles images ou le remplacement d'images existantes, voici quelques recommandations générales :

## Images

- Nous **préférons** des images SVG, mais si celles-ci n'existent pas, nous pouvons utiliser des images PNG. En outre, pour les images de couverture, nous préférons qu'elles proviennent d'[Unsplash](https://unsplash.com) et qu'elles soient au format WebP.

Les logos des entreprises doivent être carrés si possible, et au moins 200x200px s'il s'agit de PNG (images non vectorielles).

## Optimisation

### PNG

Utilisez [OptiPNG](https://sourceforge.net/projects/optipng) pour optimiser l'image PNG :

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[Scour](https://github.com/scour-project/scour) toutes les images SVG.

Dans Inkscape :

1. Fichier > Enregistrer sous...
2. Définir le type à : SVG optimisé (*.svg)

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
- [x] Activez **Images matricielles incorporées**
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

Utilisez la commande [`cwebp`](https://developers.google.com/speed/webp/docs/using) pour convertir des fichiers images PNG ou JPEG au format WebP :

```bash
cwebp -m 6 input_file -o output.webp
```
