---
title: Uploading Images
description: A guide for website contributors on uploading images in the proper format and location.
---

If you make changes to this website that involve adding new images or replacing existing ones, here are a couple of general recommendations:

## Imagens

- We **prefer** SVG images, but if those do not exist we can use PNG images. Additionally, for cover images, we prefer that they are obtained from [Unsplash](https://unsplash.com) and are in the WebP format.

Company logos should be square if possible, and at least 200x200px if they are PNGs (non-vector images).

## Otimização

### PNG

Use the [OptiPNG](https://sourceforge.net/projects/optipng) tool to optimize PNG images:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[Examine](https://github.com/scour-project/scour) todas as imagens SVG.

No Inkscape:

1. File > Save As...
2. Set type to: Optimized SVG (*.svg)

Na aba das **Opções**:

- **Número de dígitos significantes para as coordenadas** > **5**
- [x] Ative **Abreviar valores de cor**
- [x] Ative **Converter atributos CSS em atributos XML**
- [x] Ative **Contrair grupos**
- [x] Ative **Criar grupos para atributos similares**
- [ ] Desative **Manter dados do editor**
- [ ] Desative **Manter definições não referenciadas**
- [x] Ative **Usar recurso alternativo para evitar erros**

Na janela **Exportar em SVG** nas **Opções do documento**:

- [ ] Desative **Remover a declaração XML**
- [x] Ative **Remover metadados**
- [x] Ative **Remover comentários**
- [x] Turn on **Embedded raster images**
- [x] Ative **Ativar viewBox**

Na janela **Exportar em SVG** em **Impressão organizada**:

- [ ] Desative **Formatar saída com quebras de linha e indentação**
- **Caracteres de indentação** > Selecione **Espaço**
- **Profundidade da indentação** > **1**
- [ ] Desative **Retirar o atributo "xml:space" do elemento SVG raiz**

Na janela **Exportar em SVG** em **IDs**:

- [x] Ative **Remover IDs por usar**
- [ ] Desative **Abreviar IDs**
- **Adicionar prefixo nos IDs abreviados com** > `deixe em branco`
- [x] Ative **Preservar IDs criados manualmente que não terminem com dígitos**
- **Preservar os seguintes IDs** > `deixe em branco`
- **Preservar IDs que começam com** > `deixe em branco`

#### CLI

O mesmo pode ser feito com o comando [Scour](https://github.com/scour-project/scour):

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
