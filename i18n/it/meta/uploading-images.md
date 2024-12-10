---
title: Uploading Images
description: A guide for website contributors on uploading images in the proper format and location.
---

If you make changes to this website that involve adding new images or replacing existing ones, here are a couple of general recommendations:

## Immagini

- We **prefer** SVG images, but if those do not exist we can use PNG images. Additionally, for cover images, we prefer that they are obtained from [Unsplash](https://unsplash.com) and are in the WebP format.

Company logos should be square if possible, and at least 200x200px if they are PNGs (non-vector images).

## Ottimizzazione

### PNG

Use the [OptiPNG](https://sourceforge.net/projects/optipng) tool to optimize PNG images:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

Utilizza [Scour](https://github.com/scour-project/scour) per ripulire tutte le immagini SVG.

Su Inkscape:

1. File > Save As...
2. Set type to: Optimized SVG (*.svg)

Nella scheda **Opzioni**:

- **Numero di cifre significative per le coordinate:** > **5**
- [x] Attiva **Abbrevia i valori dei colori**
- [x] Attiva **Converte gli attributi CSS in attributi XML**
- [x] Attiva **Unisci i gruppi**
- [x] Attiva **Crea gruppi per attributi simili**
- [ ] Disattiva **Mantieni i dati dell'editor**
- [ ] Disattiva **Mantieni le definizioni senza riferimenti**
- [x] Attiva **Correggi gli errori di rendering**

Nella scheda **Output SVG**, in **Opzioni documento**:

- [ ] Disattiva **Rimuovi dichiarazione XML**
- [x] Attiva **Rimuovi metadati**
- [x] Attiva **Rimuovi commenti**
- [x] Attiva **Incorpora immagini raster**
- [x] Attiva **Attiva anteprima**

Nella scheda **Output SVG**, in **Formattazione**:

- [ ] Disattiva **Output con a capo e indentazioni**
- **Caratteri di indentazione** > Seleziona**Spazio**
- **Ampiezza indentazione** > **1**
- [ ] Disattiva **Elimina l'attributo "xml:space" dall'elemento SVG di base**

Nella scheda **ID**:

- [x] Attiva **Rimuovi ID non utilizzati**
- [ ] Disattiva **Abbrevia ID**
- **Prefissa gli ID abbreviati** > `lascia vuoto`
- [x] Attiva **Mantieni ID manuali che non finiscono per cifra**
- **Mantieni gli ID seguenti** > `lascia vuoto`
- **Mantieni gli ID che iniziano con** > `lascia vuoto`

#### CLI

Si può ottenere lo stesso risultato con il comando [Scour](https://github.com/scour-project/scour):

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
