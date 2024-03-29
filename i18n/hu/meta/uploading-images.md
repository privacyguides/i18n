---
title: Képek feltöltése
---

Íme néhány általános szabály a Privacy Guides-hoz való hozzájáruláshoz:

## Képek

- **Előnyben részesítjük** az SVG képeket, de ha ilyenek nem léteznek, használhatunk PNG képeket is

A vállalati logók mérete:

- 128x128px
- 384x128px

## Optimalizálás

### PNG

Használd az [OptiPNG-t](https://sourceforge.net/projects/optipng) a PNG kép optimalizálásához:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[Scour](https://github.com/scour-project/scour) all SVG images.

Inkscape-ben:

1. Fájl > Mentés másként..
2. Típus beállítása: Optimalizált SVG (*.svg)

A **Beállítások** lapon:

- **Number of significant digits for coordinates** > **5**
- [x] Turn on **Shorten color values**
- [x] Turn on **Convert CSS attributes to XML attributes**
- [x] Turn on **Collapse groups**
- [x] Turn on **Create groups for similar attributes**
- [ ] Turn off **Keep editor data**
- [ ] Turn off **Keep unreferenced definitions**
- [x] Turn on **Work around renderer bugs**

In the **SVG Output** tab under **Document options**:

- [ ] Turn off **Remove the XML declaration**
- [x] Turn on **Remove metadata**
- [x] Turn on **Remove comments**
- [x] Turn on **Embeded raster images**
- [x] Turn on **Enable viewboxing**

In the **SVG Output** under **Pretty-printing**:

- [ ] Turn off **Format output with line-breaks and indentation**
- **Indentation characters** > Select **Space**
- **Depth of indentation** > **1**
- [ ] Turn off **Strip the "xml:space" attribute from the root SVG element**

In the **IDs** tab:

- [x] Turn on **Remove unused IDs**
- [ ] Turn off **Shorten IDs**
- **Prefix shortened IDs with** > `leave blank`
- [x] Turn on **Preserve manually created IDs not ending with digits**
- **Preserve the following IDs** > `leave blank`
- **Preserve IDs starting with** > `leave blank`

#### CLI

Ugyanez érhető el a [Scour](https://github.com/scour-project/scour) paranccsal is:

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
