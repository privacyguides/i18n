---
title: Uploading Images
description: A guide for website contributors on uploading images in the proper format and location.
---

If you make changes to this website that involve adding new images or replacing existing ones, here are a couple of general recommendations:

## Imagens

- Nós **preferimos** imagens SVG, mas se elas não existirem, você pode usar imagens PNG. Além disso, para imagens de capa, preferimos que elas sejam obtidas do [Unsplash](https://unsplash.com) e estejam no formato WebP.

Os logotipos da empresa devem ser quadrados, se possível, e ter pelo menos 200x200px se forem PNGs (imagens não vetoriais).

## Otimização

### PNG

Use a ferramenta [OptiPNG](https://sourceforge.net/projects/optipng) para otimizar imagens PNG:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[Examine](https://github.com/scour-project/scour) todas as imagens SVG.

In Inkscape:

1. Arquivo > Salvar como...
2. Definir o tipo como: SVG otimizado (*.svg)

Na guia **Opções**:

- **Número de dígitos significativos para coordenadas** > **5**
- [x] Ativar a opção **Reduzir valores de cor**
- [x] Ative a opção **Converter atributos CSS em atributos XML**
- [x] Turn on **Collapse groups**
- [x] Turn on **Create groups for similar attributes**
- [ ] Turn off **Keep editor data**
- [ ] Turn off **Keep unreferenced definitions**
- [x] Turn on **Work around renderer bugs**

In the **SVG Output** tab under **Document options**:

- [ ] Turn off **Remove the XML declaration**
- [x] Turn on **Remove metadata**
- [x] Turn on **Remove comments**
- [x] Turn on **Embedded raster images**
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

The same can be achieved with the [Scour](https://github.com/scour-project/scour) command:

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

Use o comando [cwebp](https://developers.google.com/speed/webp/docs/using) para converter arquivos de imagem PNG ou JPEG para o formato WebP:

```bash
cwebp -q 70 -m 6 input_file -o output.webp
```
