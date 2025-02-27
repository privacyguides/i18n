---
title: Uploading Images
description: A guide for website contributors on uploading images in the proper format and location.
---

If you make changes to this website that involve adding new images or replacing existing ones, here are a couple of general recommendations:

## Afbeeldingen

- We **prefer** SVG images, but if those do not exist we can use PNG images. Additionally, for cover images, we prefer that they are obtained from [Unsplash](https://unsplash.com) and are in the WebP format.

Company logos should be square if possible, and at least 200x200px if they are PNGs (non-vector images).

## Optimalisatie

### PNG

Use the [OptiPNG](https://sourceforge.net/projects/optipng) tool to optimize PNG images:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[Scour](https://github.com/scour-project/scour) alle SVG-afbeeldingen.

In Inkscape:

1. File > Save As...
2. Set type to: Optimized SVG (*.svg)

In het tabblad **Opties**:

- **Aantal significante cijfers voor coördinaten** > **5**
- [x] Zet aan **Kleurwaarden inkorten**
- [x] Zet **aan Zet CSS-attributen om in XML-attributen**
- [x] Zet **aan Samengevoegde groepen**
- [x] Zet **aan Maak groepen voor vergelijkbare kenmerken**
- [ ] Schakel **Bewaar bewerkingsgegevens** uit
- [ ] Schakel **uit zonder verwijzing gedefinieerde definities**
- [x] Zet **Werk rond renderbugs** aan

In het tabblad **SVG-uitvoer** onder **Documentopties**:

- [ ] Schakel **Verwijder de XML declaratie** uit
- [x] Zet **Metadata verwijderen** aan
- [x] Schakel **Reacties verwijderen** in
- [x] Turn on **Embedded raster images**
- [x] Zet **'viewboxen' aan**

In de **SVG Output** onder **Pretty-printing**:

- [ ] Schakel **Formatteer uitvoer uit met regeleinden en inspringen**
- **Inspringing tekens** > Selecteer **spatie**
- **Inspringing** > **1**
- [ ] Schakel **Strip het kenmerk "xml:space" uit het hoofdSVG-element**

In het **IDs** tabblad:

- [x] Schakel in **Ongebruikte ID's verwijderen**
- [ ] Schakel **Korte ID's** uit
- **Voorvoegsel verkorte IDs met** > `leeg laten`
- [x] Zet **Handmatig aangemaakte IDs aan die niet eindigen met cijfers**
- **Behoud de volgende IDs** > `laat leeg`
- **Behoud ID's beginnend met** > `laat leeg`

#### CLI

Hetzelfde kan worden bereikt met het commando [Scour](https://github.com/scour-project/scour):

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

Use the [cwebp](https://developers.google.com/speed/webp/docs/using) command to convert PNG or JPEG image files to WebP format:

```bash
cwebp -q 70 -m 6 input_file -o output.webp
```
