---
title: Uploading Images
description: A guide for website contributors on uploading images in the proper format and location.
---

If you make changes to this website that involve adding new images or replacing existing ones, here are a couple of general recommendations:

## Bilder

- We **prefer** SVG images, but if those do not exist we can use PNG images. Additionally, for cover images, we prefer that they are obtained from [Unsplash](https://unsplash.com) and are in the WebP format.

Firmenlogos haben eine Leinwandgröße von:

- 128 x 128 px
- 384 x 128 px

## Optimierung

### PNG

Use the [OptiPNG](https://sourceforge.net/projects/optipng) tool to optimize PNG images:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[Scour](https://github.com/scour-project/scour) alle SVG-Bilder.

In Inkscape:

1. Speichern unter...
2. Dateityp auf "Optimiertes SVG (*.svg)" setzen

In der **Optionen** Registerkarte:

- **Anzahl der signifikaten Stellen für Koordinaten** > **5**
- [x] Einschalten **Farbwerte kürzen**
- [x] Einschalten **CSS-Attribute in XML-Attribute umwandeln**
- [x] Einschalten **Gruppen zusammenklappen**
- [x] Einschalten **Gruppen für ähnliche Attribute erstellen**
- [ ] Ausschalten **Editor-Daten erhalten**
- [ ] Ausschalten **Unreferenzierte Definitionen erhalten**
- [x] Einschalten **Renderer-Fehler umgehen**

In der **SVG-Ausgabe** Registerkarte unter **Dokumenteinstellungen**:

- [ ] Ausschalten **XML-Deklaration entfernen**
- [x] Einschalten **Metadaten entfernen**
- [x] Einschalten **Kommentare entfernen**
- [x] Einschalten **Rasterbilder einbetten**
- [x] Einschalten **Viewbox aktivieren**

In der **SVG-Ausgabe** Registerkarte unter **Formatierung**:

- [ ] Ausschalten **Ausgabe mit Zeilenumbrüchen und Einrückungen formatieren**
- **Zeichen für Einrückungen** > Wähle **Leerzeichen**
- **Einrücktiefe** > **1**
- [ ] Ausschalten **"xml:space"-Attribut vom SVG-Wurzelelement entfernen**

In der **IDs** Registerkarte:

- [x] Einschalten **Unbenutzte IDs entfernen**
- [ ] Ausschalten **IDs kürzen**
- **Präfix für gekürzte IDs** > `leer lassen`
- [x] Einschalten **Manuell erstellte IDs, die nicht mit Ziffern enden, erhalten**
- **Folgende IDs erhalten** > `leer lassen`
- **IDs mit folgendem Präfix erhalten** > `leer lassen`

#### CLI

Das Gleiche kann mit dem [Scour](https://github.com/scour-project/scour) Befehl erreicht werden:

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
